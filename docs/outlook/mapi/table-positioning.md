---
title: Tabellen Positionierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 656f696c58e9b62e7e601d7f531870b8c385e862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345654"
---
# <a name="table-positioning"></a><span data-ttu-id="08e3d-103">Tabellen Positionierung</span><span class="sxs-lookup"><span data-stu-id="08e3d-103">Table Positioning</span></span>

  
  
<span data-ttu-id="08e3d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08e3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08e3d-105">Die aktuelle Position in einer Tabelle wird immer durch einen Cursor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08e3d-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="08e3d-106">Für jede Ansicht einer Tabelle gibt es einen Cursor. der Wert wird vom Implementierer der Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="08e3d-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="08e3d-107">Wenn ein Client oder ein Dienstanbieter, der die Tabelle verwendet, einen Aufruf zum Ändern der Position der Tabelle durchführt, wird der Wert des Cursors zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="08e3d-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="08e3d-108">Die Position einer Tabelle kann mit folgenden Änderungen geändert werden:</span><span class="sxs-lookup"><span data-stu-id="08e3d-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="08e3d-109">Textmarke.</span><span class="sxs-lookup"><span data-stu-id="08e3d-109">A bookmark.</span></span>
    
- <span data-ttu-id="08e3d-110">Ein Bruchteil.</span><span class="sxs-lookup"><span data-stu-id="08e3d-110">A fractional value.</span></span>
    
- <span data-ttu-id="08e3d-111">Ein Filter.</span><span class="sxs-lookup"><span data-stu-id="08e3d-111">A filter.</span></span>
    

