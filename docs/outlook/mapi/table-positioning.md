---
title: Tabellenpositionierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f7b2baa8cd78fbb8ace72fd0edb7c77f4c02a4c8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583862"
---
# <a name="table-positioning"></a><span data-ttu-id="6ca77-103">Tabellenpositionierung</span><span class="sxs-lookup"><span data-stu-id="6ca77-103">Table Positioning</span></span>

  
  
<span data-ttu-id="6ca77-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ca77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ca77-105">Die aktuelle Position in einer Tabelle wird immer durch einen Cursor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ca77-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="6ca77-106">Es ist ein Cursor für die einzelnen Ansichten einer Tabelle. der Wert wird von der Tabelle Implementierer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ca77-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="6ca77-107">Wenn ein Client oder Dienstanbieter mithilfe der Tabelle so ändern Sie die Position der Tabelle aufruft, wird der Wert des Cursors zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6ca77-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="6ca77-108">Position einer Tabelle kann mit geändert werden:</span><span class="sxs-lookup"><span data-stu-id="6ca77-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="6ca77-109">Textmarke.</span><span class="sxs-lookup"><span data-stu-id="6ca77-109">A bookmark.</span></span>
    
- <span data-ttu-id="6ca77-110">Ein Bruch-Wert.</span><span class="sxs-lookup"><span data-stu-id="6ca77-110">A fractional value.</span></span>
    
- <span data-ttu-id="6ca77-111">Ein Filter.</span><span class="sxs-lookup"><span data-stu-id="6ca77-111">A filter.</span></span>
    

