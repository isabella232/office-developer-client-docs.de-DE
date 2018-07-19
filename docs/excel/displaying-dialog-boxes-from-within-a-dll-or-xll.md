---
title: Anzeigen von Dialogfeldern aus innerhalb einer DLL oder XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLLs [excel 2007], Anzeigen von Dialogfeldern aus Dialogfelder [Excel 2007], Anzeigen von aus einer DLL oder XLL DLLs [Excel 2007], Anzeigen von Dialogfeldern
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790405"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="acf0f-104">Anzeigen von Dialogfeldern aus innerhalb einer DLL oder XLL</span><span class="sxs-lookup"><span data-stu-id="acf0f-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="acf0f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="acf0f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="acf0f-106">Um Win32 das Anzeigen eines Dialogfelds verwenden, beispielsweise der Funktion Windows SDK **DialogBox**, müssen Sie zuerst die vollständige 32-Bit-Instanz und im Hauptfenster von Handles für Excel beziehen.</span><span class="sxs-lookup"><span data-stu-id="acf0f-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="acf0f-107">Weitere Informationen finden Sie unter [Zugriff auf Excel-Instanz und Main Fenster behandelt](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="acf0f-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="acf0f-108">Vorausgesetzt, dass das Projekt die Feld-Ressource enthält, müssen Sie nur in mehreren Schritten für die Handhabung von Nachrichten-Routine, die im Dialogfeld neu angezeigten festzulegen und Wiederherstellen die Excel-Nachricht Routine verarbeiten, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="acf0f-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="acf0f-109">Beispiel Befehl [fShowDialog](fshowdialog.md) im generischen Projekt veranschaulicht die Verwendung der Windows-Funktionen dazu ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="acf0f-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="acf0f-110">Sie können auch Dialogfeldern mit der C-API ohne Windows SDK Funktionen verwenden anzeigen.</span><span class="sxs-lookup"><span data-stu-id="acf0f-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="acf0f-111">Allerdings werden die Dialogfeld Feld Funktionen der C-API sehr begrenzt verglichen, mit denen der Windows, Visual Basic für Applikationen (VBA) oder Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="acf0f-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="acf0f-112">(Beispielsweise sind C-API-Dialogfelder immer modal).</span><span class="sxs-lookup"><span data-stu-id="acf0f-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acf0f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acf0f-113">See also</span></span>



[<span data-ttu-id="acf0f-114">Erstellen von XLLs</span><span class="sxs-lookup"><span data-stu-id="acf0f-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="acf0f-115">Entwickeln von DLLs</span><span class="sxs-lookup"><span data-stu-id="acf0f-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="acf0f-116">Zugriff auf Excel-Instanz und im Hauptfenster von Handles</span><span class="sxs-lookup"><span data-stu-id="acf0f-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="acf0f-117">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="acf0f-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

