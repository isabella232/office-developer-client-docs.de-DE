---
title: Arbeiten mit umfangreichen Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a191a8551d425d7e8b3b9a281936a4a0e2dfd587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795843"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="a6d8e-103">Arbeiten mit umfangreichen Spalten</span><span class="sxs-lookup"><span data-stu-id="a6d8e-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="a6d8e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6d8e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6d8e-105">Spalten mit Zeichenfolgen oder binäre Eigenschaftendaten können sehr groß sein, möglicherweise Tausende von Byte.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="a6d8e-106">Da eine oder mehrere Spalten mit Hunderten von Bytes in einer Ansicht einschließlich häufig nicht sinnvoll ist, kann MAPI Implementierer Tabelle, um den Wert, der am häufigsten auf 255 Byte und seltener 510 Byte abzuschneiden.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="a6d8e-107">Wenn möglich, sollte die Tabelle Implementierer den vollständigen Wert einer Eigenschaft in einer Tabellenspalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="a6d8e-108">Es wird empfohlen, stattdessen nur die ersten 255 Byte enthalten.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="a6d8e-109">Clients können nicht im Voraus wissen, ob eine Tabelle verwendeten schneidet große Spalten ab.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="a6d8e-110">Sie sollten davon ausgehen, dass eine Spalte eine abgeschnittene Eigenschaft darstellt, wenn die Länge der Spalte 510 maximal 255 Bytes ist.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="a6d8e-111">Bei Bedarf können Clients direkt den vollständigen Wert einer abgeschnittene Spalte aus dem Objekt abrufen, indem das Objekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="a6d8e-112">Erstellen von Einschränkungen mit großen Eigenschaften Clients Beachten Sie, dass es bis zu der Tabelle Implementierer ist, wie diese Einschränkungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="a6d8e-113">Einige Implementierer Tabelle zulassen Einschränkungen, die erstellt werden, mit der abgeschnittene Spalte auf die abgeschnittene Größe basieren, während andere Benutzer auf den gesamten Wert basieren soll.</span><span class="sxs-lookup"><span data-stu-id="a6d8e-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6d8e-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6d8e-114">See also</span></span>



[<span data-ttu-id="a6d8e-115">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="a6d8e-115">MAPI Tables</span></span>](mapi-tables.md)

