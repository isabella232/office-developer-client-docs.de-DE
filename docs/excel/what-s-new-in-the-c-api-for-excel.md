---
title: Was ist neu in der C-API für Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- C-api [excel 2007], was ist neu
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19790571"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="f13da-104">Was ist neu in der C-API für Excel</span><span class="sxs-lookup"><span data-stu-id="f13da-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="f13da-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f13da-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f13da-106">In Verbindung mit Microsoft Excel 2013 unterstützt der Microsoft Excel 2013 XLL Software Development Kit (SDK) für die folgenden Features.</span><span class="sxs-lookup"><span data-stu-id="f13da-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="f13da-107">**Neue Funktionen**</span><span class="sxs-lookup"><span data-stu-id="f13da-107">**New Functions**</span></span>
    
    <span data-ttu-id="f13da-108">Microsoft Excel 2013 XLL SDK unterstützt Rückrufen aller der neuer Excel-Arbeitsblattfunktionen in Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="f13da-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="f13da-109">Weitere Informationen zu Excel 2013-Funktionen aufrufen finden Sie unter [in Excel aus der DLL oder XLL aufgerufen](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="f13da-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="f13da-110">**Asynchrone benutzerdefinierte Funktionen**</span><span class="sxs-lookup"><span data-stu-id="f13da-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="f13da-111">Excel 2013 unterstützt das Aufrufen von benutzerdefinierten Funktionen (UDF) asynchron die kann die Leistung verbessern, indem mehrere Berechnungen zur selben Zeit ausführen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f13da-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="f13da-112">Weitere Informationen zu asynchronen UDFs finden Sie unter [Asynchronous User-Defined-Funktionen](asynchronous-user-defined-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f13da-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="f13da-113">**Clusterconnectoren**</span><span class="sxs-lookup"><span data-stu-id="f13da-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="f13da-114">Clusterconnectors Aktivieren von UDFs auf High Performance Computecluster ausführen.</span><span class="sxs-lookup"><span data-stu-id="f13da-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="f13da-115">Weitere Informationen zum Erstellen von clusterconnectoren finden Sie unter [Entwickeln von Excel-Clusterconnectoren](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="f13da-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f13da-116">XLL-add-ins, die Sie auf Computecluster ausführen möchten, müssen nur clustersichere Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f13da-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="f13da-117">Weitere Informationen zu den Funktionen, die Sie verwenden können, finden Sie unter [Excel XLL SDK-API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md) und [Clustersichere Funktionen](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f13da-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="f13da-118">**64-Bit-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="f13da-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="f13da-119">Sie können jetzt kompilieren und Verknüpfen von 32-Bit- und 64-Bit-XLLs.</span><span class="sxs-lookup"><span data-stu-id="f13da-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="f13da-120">Weitere Informationen finden Sie unter [Erstellen von XLLs](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="f13da-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f13da-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f13da-121">See also</span></span>



[<span data-ttu-id="f13da-122">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="f13da-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="f13da-123">Programmieren mit der C-API in Excel</span><span class="sxs-lookup"><span data-stu-id="f13da-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="f13da-124">Multithreading und Arbeitsspeicher Konflikte in Excel</span><span class="sxs-lookup"><span data-stu-id="f13da-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="f13da-125">Erste Schritte mit Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="f13da-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

