---
title: Verwenden einer Tabelle zum Arbeiten mit Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795812"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="76476-103">Verwenden einer Tabelle zum Arbeiten mit Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76476-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="76476-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76476-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76476-105">Viele Eigenschaften sind sowohl auf die Objekte, die sie unterstützen und als Spalten in Tabellen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="76476-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="76476-106">Wenn möglich, rufen Sie diese Eigenschaften über die Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="76476-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="76476-107">Rufen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) alle Eigenschaften enthalten, die der Client muss und [IMAPITable::QueryRows](imapitable-queryrows.md) alle Zeilen der Tabelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="76476-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="76476-108">Diese beiden Aufrufe in der Regel ausreichend zum Abrufen von genügend Informationen, die ein Benutzer angezeigt werden und sind häufig ausreichend für alle erforderlichen interner Aufrufen **OpenEntry** zum Öffnen des Objekts nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="76476-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="76476-109">Es gibt nur zwei Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="76476-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="76476-110">Wenn die Eigenschaft mehr als 255 Byte ist.</span><span class="sxs-lookup"><span data-stu-id="76476-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="76476-111">Die ** IMAPITable ** Schnittstelle möglicherweise nicht zurück, die den gesamte Eigenschaftswert stattdessen auf 255 Byte abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="76476-111">The ** IMAPITable ** interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="76476-112">Überlegen Sie jedoch dieser Kompromiss.</span><span class="sxs-lookup"><span data-stu-id="76476-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="76476-113">Wenn Sie diese Daten an den Benutzer anzeigen, möglicherweise 255 Byte genug für eine textbezogene dar, wie ein Kommentar.</span><span class="sxs-lookup"><span data-stu-id="76476-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="76476-114">Wenn Sie eine bestimmte Eigenschaft aus einer einzelnen Zeile in einer Tabelle benötigen.</span><span class="sxs-lookup"><span data-stu-id="76476-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="76476-115">In diesem Fall ist es nicht erforderlich, eine Tabelle mit den Eigenschaften zu erstellen, die noch nie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76476-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="76476-116">In den meisten Fällen benötigen die gleichen Eigenschaften Sie für alle Zeilen.</span><span class="sxs-lookup"><span data-stu-id="76476-116">Most of the time you will need the same properties for all rows.</span></span>
    

