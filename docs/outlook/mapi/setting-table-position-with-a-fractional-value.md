---
title: Festlegen der Tabellenposition mit einem Bruchwert
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8ffed8070c219e6611aebbcb1dd5cd181b662850
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579697"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="3937d-103">Festlegen der Tabellenposition mit einem Bruchwert</span><span class="sxs-lookup"><span data-stu-id="3937d-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="3937d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3937d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3937d-105">Tabelle Benutzer können auf eine Position verschieben, die einen ungefähren Prozentsatz der Zeilen in Bezug auf die Summe darstellt.</span><span class="sxs-lookup"><span data-stu-id="3937d-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="3937d-106">Statt auf eine genaue Zeile verschoben wurde, auf der Grundlage dieser Methode für die Positionierung teilt der Tabelle in Teile Brüche.</span><span class="sxs-lookup"><span data-stu-id="3937d-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="3937d-107">Benutzer können beispielsweise auf halb, zeigen Sie eine Tabelle oder in die Zeile, die die Art und Weise, durch die Tabelle die 7/8 ist verschieben.</span><span class="sxs-lookup"><span data-stu-id="3937d-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="3937d-108">**So verschieben Sie den Cursor eine ungefähre Anzahl der Zeilen**</span><span class="sxs-lookup"><span data-stu-id="3937d-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="3937d-109">Rufen Sie [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="3937d-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="3937d-110">**SeekRowApprox** verschiebt in die Zeile, die einen bestimmten Prozentsatz der Zeilen in Bezug auf den Anfang der Tabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="3937d-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="3937d-111">Dieser Prozentsatz ist in den _UlNumerator_ und _UlDenominator_ -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="3937d-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="3937d-112">**SeekRowApprox** wird häufig zum Implementieren von Bildlaufleisten verwendet.</span><span class="sxs-lookup"><span data-stu-id="3937d-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="3937d-113">**Um die ungefähre Position einer Tabelle bestimmen**</span><span class="sxs-lookup"><span data-stu-id="3937d-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="3937d-114">Rufen Sie [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="3937d-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="3937d-115">**QueryPosition** kann verwendet werden, um den Benutzer über die aktuelle Position zu informieren.</span><span class="sxs-lookup"><span data-stu-id="3937d-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="3937d-116">Einen Bruch Wert basierend auf der Anzahl der Zeilen in der Tabelle und die Anzahl der aktuellen Zeile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3937d-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="3937d-117">Davon ausgehen Sie, dass dieser Wert eine Annäherung darstellt.</span><span class="sxs-lookup"><span data-stu-id="3937d-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="3937d-118">Tabelle Implementierer sollten sich nicht um die genaue Position zu berechnen, da präzise Implementierungen aufzurufen, insbesondere für kategorisierten Tabellen kostspielig sein können.</span><span class="sxs-lookup"><span data-stu-id="3937d-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3937d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3937d-119">See also</span></span>



[<span data-ttu-id="3937d-120">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="3937d-120">MAPI Tables</span></span>](mapi-tables.md)

