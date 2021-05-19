---
title: Anzeigen von Dialogfelder aus einer DLL oder XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [excel 2007], Anzeigen von Dialogfelder aus,Dialogfelder [Excel 2007], Anzeigen aus einer DLL oder XLL,DLLs [Excel 2007], Anzeigen von Dialogfelder aus
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417868"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="a1ebf-104">Anzeigen von Dialogfelder aus einer DLL oder XLL</span><span class="sxs-lookup"><span data-stu-id="a1ebf-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="a1ebf-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a1ebf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a1ebf-106">Um ein Win32-Dialogfeld mit z. B. der Windows SDK-Funktion **DialogBox** anzuzeigen, müssen Sie zuerst die vollständige 32-Bit-Instanz und die Hauptfensterziehpunkte für Excel abrufen.</span><span class="sxs-lookup"><span data-stu-id="a1ebf-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="a1ebf-107">Weitere Informationen finden Sie unter [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="a1ebf-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="a1ebf-108">Wenn Ihr Projekt die Dialogfeldressource enthält, müssen Sie mehrere Schritte ausführen, um die Nachrichtenbehandlungsroutine auf die des neu angezeigten Dialogfelds zu setzen und die Excel-Nachrichtenbehandlungsroutine wiederherzustellen, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a1ebf-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="a1ebf-109">Der Beispielbefehl [fShowDialog](fshowdialog.md) im Generic-Projekt veranschaulicht die Verwendung der Windows-Funktionen, um dies ordnungsgemäß auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a1ebf-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="a1ebf-110">Sie können auch Dialogfelder mit der C-API anzeigen, ohne Windows SDK-Funktionen verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="a1ebf-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="a1ebf-111">Die Dialogfeldfunktionen der C-API sind jedoch im Vergleich zu Windows, Visual Basic for Applications (VBA) oder Microsoft Foundation Classes (MFC) sehr eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="a1ebf-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="a1ebf-112">(Beispielsweise sind C-API-Dialogfelder immer modal).</span><span class="sxs-lookup"><span data-stu-id="a1ebf-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1ebf-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1ebf-113">See also</span></span>



[<span data-ttu-id="a1ebf-114">Erstellen von XLLs</span><span class="sxs-lookup"><span data-stu-id="a1ebf-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="a1ebf-115">Entwickeln von DLLs</span><span class="sxs-lookup"><span data-stu-id="a1ebf-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="a1ebf-116">Zugreifen auf Excel-Instanz- und Hauptfensterhandles</span><span class="sxs-lookup"><span data-stu-id="a1ebf-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="a1ebf-117">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="a1ebf-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

