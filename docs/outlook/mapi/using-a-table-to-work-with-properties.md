---
title: Verwenden einer Tabelle zum Arbeiten mit Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f02da9eb1920f55acf65dfb6a503e42d4c3daf2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585423"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="f035a-103">Verwenden einer Tabelle zum Arbeiten mit Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f035a-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="f035a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f035a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f035a-105">Viele Eigenschaften sind sowohl auf die Objekte, die sie unterstützen und als Spalten in Tabellen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f035a-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="f035a-106">Wenn möglich, rufen Sie diese Eigenschaften über die Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="f035a-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="f035a-107">Rufen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) alle Eigenschaften enthalten, die der Client muss und [IMAPITable::QueryRows](imapitable-queryrows.md) alle Zeilen der Tabelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="f035a-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="f035a-108">Diese beiden Aufrufe in der Regel ausreichend zum Abrufen von genügend Informationen, die ein Benutzer angezeigt werden und sind häufig ausreichend für alle erforderlichen interner Aufrufen **OpenEntry** zum Öffnen des Objekts nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f035a-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="f035a-109">Es gibt nur zwei Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="f035a-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="f035a-110">Wenn die Eigenschaft mehr als 255 Byte ist.</span><span class="sxs-lookup"><span data-stu-id="f035a-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="f035a-111">Die ** IMAPITable ** Schnittstelle möglicherweise nicht zurück, die den gesamte Eigenschaftswert stattdessen auf 255 Byte abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="f035a-111">The ** IMAPITable ** interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="f035a-112">Überlegen Sie jedoch dieser Kompromiss.</span><span class="sxs-lookup"><span data-stu-id="f035a-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="f035a-113">Wenn Sie diese Daten an den Benutzer anzeigen, möglicherweise 255 Byte genug für eine textbezogene dar, wie ein Kommentar.</span><span class="sxs-lookup"><span data-stu-id="f035a-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="f035a-114">Wenn Sie eine bestimmte Eigenschaft aus einer einzelnen Zeile in einer Tabelle benötigen.</span><span class="sxs-lookup"><span data-stu-id="f035a-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="f035a-115">In diesem Fall ist es nicht erforderlich, eine Tabelle mit den Eigenschaften zu erstellen, die noch nie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f035a-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="f035a-116">In den meisten Fällen benötigen die gleichen Eigenschaften Sie für alle Zeilen.</span><span class="sxs-lookup"><span data-stu-id="f035a-116">Most of the time you will need the same properties for all rows.</span></span>
    

