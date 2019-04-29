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
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439912"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="fa93b-103">Verwenden einer Tabelle zum Arbeiten mit Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa93b-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="fa93b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa93b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa93b-105">Viele Eigenschaften sind sowohl von den Objekten, die Sie unterstützen, als auch von Spalten in Tabellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fa93b-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="fa93b-106">Rufen Sie diese Eigenschaften nach Möglichkeit über die Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="fa93b-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="fa93b-107">Rufen Sie [IMAPITable::](imapitable-setcolumns.md) SetColumns auf, um alle Eigenschaften einzuschließen, die der Client benötigt, und [IMAPITable:: QueryRows](imapitable-queryrows.md) , um alle Zeilen der Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fa93b-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="fa93b-108">Diese beiden Aufrufe sind in der Regel ausreichend, um genügend Informationen abzurufen, die für einen Benutzer angezeigt werden sollen, und Sie sind häufig für die erforderliche interne Verarbeitung \*\*\*\* ausreichend, wodurch ein Aufruf von OpenEntry zum Öffnen des Objekts erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fa93b-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="fa93b-109">Es gibt nur zwei Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="fa93b-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="fa93b-110">Wenn die Eigenschaft über 255 Byte ist.</span><span class="sxs-lookup"><span data-stu-id="fa93b-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="fa93b-111">Die \* \* IMAPITable \* \*-Schnittstelle gibt möglicherweise nicht den gesamten Eigenschaftswert zurück und schneidet Sie stattdessen mit 255 Byte ab.</span><span class="sxs-lookup"><span data-stu-id="fa93b-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="fa93b-112">Denken Sie jedoch an diesen Kompromiss.</span><span class="sxs-lookup"><span data-stu-id="fa93b-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="fa93b-113">Wenn Sie diese Daten dem Benutzer anzeigen, können 255 Byte für ein Textfeld wie einen Kommentar ausreichen.</span><span class="sxs-lookup"><span data-stu-id="fa93b-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="fa93b-114">Wenn Sie eine bestimmte Eigenschaft aus einer einzelnen Zeile in einer Tabelle benötigen.</span><span class="sxs-lookup"><span data-stu-id="fa93b-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="fa93b-115">In diesem Fall ist es nicht erforderlich, eine Tabelle mit Eigenschaften zu erstellen, die nie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa93b-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="fa93b-116">In den meisten Fällen benötigen Sie die gleichen Eigenschaften für alle Zeilen.</span><span class="sxs-lookup"><span data-stu-id="fa93b-116">Most of the time you will need the same properties for all rows.</span></span>
    

