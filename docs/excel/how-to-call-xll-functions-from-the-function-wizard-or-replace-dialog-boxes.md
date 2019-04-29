---
title: Aufrufen von XLL-Funktionen aus dem Funktionsassistenten oder Ersetzen von Dialogfeldern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL-Funktionen [Excel 2007], Aufruf von Dialogfeld ersetzen, Dialogfeld ersetzen [Excel 2007], Aufrufen von XLL-Funktionen, Funktions-Assistent [Excel 2007], Aufrufen von XLL-Funktionen, XLL-Funktionen [Excel 2007], aufrufen vom Funktions-Assistenten
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11189beed13e2ceb99ef04b7a2f966cb4171915c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410749"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="2cad3-104">Aufrufen von XLL-Funktionen aus dem Funktionsassistenten oder Ersetzen von Dialogfeldern</span><span class="sxs-lookup"><span data-stu-id="2cad3-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="2cad3-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2cad3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2cad3-106">Microsoft Excel ruft in der Regel XLL-Funktionen während der normalen Neuberechnung der Arbeitsmappe oder einen Teil davon, wenn die Berechnung unter der Kontrolle eines Makros ist.</span><span class="sxs-lookup"><span data-stu-id="2cad3-106">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro.</span></span> <span data-ttu-id="2cad3-107">Beachten Sie, dass sich die Funktion möglicherweise nicht in einer Zellformel befindet, aber möglicherweise Teil einer benannten Bereich-Definition oder ein bedingter Formatierungsausdruck ist.</span><span class="sxs-lookup"><span data-stu-id="2cad3-107">Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="2cad3-108">Es gibt zwei Situationen, in denen eine Funktion von einem Excel-Dialogfeld aus aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2cad3-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="2cad3-109">Eins ist das Dialogfeld " **Funktionsargumente einfügen** ", in dem Benutzer einen Funktionsaufruf eines Arguments gleichzeitig erstellen können.</span><span class="sxs-lookup"><span data-stu-id="2cad3-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="2cad3-110">Das andere ist, wenn Formeln geändert und von Excel im Dialogfeld **ersetzen** erneut eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2cad3-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="2cad3-111">Für das Dialogfeld **Funktionsargumente einfügen** möchten Sie möglicherweise nicht, dass ihre Funktion normal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cad3-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="2cad3-112">Möglicherweise dauert es lange, bis Sie ausgeführt werden, und Sie möchten die Verwendung des Dialogfelds nicht verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="2cad3-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="2cad3-113">Sowohl das Dialogfeld **Funktion einfügen** als auch das Dialogfeld **ersetzen** weisen den Windows-Klassennamen **bosa_sdm_XL**n auf, wobei n eine Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="2cad3-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL**n, where n is a number.</span></span> <span data-ttu-id="2cad3-114">Windows bietet eine API-Funktion \*\*\*\*, GetClassName, die diesen Namen aus einem Windows-Handle, einem Variablen Typ HWND, abruft.</span><span class="sxs-lookup"><span data-stu-id="2cad3-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="2cad3-115">Es bietet auch eine weitere Funktion, **EnumWindows**, die eine bereitgestellte Rückruffunktion (innerhalb der dll) einmal für jedes Fenster der obersten Ebene aufruft, das derzeit geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="2cad3-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="2cad3-116">Die Rückruffunktion muss nur die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="2cad3-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="2cad3-117">Überprüfen Sie, ob das übergeordnete Element dieses Fensters die aktuelle Instanz von Excel ist (falls mehrere Instanzen vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="2cad3-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="2cad3-118">Rufen Sie den Klassennamen aus dem Handle ab, das von Windows übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2cad3-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="2cad3-119">Überprüfen Sie, ob der Klassenname das Format **bosa_sdm_XL**n hat.</span><span class="sxs-lookup"><span data-stu-id="2cad3-119">Check if the class name is of the form **bosa_sdm_XL**n.</span></span>
    
4. <span data-ttu-id="2cad3-120">Wenn Sie zwischen den beiden Dialogfeldern unterscheiden müssen, überprüfen Sie, ob der Titel des Dialogfelds einen identifizierenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="2cad3-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="2cad3-121">Der Fenstertitel wird mithilfe des Windows-API-Aufrufs **GetWindowText**abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2cad3-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="2cad3-122">Im folgenden C++-Code wird gezeigt, wie eine Klasse und ein Rückruf an Windows übergeben werden, die diese Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cad3-122">The following C++ code shows a class and callback to be passed to Windows that performs these steps.</span></span> <span data-ttu-id="2cad3-123">Dies wird von den Funktionen aufgerufen, die Test speziell für eines der betreffenden Dialogfelder aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2cad3-123">This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2cad3-124">Fenstertitel zukünftiger Excel-Versionen können sich ändern und diesen Code ungültig machen.</span><span class="sxs-lookup"><span data-stu-id="2cad3-124">Window titles of future Excel versions might change and invalidate this code.</span></span> <span data-ttu-id="2cad3-125">Beachten Sie, dass das Festlegen von **window_title_text** auf **null** den Effekt hat, dass der Fenstertitel in der Rückruf Suche ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="2cad3-125">Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
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

<span data-ttu-id="2cad3-126">Das Dialogfeld **Funktion einfügen** verfügt nicht über einen Titel, sodass die folgende Funktion eine Such Titelzeichenfolge von "", also eine leere Zeichenfolge, an den Rückruf übergibt, um anzugeben, dass die übereinstimmungsbedingung darin besteht, dass das Fenster keinen Titel haben sollte.</span><span class="sxs-lookup"><span data-stu-id="2cad3-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="2cad3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cad3-127">See also</span></span>



[<span data-ttu-id="2cad3-128">Zugreifen auf XLL-Code in Excel</span><span class="sxs-lookup"><span data-stu-id="2cad3-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="2cad3-129">Aufrufen von Excel von der DLL oder XLL aus</span><span class="sxs-lookup"><span data-stu-id="2cad3-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="2cad3-130">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="2cad3-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

