---
title: Arbeiten mit großen Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420423"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="adbc7-103">Arbeiten mit großen Spalten</span><span class="sxs-lookup"><span data-stu-id="adbc7-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="adbc7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adbc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adbc7-105">Spalten mit Zeichenfolgen- oder binären Eigenschaftsdaten können groß sein, möglicherweise viele Tausend Byte lang.</span><span class="sxs-lookup"><span data-stu-id="adbc7-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="adbc7-106">Da das Hinzufügen einer oder mehreren Spalten mit Hunderten von Bytes in einer Ansicht häufig nicht praktikabel ist, ermöglicht MAPI Tabellen implementierern, den Wert zu kürzen, meist auf 255 Byte und seltener auf 510 Byte.</span><span class="sxs-lookup"><span data-stu-id="adbc7-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="adbc7-107">Nach Möglichkeit sollten Tabellen implementierer den vollständigen Wert einer Eigenschaft in einer Tabellenspalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="adbc7-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="adbc7-108">Die empfohlene Alternative ist, nur die ersten 255 Byte zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="adbc7-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="adbc7-109">Clients können nicht im Voraus wissen, ob eine tabelle, die sie verwenden, große Spalten abkürzt.</span><span class="sxs-lookup"><span data-stu-id="adbc7-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="adbc7-110">Sie sollten davon ausgehen, dass eine Spalte eine abgeschnittene Eigenschaft darstellt, wenn die Länge der Spalte entweder 255 oder 510 Byte beträgt.</span><span class="sxs-lookup"><span data-stu-id="adbc7-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="adbc7-111">Bei Bedarf können Clients den vollständigen Wert einer abgeschnittenen Spalte direkt aus dem Objekt abrufen, indem sie die [IMAPIProp::GetProps-Methode des](imapiprop-getprops.md) Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="adbc7-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="adbc7-112">Clients, die Einschränkungen mit großen Eigenschaften erstellen, sollten beachten, dass es dem Tabellen implementier ob liegt, wie diese Einschränkungen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="adbc7-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="adbc7-113">Einige Tabellen implementierer ermöglichen, dass Einschränkungen, die mit einer abgeschnittenen Spalte erstellt werden, auf der abgeschnittenen Größe basieren, während andere sie auf dem gesamten Wert basieren.</span><span class="sxs-lookup"><span data-stu-id="adbc7-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="adbc7-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adbc7-114">See also</span></span>



[<span data-ttu-id="adbc7-115">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="adbc7-115">MAPI Tables</span></span>](mapi-tables.md)

