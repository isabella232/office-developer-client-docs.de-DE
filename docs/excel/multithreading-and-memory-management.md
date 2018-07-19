---
title: Multithreading und Speicherverwaltung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790554"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="99e22-103">Multithreading und Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="99e22-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="99e22-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="99e22-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="99e22-105">Korrekte Handhabung von Arbeitsspeicher ist entscheidend für zuverlässige XLL-add-ins für Microsoft Excel erstellen.</span><span class="sxs-lookup"><span data-stu-id="99e22-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="99e22-106">Fehler beim Zuweisen der entsprechenden Speicherpuffern und diese frei, wenn sie nicht mehr benötigt werden reduziert die Leistung, Ressourcenkonflikte erstellt und Excel Dienstausfall.</span><span class="sxs-lookup"><span data-stu-id="99e22-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="99e22-107">Beginnen mit Microsoft Office Excel 2007, können Sie Excel, um bis zu 1.024 gleichzeitigen Threads verwenden, wenn Neuberechnen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="99e22-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="99e22-108">In einigen Fällen können insbesondere dann, wenn mehrere Prozessoren verfügbar sind oder mit benutzerdefinierten Funktionen unter Servercluster multithreading Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="99e22-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="99e22-109">In den folgenden Themen wird beschrieben, wie Arbeitsspeicher und Threads im XLLs verwalten:</span><span class="sxs-lookup"><span data-stu-id="99e22-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="99e22-110">Speicherverwaltung in Excel</span><span class="sxs-lookup"><span data-stu-id="99e22-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="99e22-111">Multithreading und Arbeitsspeicher Konflikte in Excel</span><span class="sxs-lookup"><span data-stu-id="99e22-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="99e22-112">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="99e22-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="99e22-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99e22-113">See also</span></span>



[<span data-ttu-id="99e22-114">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="99e22-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

