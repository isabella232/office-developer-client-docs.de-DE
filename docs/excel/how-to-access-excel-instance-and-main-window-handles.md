---
title: Zugriff Excel Instanz- und Hauptfensterhandles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugreifen auf Excel-Handles,Handles [Excel 2007], Zugreifen auf,Excel-Instanzen, Zugriff,Fensterhandles [Excel 2007], Zugriff auf
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310759"
---
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="ddddb-104">Zugriff Excel Instanz- und Hauptfensterhandles</span><span class="sxs-lookup"><span data-stu-id="ddddb-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="ddddb-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ddddb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ddddb-106">Um in der Windows programmieren zu können, müssen Sie manchmal die Microsoft Excel-Instanzhandle oder das Hauptfensterhandle kennen.</span><span class="sxs-lookup"><span data-stu-id="ddddb-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="ddddb-107">Diese Handles sind z. B. hilfreich, wenn Sie benutzerdefinierte Windows erstellen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ddddb-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="ddddb-108">Es gibt zwei nur XLL-C-API-Funktionen, die Zugriff auf diese Handles bieten: die [xlGetInst-Funktion](xlgetinst.md) bzw. [die xlGetHwnd-Funktion.](xlgethwnd.md)</span><span class="sxs-lookup"><span data-stu-id="ddddb-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="ddddb-109">In Win32 sind alle Ziehpunkte 32-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="ddddb-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="ddddb-110">Beim Entwerfen der **XLOPER** war Windows jedoch ein 16-Bit-System.</span><span class="sxs-lookup"><span data-stu-id="ddddb-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="ddddb-111">Daher ist die Struktur nur für 16-Bit-Handles zulässig.</span><span class="sxs-lookup"><span data-stu-id="ddddb-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="ddddb-112">Wenn sie in Win32 mit **Excel4** oder **Excel4v** aufgerufen werden, geben die **xlGetInst-Funktion** und die **xlGetHwnd-Funktion** nur den niedrigen Teil des vollständigen 32-Bit-Handles zurück.</span><span class="sxs-lookup"><span data-stu-id="ddddb-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="ddddb-113">Wenn Excel 2007 und höher mit [Excel12](excel4-excel12.md) oder [Excel12v](excel4v-excel12v.md)aufgerufen werden, enthält die zurückgegebene **XLOPER12** den vollständigen 32-Bit-Handle.</span><span class="sxs-lookup"><span data-stu-id="ddddb-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="ddddb-114">Das Abrufen des vollständigen Instanzhandls ist in jeder Version von Excel einfach, da es an den Windows-Rückruf **DllMain** übergeben wird, der beim Laden der DLL aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ddddb-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="ddddb-115">Wenn Sie dieses Instanzhandle in einer globalen Variablen aufzeichnen, müssen Sie niemals die **xlGetInst-Funktion** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ddddb-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="ddddb-116">Abrufen des Haupt-Excel in Excel 2003 und früher</span><span class="sxs-lookup"><span data-stu-id="ddddb-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="ddddb-117">Um das Haupthandle Excel in Excel 2003 und früheren 32-Bit-Versionen zu erhalten, müssen Sie zuerst die **xlGetHwnd-Funktion** aufrufen, um das Wort "Low" des tatsächlichen Handles zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ddddb-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="ddddb-118">Anschließend müssen Sie die Liste der Fenster auf oberster Ebene durch iterieren, um nach einer Übereinstimmung mit dem zurückgegebenen niedrigen Wort zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ddddb-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="ddddb-119">Der folgende Code veranschaulicht die Technik.</span><span class="sxs-lookup"><span data-stu-id="ddddb-119">The following code illustrates the technique.</span></span> 
  
```cs
typedef struct _EnumStruct
{
  HWND hwnd;  // Return value for Excel main hWnd.
  unsigned short wLoword; //Contains LowWord of the Excel main hWnd
} EnumStruct;
#define CLASS_NAME_BUFFER  50
BOOL CALLBACK EnumProc(HWND hwnd, EnumStruct * pEnum)
{
  // First check the class of the window. Must be "XLMAIN".
  char rgsz[CLASS_NAME_BUFFER];
  GetClassName(hwnd, rgsz, CLASS_NAME_BUFFER);
  if (!lstrcmpi(rgsz, "XLMAIN"))
  {
    // If that hits, check the loword of the window handle.
    if (LOWORD((DWORD) hwnd) == pEnum->wLoword)
    {
      // We have a match, return Excel main hWnd.
      pEnum->hwnd = hwnd;
      return FALSE;
    }
  }
  // No match - continue the enumeration.
  return TRUE;
}
BOOL GetHwnd(HWND * pHwnd)
{
  XLOPER x;
  //
  // xlGetHwnd only returns the LoWord of Excel hWnd
  // so all the windows have to be enumerated to see
  // which match the LoWord returned by xlGetHwnd.
  //
  if (Excel4(xlGetHwnd, &x, 0) == xlretSuccess)
  {
    EnumStruct enm;
    enm.hwnd = NULL;
    enm.wLoword = x.val.w;
    EnumWindows((WNDENUMPROC) EnumProc, (LPARAM) &enm);
    if (enm.hwnd != NULL)
    {
      *pHwnd = enm.hwnd;
      return TRUE;
    }
  }
  return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="ddddb-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddddb-120">See also</span></span>



[<span data-ttu-id="ddddb-121">Anzeigen von Dialogfeldern aus einer DLL oder XLL</span><span class="sxs-lookup"><span data-stu-id="ddddb-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="ddddb-122">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="ddddb-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="ddddb-123">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="ddddb-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

