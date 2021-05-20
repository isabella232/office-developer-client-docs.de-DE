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
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437336"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="50ca0-103">Festlegen der Tabellenposition mit einem Bruchwert</span><span class="sxs-lookup"><span data-stu-id="50ca0-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="50ca0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50ca0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50ca0-105">Tabellenbenutzer können zu einer Position wechseln, die einen ungefähren Prozentsatz von Zeilen im Verhältnis zur Gesamtsumme darstellt.</span><span class="sxs-lookup"><span data-stu-id="50ca0-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="50ca0-106">Anstatt zu einer genauen Zeile zu verschieben, teilt diese Positionierungsmethode die Tabelle auf der Grundlage von Brüchen in Teile auf.</span><span class="sxs-lookup"><span data-stu-id="50ca0-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="50ca0-107">Tabellenbenutzer können z. B. zu einem Tabellenhalbpunkt oder zu der Zeile wechseln, die 7/8 des Wegs durch die Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="50ca0-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="50ca0-108">**So verschieben Sie den Cursor um eine ungefähre Anzahl von Zeilen**</span><span class="sxs-lookup"><span data-stu-id="50ca0-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="50ca0-109">Rufen [Sie IMAPITable::SeekRowApprox auf.](imapitable-seekrowapprox.md)</span><span class="sxs-lookup"><span data-stu-id="50ca0-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="50ca0-110">**SeekRowApprox** wechselt zu der Zeile, die einen bestimmten Prozentsatz von Zeilen im Verhältnis zum Anfang der Tabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="50ca0-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="50ca0-111">Dieser Prozentsatz wird in den  _Parametern ulNumerator_ und  _ulDenominator_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="50ca0-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="50ca0-112">**SeekRowApprox** wird häufig zum Implementieren von Bildlaufleisten verwendet.</span><span class="sxs-lookup"><span data-stu-id="50ca0-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="50ca0-113">**So bestimmen Sie die ungefähre Position einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="50ca0-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="50ca0-114">Rufen [Sie IMAPITable::QueryPosition auf.](imapitable-queryposition.md)</span><span class="sxs-lookup"><span data-stu-id="50ca0-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="50ca0-115">**QueryPosition** kann verwendet werden, um den Benutzer über die aktuelle Position zu informieren.</span><span class="sxs-lookup"><span data-stu-id="50ca0-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="50ca0-116">Sie legt einen Bruchwert fest, der auf der Anzahl der Zeilen in der Tabelle und der Anzahl der aktuellen Zeile basiert.</span><span class="sxs-lookup"><span data-stu-id="50ca0-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="50ca0-117">Gehen Sie davon aus, dass dieser Wert eine Näherung darstellt.</span><span class="sxs-lookup"><span data-stu-id="50ca0-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="50ca0-118">Table implementers are encouraged not calculate the exact position because accurate implementations can be expensive to invoke, especially on kategord tables.</span><span class="sxs-lookup"><span data-stu-id="50ca0-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="50ca0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50ca0-119">See also</span></span>



[<span data-ttu-id="50ca0-120">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="50ca0-120">MAPI Tables</span></span>](mapi-tables.md)

