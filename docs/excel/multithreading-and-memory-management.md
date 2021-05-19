---
title: Multithreading und Speicherverwaltung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414466"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="1041d-103">Multithreading und Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="1041d-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="1041d-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1041d-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1041d-105">Die ordnungsgemäße Behandlung des Arbeitsspeichers ist für die Erstellung zuverlässiger XLL-Add-Ins für die Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1041d-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="1041d-106">Wenn keine geeigneten Speicherpuffer zugewiesen und frei werden, wenn sie nicht mehr benötigt werden, wird die Leistung reduziert, Ressourcenstritte erstellt und Excel.</span><span class="sxs-lookup"><span data-stu-id="1041d-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="1041d-107">Ab Microsoft Office Excel 2007 können Sie Excel so konfigurieren, dass bei der Neuberechnung bis zu 1.024 gleichzeitige Threads verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1041d-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="1041d-108">In einigen Fällen, insbesondere wenn mehrere Prozessoren verfügbar sind oder benutzerdefinierte Funktionen auf Clusterservern ausgeführt werden, kann Multithreading die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="1041d-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="1041d-109">In den folgenden Themen wird das Verwalten von Arbeitsspeicher und Threads in XLLs beschrieben:</span><span class="sxs-lookup"><span data-stu-id="1041d-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="1041d-110">Speicherverwaltung in Excel</span><span class="sxs-lookup"><span data-stu-id="1041d-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="1041d-111">Multithreading und Speicherkonflikte in Excel</span><span class="sxs-lookup"><span data-stu-id="1041d-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="1041d-112">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="1041d-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="1041d-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1041d-113">See also</span></span>



[<span data-ttu-id="1041d-114">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="1041d-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

