---
title: Neues in der C-API für Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], was neu ist
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439688"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="6fc69-104">Neues in der C-API für Excel</span><span class="sxs-lookup"><span data-stu-id="6fc69-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="6fc69-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6fc69-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6fc69-106">In Verbindung mit Microsoft Excel 2013 bietet das Microsoft Excel 2013 XLL Software Development Kit (SDK) Unterstützung für die folgenden Features.</span><span class="sxs-lookup"><span data-stu-id="6fc69-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="6fc69-107">**Neue Funktionen**</span><span class="sxs-lookup"><span data-stu-id="6fc69-107">**New Functions**</span></span>
    
    <span data-ttu-id="6fc69-108">Das Microsoft Excel 2013 XLL SDK unterstützt das Aufrufen aller neuen Arbeitsblattfunktionen in Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="6fc69-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="6fc69-109">Weitere Informationen zum Aufrufen Excel 2013-Funktionen finden Sie unter [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="6fc69-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="6fc69-110">**Asynchrone benutzerdefinierte Funktionen**</span><span class="sxs-lookup"><span data-stu-id="6fc69-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="6fc69-111">Excel 2013 unterstützt das asynchrone Aufrufen von benutzerdefinierten Funktionen (USERF), wodurch die Leistung verbessert werden kann, indem mehrere Berechnungen gleichzeitig ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="6fc69-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="6fc69-112">Weitere Informationen zu asynchronen UDFs finden Sie unter [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6fc69-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="6fc69-113">**Clusterconnectors**</span><span class="sxs-lookup"><span data-stu-id="6fc69-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="6fc69-114">Mit Clusterconnectors können UDFs auf Hochleistungs-Computeclustern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6fc69-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="6fc69-115">Weitere Informationen zum Erstellen von Clusterconnectors finden Sie unter [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="6fc69-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6fc69-116">XLL-Add-Ins, die Sie auf Computeclustern ausführen möchten, müssen nur clustersichere Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6fc69-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="6fc69-117">Weitere Informationen zu den Funktionen, die Sie verwenden können, finden Sie [unter Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) und Cluster Safe [Functions](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6fc69-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="6fc69-118">**64-Bit-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="6fc69-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="6fc69-119">Sie können jetzt sowohl 32-Bit- als auch 64-Bit-XLLs kompilieren und verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6fc69-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="6fc69-120">Weitere Informationen finden Sie unter [Creating XLLs](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="6fc69-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6fc69-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fc69-121">See also</span></span>



[<span data-ttu-id="6fc69-122">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="6fc69-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="6fc69-123">Programmieren mit der C-API in Excel</span><span class="sxs-lookup"><span data-stu-id="6fc69-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="6fc69-124">Multithreading und Speicherkonflikte in Excel</span><span class="sxs-lookup"><span data-stu-id="6fc69-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="6fc69-125">Erste Schritte mit dem Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="6fc69-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

