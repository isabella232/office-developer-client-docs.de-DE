---
title: Entwickeln von XLLs für Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Add-Ins – [excel 2007],Entwickeln von XLLs – [Excel 2007],XLLs – [Excel 2007], Entwickeln
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301659"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="0bd68-104">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="0bd68-104">Developing Excel XLLs</span></span>

<span data-ttu-id="0bd68-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0bd68-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0bd68-p101">Der Hauptgrund für das Schreiben von Microsoft Excel XLLs und verwenden der C-API ist die Erstellung von Hochleistungs-Tabellenfunktionen. Die Anwendungsszenarien leistungsstarker Funktionen – und ab Excel 2007 die Möglichkeit, Multithread-Schnittstellen auf leistungsstarke Serverressourcen zu schreiben – machen sie zu einem wichtigen Bestandteil der Excel-Erweiterbarkeit. Die Leistung von XLLs wurde in Excel 2007 durch das Hinzufügen neuer Datentypen und die Unterstützung von Multithreading weiter verbessert.</span><span class="sxs-lookup"><span data-stu-id="0bd68-p101">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions. The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility. The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="0bd68-p102">Die C-API verfügt nicht über die leistungsstarken Features zur schnellen Entwicklung von Microsoft Visual Basic for Applications (VBA) über COM oder Microsoft .NET Framework. Die Speicherverwaltung ist lediglich rudimentär, weswegen mehr Verantwortung beim Entwickler liegt. Viele Excel-Features, die über COM durch VBA und .NET Framework verfügbar sind, sind in der C-API nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0bd68-p102">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework. Memory management is low level, and therefore puts greater responsibility on the developer. Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="0bd68-112">Konzepte der Excel-Programmierung</span><span class="sxs-lookup"><span data-stu-id="0bd68-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="0bd68-113">Arbeiten mit DLLs</span><span class="sxs-lookup"><span data-stu-id="0bd68-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="0bd68-114">Zugreifen auf XLL-Code in Excel</span><span class="sxs-lookup"><span data-stu-id="0bd68-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="0bd68-115">Aufrufen von XLL-Funktionen aus dem Funktionsassistenten oder Ersetzen von Dialogfeldern</span><span class="sxs-lookup"><span data-stu-id="0bd68-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="0bd68-116">Aufrufen von Excel von der DLL oder XLL aus</span><span class="sxs-lookup"><span data-stu-id="0bd68-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="0bd68-117">Erstellen von XLLs</span><span class="sxs-lookup"><span data-stu-id="0bd68-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="0bd68-118">Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken</span><span class="sxs-lookup"><span data-stu-id="0bd68-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="0bd68-119">Multithreading und Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="0bd68-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="0bd68-120">Asynchrone benutzerdefinierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="0bd68-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="0bd68-121">Clustersichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="0bd68-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="0bd68-122">Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="0bd68-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="0bd68-123">Anzeigen von Dialogfeldern aus einer DLL oder XLL</span><span class="sxs-lookup"><span data-stu-id="0bd68-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="0bd68-124">Zugreifen auf Excel-Instanz- und Hauptfensterhandles</span><span class="sxs-lookup"><span data-stu-id="0bd68-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="0bd68-125">Abwärtskompatibilität</span><span class="sxs-lookup"><span data-stu-id="0bd68-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

