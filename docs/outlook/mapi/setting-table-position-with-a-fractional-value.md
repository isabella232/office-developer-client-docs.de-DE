---
title: Festlegen der Tabellen Position mit einem Bruchwert
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339263"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="12354-103">Festlegen der Tabellen Position mit einem Bruchwert</span><span class="sxs-lookup"><span data-stu-id="12354-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="12354-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12354-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12354-105">Tabellen Benutzer können zu einer Position verschoben werden, die einen ungefähren Prozentsatz der Zeilen im Verhältnis zur Gesamtsumme darstellt.</span><span class="sxs-lookup"><span data-stu-id="12354-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="12354-106">Anstatt zu einer exakten Zeile zu wechseln, wird die Tabelle durch diese Positionierungsmethode in Teile aufgeteilt, die auf Bruchteilen basieren.</span><span class="sxs-lookup"><span data-stu-id="12354-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="12354-107">Tabellen Benutzer können beispielsweise in den halben Punkt einer Tabelle oder in die Zeile, die sich in der Tabelle von 7/8 befindet, verschieben.</span><span class="sxs-lookup"><span data-stu-id="12354-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="12354-108">**So verschieben Sie den Cursor um eine ungefähre Anzahl von Zeilen**</span><span class="sxs-lookup"><span data-stu-id="12354-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="12354-109">Rufen Sie [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md)auf.</span><span class="sxs-lookup"><span data-stu-id="12354-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="12354-110">**SeekRowApprox** wechselt zu der Zeile, die einen bestimmten Prozentsatz von Zeilen relativ zum Anfang der Tabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="12354-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="12354-111">Dieser Prozentsatz wird in den Parametern _ulNumerator_ und _ulDenominator_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="12354-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="12354-112">**SeekRowApprox** wird häufig zum Implementieren von Bildlaufleisten verwendet.</span><span class="sxs-lookup"><span data-stu-id="12354-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="12354-113">**So bestimmen Sie die ungefähre Position einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="12354-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="12354-114">Rufen Sie [IMAPITable:: QueryPosition](imapitable-queryposition.md)auf.</span><span class="sxs-lookup"><span data-stu-id="12354-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="12354-115">**QueryPosition** kann verwendet werden, um den Benutzer über die aktuelle Position zu informieren.</span><span class="sxs-lookup"><span data-stu-id="12354-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="12354-116">Es wird ein Bruchwert basierend auf der Anzahl der Zeilen in der Tabelle und der Nummer der aktuellen Zeile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12354-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="12354-117">Erwarten Sie, dass dieser Wert eine Näherung darstellt.</span><span class="sxs-lookup"><span data-stu-id="12354-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="12354-118">Tabellen Implementierer werden dazu angehalten, die genaue Position nicht zu berechnen, da genaue Implementierungen vor allem bei kategorisierten Tabellen kostspielig sein können.</span><span class="sxs-lookup"><span data-stu-id="12354-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="12354-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12354-119">See also</span></span>



[<span data-ttu-id="12354-120">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="12354-120">MAPI Tables</span></span>](mapi-tables.md)

