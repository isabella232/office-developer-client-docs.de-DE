---
title: Excel XLL-SDK-API-Funktionsreferenz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790497"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="75684-104">Excel XLL-SDK-API-Funktionsreferenz</span><span class="sxs-lookup"><span data-stu-id="75684-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="75684-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75684-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="75684-106">Das Microsoft Excel 2013 XLL SDK enthält die Quelldateien für eine "Framework"-Bibliothek, die das Schreiben von XLLs beschleunigen soll, sowie die zwei Beispielprojekte "Example" und "Generic".</span><span class="sxs-lookup"><span data-stu-id="75684-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="75684-107">Dieser Abschnitt stellt eine Funktionsreferenz für Folgendes bereit:</span><span class="sxs-lookup"><span data-stu-id="75684-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="75684-108">Excel-Rückrufe, die die XLL aufrufen kann</span><span class="sxs-lookup"><span data-stu-id="75684-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="75684-109">XLL-Rückrufe, nach denen Microsoft Excel sucht</span><span class="sxs-lookup"><span data-stu-id="75684-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="75684-110">Wichtige Funktionen in den Beispiel- und Frameworkprojekten</span><span class="sxs-lookup"><span data-stu-id="75684-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="75684-111">Beispiel-Projekte</span><span class="sxs-lookup"><span data-stu-id="75684-111">Sample projects</span></span>

<span data-ttu-id="75684-112">Das Excel 2013 XLL SDK stellt Quelldateien und Microsoft Visual Studio-Projektdateien für die folgenden Beispielprojekte bereit:</span><span class="sxs-lookup"><span data-stu-id="75684-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="75684-113">Das Projekt **Framework** (`SAMPLES\FRAMEWRK\`) enthält ein Projekt, das in einer Dokumentbibliothek, FRAMEWRK.lib, erstellt werden kann, die dann in andere Projekte XLL verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="75684-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="75684-114">Die Bibliothek enthält viele Funktionen und Tools, die das Schreiben von XLLs vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="75684-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="75684-115">Diese Bibliothek wird in den beiden anderen Projekten in Verbindung mit der Headerdatei FRAMEWRK.h verwendet.</span><span class="sxs-lookup"><span data-stu-id="75684-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="75684-116">**Das Beispielprojekt** (`SAMPLES\EXAMPLE\`) enthält ein Projekt, das auf eine XLL, EXAMPLE.xll erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="75684-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="75684-117">Die XLL enthält viele Beispiele in diesem Beispiel wird die Implementierung der XLL-add-in-Schnittstelle-Funktionen wie **XlAutoOpen**und die Verwendung von der Framework-Klassenbibliothek.</span><span class="sxs-lookup"><span data-stu-id="75684-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="75684-118">Das Projekt **generische** (`SAMPLES\GENERIC\`) enthält ein Projekt, das auf eine XLL, GENERIC.xll erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="75684-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="75684-119">Die XLL veranschaulicht verschiedene Beispielfunktionen und -befehle und ist ein guter Ausgangspunkt für das Schreiben eigener XLLs.</span><span class="sxs-lookup"><span data-stu-id="75684-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="75684-120">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="75684-120">In this section</span></span>

- [<span data-ttu-id="75684-121">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="75684-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="75684-122">C-API-R�ckruf funktioniert Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="75684-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="75684-123">Wichtige und nützliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="75684-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="75684-124">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="75684-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="75684-125">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="75684-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="75684-126">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="75684-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="75684-127">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="75684-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="75684-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75684-128">See also</span></span>

- [<span data-ttu-id="75684-129">Programmieren mit der C-API in Excel</span><span class="sxs-lookup"><span data-stu-id="75684-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="75684-130">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="75684-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

