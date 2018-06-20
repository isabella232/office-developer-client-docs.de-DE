---
title: Zugriff auf Excel-Instanz und im Hauptfenster von Handles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugreifen auf excel-Kontrollpunkte, Kontrollpunkte [Excel 2007], den Zugriff auf Excel-Instanzen, die Zugriff auf Fensterhandles [Excel 2007], zugreifen auf
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 035cd2a8423e3ab14f4b2ca4b73fbc39641e54d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790520"
---
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="50453-104">Zugriff auf Excel-Instanz und im Hauptfenster von Handles</span><span class="sxs-lookup"><span data-stu-id="50453-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="50453-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="50453-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="50453-106">Sie müssen manchmal zum Programmieren in der Windows-Umgebung die Microsoft Excel-Instanzzugriffsnummer oder im Hauptfenster von behandeln kennen.</span><span class="sxs-lookup"><span data-stu-id="50453-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="50453-107">Diese Handles sind beispielsweise nützlich, wenn Sie erstellen und Anzeigen von benutzerdefinierten Dialogfeldern in Windows.</span><span class="sxs-lookup"><span data-stu-id="50453-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="50453-108">Es gibt zwei nur XLL-C-API-Funktionen, die Zugriff auf diese Handles bereitstellen: die [XlGetInst](xlgetinst.md) -Funktion und der [XlGetHwnd](xlgethwnd.md) jeweils fungieren.</span><span class="sxs-lookup"><span data-stu-id="50453-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="50453-109">In Win32 sind alle Handles 32-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="50453-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="50453-110">Die **XLOPER** entwickelt wurde, konnte Windows jedoch ein 16-Bit-System.</span><span class="sxs-lookup"><span data-stu-id="50453-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="50453-111">Aus diesem Grund muss die Struktur nur für 16-Bit-Handles zulässig.</span><span class="sxs-lookup"><span data-stu-id="50453-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="50453-112">In Win32 zurück, wenn aufgerufen, wobei **Excel4** oder **Excel4v**, der **XlGetInst** und die Funktion **XlGetHwnd** nur den unteren Teil des das vollständige 32-Bit-Handle.</span><span class="sxs-lookup"><span data-stu-id="50453-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="50453-113">Wenn diese Funktionen mit [Excel12](excel4-excel12.md) oder [Excel12v](excel4v-excel12v.md), aufgerufen werden enthält zurückgegebene **XLOPER12** in Excel 2007 und höhere Versionen das 32-Bit-Handle.</span><span class="sxs-lookup"><span data-stu-id="50453-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="50453-114">Abrufen der vollständigen Instanzzugriffsnummer ist einfach in keiner Version von Excel, wie es an den Windows-Rückruf **DllMain**, übergeben wird, die aufgerufen wird, wenn die DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="50453-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="50453-115">Wenn Sie diese Instanzzugriffsnummer in einer globalen Variablen aufzeichnen, müssen Sie nie die Funktion **XlGetInst** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50453-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="50453-116">Abrufen des Handles Hauptfenster Excel in Excel 2003 und früheren Versionen</span><span class="sxs-lookup"><span data-stu-id="50453-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="50453-117">Um das Hauptfenster Excel Handle in Excel 2003 und früheren Versionen von 32-Bit-Version zu erhalten, müssen Sie zunächst die **XlGetHwnd** -Funktion, um das niedrige Word des tatsächlichen Handles erhalten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50453-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="50453-118">Klicken Sie dann, müssen Sie die Liste der Fenster der obersten Ebene für eine Übereinstimmung mit dem zurückgegebenen niedrig Wort suchen durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="50453-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="50453-119">Der folgende Code veranschaulicht diese Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="50453-119">The following code illustrates the technique.</span></span> 
  
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
  // which match the LoWord retuned by xlGetHwnd.
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

## <a name="see-also"></a><span data-ttu-id="50453-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50453-120">See also</span></span>



[<span data-ttu-id="50453-121">Anzeigen von Dialogfeldern aus innerhalb einer DLL oder XLL</span><span class="sxs-lookup"><span data-stu-id="50453-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="50453-122">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="50453-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="50453-123">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="50453-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

