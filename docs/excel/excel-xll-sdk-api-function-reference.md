---
title: Excel XLL SDK – API-Funktionsreferenz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- API-Funktionsreferenz [Excel 2007],Funktionen [Excel 2007],Referenz [Excel 2007],Excel 2007 XLL Software Development Kit, Referenz
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790497"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="a5acd-104">Excel XLL SDK – API-Funktionsreferenz</span><span class="sxs-lookup"><span data-stu-id="a5acd-104">Excel 2013 XLL SDK API Function Reference</span></span>

<span data-ttu-id="a5acd-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5acd-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a5acd-106">Das Microsoft Excel 2013 XLL SDK enth�lt die Quelldateien für eine "Framework"-Bibliothek, die das Schreiben von XLLs beschleunigen soll, sowie die zwei Beispielprojekte "Example" und "Generic".</span><span class="sxs-lookup"><span data-stu-id="a5acd-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="a5acd-107">Dieser Abschnitt stellt eine Funktionsreferenz für Folgendes bereit:</span><span class="sxs-lookup"><span data-stu-id="a5acd-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="a5acd-108">Excel-Rückrufe, die die XLL aufrufen kann</span><span class="sxs-lookup"><span data-stu-id="a5acd-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="a5acd-109">XLL-Rückrufe, nach denen Microsoft Excel sucht</span><span class="sxs-lookup"><span data-stu-id="a5acd-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="a5acd-110">Wichtige Funktionen in den Beispiel- und Frameworkprojekten.</span><span class="sxs-lookup"><span data-stu-id="a5acd-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="a5acd-111">Beispielprojekte</span><span class="sxs-lookup"><span data-stu-id="a5acd-111">Sample Projects</span></span>

<span data-ttu-id="a5acd-112">Das Excel 2013 XLL SDK enthält Quelldateien und Microsoft Visual Studio Project-Dateien für die folgenden Beispielprojekte:</span><span class="sxs-lookup"><span data-stu-id="a5acd-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="a5acd-113">Das Projekt **Framework** (`SAMPLES\FRAMEWRK\`) enthält ein Projekt, aus dem die Bibliothek FRAMEWRK.lib erstellt werden kann, die dann mit anderen XLL-Projekten verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5acd-113">The **Framework** project (  `SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="a5acd-114">Die Bibliothek enthält viele Funktionen und Tools, die das Schreiben von XLLs einfacher machen.</span><span class="sxs-lookup"><span data-stu-id="a5acd-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="a5acd-115">Diese Bibliothek wird in den beiden anderen Projekten zusammen mit der Headerdatei FRAMEWRK.h verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5acd-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="a5acd-116">Das Projekt **Example** (`SAMPLES\EXAMPLE\`) enthält ein Projekt, aus dem die XLL-Datei EXAMPLE.xll erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5acd-116">The **Generic** project (  `SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="a5acd-117">Die XLL enthält viele Beispiele für die Verwendung der Bibliothek „Framework“ sowie Beispielimplementierungen der XLL-Add-In-Schnittstellenfunktionen wie z. B. **xlAutoOpen**.</span><span class="sxs-lookup"><span data-stu-id="a5acd-117">The Example project (SAMPLES\EXAMPLE\) contains a project that can be built to an XLL, EXAMPLE.xll. The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="a5acd-118">Das Projekt **Generic** (`SAMPLES\GENERIC\`) enthält ein Projekt, aus dem die XLL-Datei GENERIC.xll erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5acd-118">The **Generic** project (  `SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="a5acd-119">Die XLL veranschaulicht verschiedene Beispiele für Funktionen und Befehle und ist ein guter Ausgangspunkt zum Schreiben Ihrer eigenen XLLs.</span><span class="sxs-lookup"><span data-stu-id="a5acd-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="a5acd-120">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="a5acd-120">In this section</span></span>

- [<span data-ttu-id="a5acd-121">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="a5acd-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="a5acd-122">C-API-R�ckruf funktioniert Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="a5acd-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="a5acd-123">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a5acd-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="a5acd-124">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="a5acd-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="a5acd-125">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="a5acd-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="a5acd-126">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="a5acd-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="a5acd-127">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a5acd-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="a5acd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5acd-128">See also</span></span>

- [<span data-ttu-id="a5acd-129">Programmieren mit der C-API in Excel</span><span class="sxs-lookup"><span data-stu-id="a5acd-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="a5acd-130">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="a5acd-130">Developing Excel 2013 XLLs</span></span>](developing-excel-xlls.md)

