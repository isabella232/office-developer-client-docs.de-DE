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
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7ebb33a5b98cebedfca7fb5923e62486bfd85696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790517"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="44588-104">Anruf XLL-Funktionen aus der Funktions-Assistenten oder Dialogfelder ersetzen</span><span class="sxs-lookup"><span data-stu-id="44588-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="44588-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="44588-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="44588-106">Microsoft Excel ruft in der Regel XLL-Funktionen während der normalen neuberechnung der Arbeitsmappe oder einen Teil davon ein, wenn die Berechnung von einem Makro gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="44588-106">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro.</span></span> <span data-ttu-id="44588-107">Denken Sie daran, dass die Funktion möglicherweise nicht in einer Formel der Zelle befinden sich jedoch möglicherweise Teil der Definition eines benannten Bereichs oder einer bedingten Formatierung Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="44588-107">Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="44588-108">Es gibt zwei Situationen, in dem eine Funktion aus einer Excel-Dialogfeld aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="44588-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="44588-109">Eine ist im Dialogfeld **Funktionsargumente einfügen** , in dem Benutzer eine Funktion Anruf ein Argument zu einem Zeitpunkt erstellen können.</span><span class="sxs-lookup"><span data-stu-id="44588-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="44588-110">Das andere ist Formeln werden geändert und erneut eingegeben von Excel in das Dialogfeld **Ersetzen** .</span><span class="sxs-lookup"><span data-stu-id="44588-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="44588-111">Das Dialogfeld **Funktionsargumente einfügen** sollten Sie nicht der Funktion normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44588-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="44588-112">Möglicherweise dauert sehr lange ausführen, und Sie möchten nicht die Verwendung des Dialogfelds verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="44588-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="44588-113">Das Dialogfeld **Funktion einfügen** und das Dialogfeld **Ersetzen** müssen das Windows-Klasse Namen **Bosa_sdm_XL**n, wobei n eine Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="44588-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL**n, where n is a number.</span></span> <span data-ttu-id="44588-114">Windows bietet eine API-Funktion, **GetClassName**, die dieser Name aus einem Windows-Handle eines HWND Variablentyp abruft.</span><span class="sxs-lookup"><span data-stu-id="44588-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="44588-115">Es bietet auch eine andere Funktion, **EnumWindows**, die eine angegebene Callback-Funktion (innerhalb der DLL) aufruft einmal für jedes Fenster der obersten Ebene, das zurzeit geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="44588-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="44588-116">Die Callback-Funktion muss nur die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="44588-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="44588-117">Überprüfen Sie, ob das übergeordnete Element dieses Fenster der aktuellen Instanz von Excel ist (falls es mehrere Instanzen ausgeführt sind).</span><span class="sxs-lookup"><span data-stu-id="44588-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="44588-118">Rufen Sie den Klassennamen aus dem Handle vom Windows übergeben.</span><span class="sxs-lookup"><span data-stu-id="44588-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="44588-119">Überprüfen Sie, ob der Klassenname des Formulars **Bosa_sdm_XL**n ist.</span><span class="sxs-lookup"><span data-stu-id="44588-119">Check if the class name is of the form **bosa_sdm_XL**n.</span></span>
    
4. <span data-ttu-id="44588-120">Wenn Sie zum unterscheiden zwischen den beiden Dialogfeldern müssen, überprüfen Sie, ob der Titel des Dialogfelds identifizierende Text enthält.</span><span class="sxs-lookup"><span data-stu-id="44588-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="44588-121">Der Titel des Fensters wird mithilfe des Windows-API-Aufrufs **GetWindowText**abgerufen.</span><span class="sxs-lookup"><span data-stu-id="44588-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="44588-122">Der folgende C++-Code zeigt ein-Klasse und Rückruf an Windows übergeben werden, mit dem diese Schritte ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44588-122">The following C++ code shows a class and callback to be passed to Windows that performs these steps.</span></span> <span data-ttu-id="44588-123">Dies wird durch die Funktionen den Anruf Test speziell für entweder der betreffenden Dialogfelder bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="44588-123">This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="44588-124">Fenstertitel für zukünftige Versionen von Excel können sich ändern, und dieser Code ungültig.</span><span class="sxs-lookup"><span data-stu-id="44588-124">Window titles of future Excel versions might change and invalidate this code.</span></span> <span data-ttu-id="44588-125">Beachten Sie außerdem, dass wenn **Window_title_text** auf **null festgelegt** wird ignoriert Titel in der Callback-Suche, hat.</span><span class="sxs-lookup"><span data-stu-id="44588-125">Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
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

<span data-ttu-id="44588-126">Das Dialogfeld **Funktion einfügen** besitzt keines Titels, sodass die folgende Funktion eine Suchzeichenfolge Titel des übergibt "", d. h., eine leere Zeichenfolge an den Rückruf, um anzugeben, dass die Bedingung Übereinstimmung besteht darin, dass das Fenster keinen Titel haben sollen.</span><span class="sxs-lookup"><span data-stu-id="44588-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="44588-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44588-127">See also</span></span>



[<span data-ttu-id="44588-128">Zugriff auf XLL-Code in Excel (engl.)</span><span class="sxs-lookup"><span data-stu-id="44588-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="44588-129">Aufrufen von Excel von der DLL oder XLL aus</span><span class="sxs-lookup"><span data-stu-id="44588-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="44588-130">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="44588-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

