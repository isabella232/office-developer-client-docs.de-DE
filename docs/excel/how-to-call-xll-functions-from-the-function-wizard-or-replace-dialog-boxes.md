---
title: Anruf XLL-Funktionen aus der Funktions-Assistenten oder Dialogfelder ersetzen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL-Funktionen [excel 2007], ersetzen Sie im Dialogfeld Ersetzen Dialogfeld aufrufen Feld [Excel 2007] aufrufende XLL-Funktionen, Funktions-Assistenten [Excel 2007], [Excel 2007] XLL-Funktionen, XLL-Funktionen aufrufen Aufrufen in Funktions-Assistenten
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7ebb33a5b98cebedfca7fb5923e62486bfd85696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790517"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Anruf XLL-Funktionen aus der Funktions-Assistenten oder Dialogfelder ersetzen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel ruft in der Regel XLL-Funktionen während der normalen neuberechnung der Arbeitsmappe oder einen Teil davon ein, wenn die Berechnung von einem Makro gesteuert wird. Denken Sie daran, dass die Funktion möglicherweise nicht in einer Formel der Zelle befinden sich jedoch möglicherweise Teil der Definition eines benannten Bereichs oder einer bedingten Formatierung Ausdruck.
  
Es gibt zwei Situationen, in dem eine Funktion aus einer Excel-Dialogfeld aufgerufen werden kann. Eine ist im Dialogfeld **Funktionsargumente einfügen** , in dem Benutzer eine Funktion Anruf ein Argument zu einem Zeitpunkt erstellen können. Das andere ist Formeln werden geändert und erneut eingegeben von Excel in das Dialogfeld **Ersetzen** . Das Dialogfeld **Funktionsargumente einfügen** sollten Sie nicht der Funktion normal ausgeführt. Möglicherweise dauert sehr lange ausführen, und Sie möchten nicht die Verwendung des Dialogfelds verlangsamen. 
  
Das Dialogfeld **Funktion einfügen** und das Dialogfeld **Ersetzen** müssen das Windows-Klasse Namen **Bosa_sdm_XL**n, wobei n eine Zahl ist. Windows bietet eine API-Funktion, **GetClassName**, die dieser Name aus einem Windows-Handle eines HWND Variablentyp abruft. Es bietet auch eine andere Funktion, **EnumWindows**, die eine angegebene Callback-Funktion (innerhalb der DLL) aufruft einmal für jedes Fenster der obersten Ebene, das zurzeit geöffnet ist.
  
Die Callback-Funktion muss nur die folgenden Schritte ausführen:
  
1. Überprüfen Sie, ob das übergeordnete Element dieses Fenster der aktuellen Instanz von Excel ist (falls es mehrere Instanzen ausgeführt sind).
    
2. Rufen Sie den Klassennamen aus dem Handle vom Windows übergeben.
    
3. Überprüfen Sie, ob der Klassenname des Formulars **Bosa_sdm_XL**n ist.
    
4. Wenn Sie zum unterscheiden zwischen den beiden Dialogfeldern müssen, überprüfen Sie, ob der Titel des Dialogfelds identifizierende Text enthält. Der Titel des Fensters wird mithilfe des Windows-API-Aufrufs **GetWindowText**abgerufen.
    
Der folgende C++-Code zeigt ein-Klasse und Rückruf an Windows übergeben werden, mit dem diese Schritte ausgeführt. Dies wird durch die Funktionen den Anruf Test speziell für entweder der betreffenden Dialogfelder bezeichnet. 
  
> [!NOTE]
> Fenstertitel für zukünftige Versionen von Excel können sich ändern, und dieser Code ungültig. Beachten Sie außerdem, dass wenn **Window_title_text** auf **null festgelegt** wird ignoriert Titel in der Callback-Suche, hat. 
  
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

Das Dialogfeld **Funktion einfügen** besitzt keines Titels, sodass die folgende Funktion eine Suchzeichenfolge Titel des übergibt "", d. h., eine leere Zeichenfolge an den Rückruf, um anzugeben, dass die Bedingung Übereinstimmung besteht darin, dass das Fenster keinen Titel haben sollen. 
  
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



[Zugriff auf XLL-Code in Excel (engl.)](accessing-xll-code-in-excel.md)
  
[Aufrufen von Excel von der DLL oder XLL aus](calling-into-excel-from-the-dll-or-xll.md)
  
[Entwickeln von Excel-XLLs](developing-excel-xlls.md)

