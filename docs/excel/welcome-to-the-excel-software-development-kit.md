---
title: Willkommen beim Excel Software Development Kit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- excel 2007 xll software development kit,add-ins [Excel 2007]
localization_priority: Normal
ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4de88a12b5fb945c6243e52b77babe88b2d02417
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790577"
---
# <a name="welcome-to-the-excel-software-development-kit"></a><span data-ttu-id="66b8c-104">Willkommen beim Excel Software Development Kit</span><span class="sxs-lookup"><span data-stu-id="66b8c-104">Welcome to the Excel Software Development Kit</span></span>

 <span data-ttu-id="66b8c-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="66b8c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="66b8c-p101">Willkommen bei der Dokumentation zum Excel 2013 XLL Software Development Kit (SDK). Diese Referenz enth�lt konzeptionelle �bersichten, Programmieraufgaben und Beispiele, die Sie beim Entwickeln von Microsoft Excel 2013 XLLs unterst�tzen sollen.</span><span class="sxs-lookup"><span data-stu-id="66b8c-p101">Welcome to the Excel 2013 XLL Software Development Kit (SDK) documentation. This reference contains conceptual overviews, programming tasks, and samples to help you develop Microsoft Excel 2013 XLLs.</span></span>
  
<span data-ttu-id="66b8c-108">�berarbeitet: November 2012</span><span class="sxs-lookup"><span data-stu-id="66b8c-108">Revised: November 2012</span></span>
  
<span data-ttu-id="66b8c-109">Laden Sie das [Excel 2013 XLL SDK](http://go.microsoft.com/fwlink/?LinkID=251082) herunter.</span><span class="sxs-lookup"><span data-stu-id="66b8c-109">Download the [Excel 2013 XLL SDK](http://go.microsoft.com/fwlink/?LinkID=251082).</span></span>
  
<span data-ttu-id="66b8c-110">Das Excel 2013 XLL SDK enth�lt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="66b8c-110">The Excel 2013 XLL SDK includes the following:</span></span>
  
- <span data-ttu-id="66b8c-111">**C-API (Application Programming Interface, Anwendungsprogrammierschnittstelle)** � enth�lt Header- und Quelldateien, die DLLs den Zugriff auf Excel 2013-Funktionen erm�glichen, sowie eine Beschreibung der Schnittstelle, die eine DLL f�r die Arbeit mit dem Excel Add-In-Manager verf�gbar machen sollte.</span><span class="sxs-lookup"><span data-stu-id="66b8c-111">**C application programming interface (API)**—Includes header and source files that enable DLLs to access Excel 2013 functionality, and a description of the interface that a DLL should expose to work with the Excel Add-in Manager.</span></span>
    
- <span data-ttu-id="66b8c-p102">**Microsoft Visual Studio-Projekte** � enth�lt C/C++-Quellcode und veranschaulicht die Verwendung der C-API. Diese Beispielprojekte stellen Beispiele zur Verf�gung und dienen als Ausgangspunkt f�r die Entwicklung eigener Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="66b8c-p102">**Microsoft Visual Studio projects**—Includes C/C++ source code and shows how to use the C API. These sample projects provide examples and they serve as a starting point for your own add-in development.</span></span>
    
<span data-ttu-id="66b8c-114">Die SDK-Dokumentation enth�lt die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="66b8c-114">The SDK documentation contains the following sections:</span></span>
  
- [<span data-ttu-id="66b8c-115">Erste Schritte mit Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="66b8c-115">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)
    
- [<span data-ttu-id="66b8c-116">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="66b8c-116">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
    
- [<span data-ttu-id="66b8c-117">Entwickeln von Excel 2013-Clusterconnectoren</span><span class="sxs-lookup"><span data-stu-id="66b8c-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
    
- [<span data-ttu-id="66b8c-118">Excel XLL-SDK-API-Funktionsreferenz</span><span class="sxs-lookup"><span data-stu-id="66b8c-118">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
    
## <a name="functionality-not-covered"></a><span data-ttu-id="66b8c-119">Nicht behandelte Funktionen</span><span class="sxs-lookup"><span data-stu-id="66b8c-119">Functionality Not Covered</span></span>

<span data-ttu-id="66b8c-120">Die folgenden Themen werden nicht behandelt:</span><span class="sxs-lookup"><span data-stu-id="66b8c-120">The following subjects are not covered:</span></span>
  
- <span data-ttu-id="66b8c-121">Entwickeln von benutzerdefinierten Funktionen und Befehlen in Excel-Makrovorlagen (XLM)</span><span class="sxs-lookup"><span data-stu-id="66b8c-121">Developing user-defined functions and commands in Excel macro (XLM) sheets.</span></span>
    
- <span data-ttu-id="66b8c-122">Erstellen von benutzerdefinierten Funktionen in DLLs, die den Ablauf der Ausf�hrung eines XLM-Makros steuern.</span><span class="sxs-lookup"><span data-stu-id="66b8c-122">Creating user-defined functions in DLLs that control the flow of execution of an XLM macro.</span></span>
    
    <span data-ttu-id="66b8c-123">Diese Funktionen geben einen speziellen Ablaufsteuerungs-Datentyp zur�ck, der in dieser Dokumentation ebenfalls nicht erl�utert wird.</span><span class="sxs-lookup"><span data-stu-id="66b8c-123">Such functions work by returning a special flow control data type, which is also not described in this documentation.</span></span>
    
## <a name="related-links"></a><span data-ttu-id="66b8c-124">Links zu verwandten Themen</span><span class="sxs-lookup"><span data-stu-id="66b8c-124">Related Links</span></span>

[<span data-ttu-id="66b8c-125">Excel Developer Center</span><span class="sxs-lookup"><span data-stu-id="66b8c-125">Excel Developer Center</span></span>](http://msdn.microsoft.com/de-de/office/aa905411.aspx)
  
[<span data-ttu-id="66b8c-126">Office Developer Center</span><span class="sxs-lookup"><span data-stu-id="66b8c-126">Microsoft Office Developer Center</span></span>](http://msdn.microsoft.com/de-de/office/default.aspx)
  
[<span data-ttu-id="66b8c-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span><span class="sxs-lookup"><span data-stu-id="66b8c-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span></span>](http://go.microsoft.com/fwlink/?LinkID=186435)
  

