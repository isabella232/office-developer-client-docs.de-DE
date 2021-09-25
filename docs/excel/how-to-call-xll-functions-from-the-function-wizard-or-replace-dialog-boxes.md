---
title: Aufrufen von XLL-Funktionen aus dem Funktions-Assistenten oder Ersetzen von Dialogfeldern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xll functions [excel 2007], calling from replace dialog box,Replace dialog box [Excel 2007], calling XLL functions,Function Wizard [Excel 2007], calling XLL functions,XLL functions [Excel 2007], calling from Function Wizard
ms.localizationpriority: medium
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3709c3f4736a5eb977bbfdd6f13a1fd9b87f1d7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592977"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Aufrufen von XLL-Funktionen aus dem Funktions-Assistenten oder Ersetzen von Dialogfeldern

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel ruft in der Regel XLL-Funktionen während der normalen Neuberechnung der Arbeitsmappe oder einen Teil davon auf, wenn sich die Berechnung unter der Kontrolle eines Makros befindet. Denken Sie daran, dass sich die Funktion möglicherweise nicht in einer Zellformel befindet, aber Teil einer benannten Bereichsdefinition oder eines bedingten Formatierungsausdrucks sein kann.
  
Es gibt zwei Situationen, in denen eine Funktion aus einem Excel Dialogfeld aufgerufen werden kann. Eins ist das Dialogfeld **"Funktionsargumente einfügen",** in dem Benutzer jeweils ein Argument für einen Funktionsaufruf erstellen können. Die andere ist, wenn Formeln geändert und von Excel im Dialogfeld **Ersetzen** erneut aktiviert werden. Im Dialogfeld **"Funktionsargumente einfügen"** möchten Sie möglicherweise nicht, dass die Funktion normal ausgeführt wird. Dies kann darauf zurückzuführen sein, dass die Ausführung sehr lange dauert und Sie die Verwendung des Dialogfelds nicht verlangsamen möchten. 
  
Sowohl das Dialogfeld **"Funktion einfügen"** als auch das Dialogfeld **"Ersetzen"** weisen den Windows Klassennamen **bosa_sdm_XL** n auf, wobei n eine Zahl ist. Windows stellt eine API-Funktion, **GetClassName,** bereit, die diesen Namen von einem Windows Handle, einem HWND-Variablentyp, abruft. Es stellt auch eine weitere Funktion bereit, **EnumWindows,** die eine bereitgestellte Rückruffunktion (innerhalb der DLL) einmal für jedes Fenster auf oberster Ebene aufruft, das derzeit geöffnet ist.
  
Die Rückruffunktion muss nur die folgenden Schritte ausführen:
  
1. Überprüfen Sie, ob das übergeordnete Element dieses Fensters die aktuelle Instanz von Excel ist (für den Fall, dass mehrere Instanzen ausgeführt werden).
    
2. Rufen Sie den Klassennamen aus dem handle ab, das von Windows übergeben wurde.
    
3. Überprüfen Sie, ob der Klassenname das Formular **bosa_sdm_XL** n aufgibt.
    
4. Wenn Sie zwischen den beiden Dialogfeldern unterscheiden müssen, überprüfen Sie, ob der Titel des Dialogfelds bestimmten Text enthält. Der Fenstertitel wird mithilfe des Windows API-Aufrufs **GetWindowText** abgerufen.
    
Der folgende C++-Code zeigt eine Klasse und einen Rückruf, die an Windows übergeben werden, die diese Schritte ausführt. Dies wird von den Funktionen aufgerufen, die Tests speziell für eines der betreffenden Dialogfelder aufrufen. 
  
> [!NOTE]
> Fenstertitel zukünftiger Excel Versionen können diesen Code ändern und ungültig machen. Beachten Sie außerdem, dass das Festlegen **von window_title_text** auf **NULL** dazu führen kann, dass der Fenstertitel in der Rückrufsuche ignoriert wird. 
  
```cs
#define CLASS_NAME_BUFFSIZE  50
#define WINDOW_TEXT_BUFFSIZE  50
// Data structure used as input to xldlg_enum_proc(), called by
// called_from_paste_fn_dlg(), called_from_replace_dlg(), and
// called_from_Excel_dlg(). These functions tell the caller whether
// the current worksheet function was called from one or either of
// these dialog boxes.
typedef struct
{
  bool is_dlg;
  short low_hwnd;
  char *window_title_text; // set to NULL if don't care
}
  xldlg_enum_struct;
// The callback function called by Windows for every top-level window.
BOOL CALLBACK xldlg_enum_proc(HWND hwnd, xldlg_enum_struct *p_enum)
{
// Check if the parent window is Excel.
// Note: Because of the change from MDI (Excel 2010)
// to SDI (Excel 2013), comment out this step in Excel 2013.
  if(LOWORD((DWORD)GetParent(hwnd)) != p_enum->low_hwnd)
    return TRUE; // keep iterating
  char class_name[CLASS_NAME_BUFFSIZE + 1];
//  Ensure that class_name is always null terminated for safety.
  class_name[CLASS_NAME_BUFFSIZE] = 0;
  GetClassName(hwnd, class_name, CLASS_NAME_BUFFSIZE);
//  Do a case-insensitve comparison for the Excel dialog window
//  class name with the Excel version number truncated.
  size_t len; // The length of the window's title text
  if(_strnicmp(class_name, "bosa_sdm_xl", 11) == 0)
  {
// Check if a searching for a specific title string
    if(p_enum->window_title_text) 
    {
// Get the window's title and see if it matches the given text.
      char buffer[WINDOW_TEXT_BUFFSIZE + 1];
      buffer[WINDOW_TEXT_BUFFSIZE] = 0;
      len = GetWindowText(hwnd, buffer, WINDOW_TEXT_BUFFSIZE);
      if(len == 0) // No title
      {
        if(p_enum->window_title_text[0] != 0)
          return TRUE; // No match, so keep iterating
      }
// Window has a title so do a case-insensitive comparison of the
// title and the search text, if provided.
      else if(p_enum->window_title_text[0] != 0
      && _stricmp(buffer, p_enum->window_title_text) != 0)
        return TRUE; // Keep iterating
    }
    p_enum->is_dlg = true;
    return FALSE; // Tells Windows to stop iterating.
  }
  return TRUE; // Tells Windows to continue iterating.
}
```

Das Dialogfeld **"Funktion einfügen"** hat keinen Titel. Daher übergibt die folgende Funktion die Suchtitelzeichenfolge "", d. h. eine leere Zeichenfolge, an den Rückruf, um anzugeben, dass die Übereinstimmungsbedingung darin besteht, dass das Fenster keinen Titel aufweisen soll. 
  
```cs
bool called_from_paste_fn_dlg(void)
{
    XLOPER xHwnd;
// Calls Excel4, which only returns the low part of the Excel
// main window handle. This is OK for the search however.
    if(Excel4(xlGetHwnd, &xHwnd, 0))
        return false; // Couldn't get it, so assume not
// Search for bosa_sdm_xl* dialog box with no title string.
    xldlg_enum_struct es = {FALSE, xHwnd.val.w, ""};
    EnumWindows((WNDENUMPROC)xldlg_enum_proc, (LPARAM)&es);
    return es.is_dlg;
}
```

## <a name="see-also"></a>Siehe auch



[Zugreifen auf XLL-Code in Excel](accessing-xll-code-in-excel.md)
  
[Aufrufen von Excel von der DLL oder XLL aus](calling-into-excel-from-the-dll-or-xll.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

