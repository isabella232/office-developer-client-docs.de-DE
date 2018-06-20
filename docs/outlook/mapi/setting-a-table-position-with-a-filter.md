---
title: Wenn Sie eine Tabelle Position mit einem Filter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4c3a5c13433fb2f037be24ddd4c877579429f7bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795515"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="53e5a-103">Wenn Sie eine Tabelle Position mit einem Filter</span><span class="sxs-lookup"><span data-stu-id="53e5a-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="53e5a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53e5a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53e5a-105">Tabelle Benutzer können den Cursor an eine Zeile setzen, die einen Satz von Filterkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="53e5a-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="53e5a-106">Filter können verschiedene Richtlinien wie Spaltenwerte-Eigenschaft, Bitmasken oder Unterobjekte basieren.</span><span class="sxs-lookup"><span data-stu-id="53e5a-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="53e5a-107">Filter werden in MAPI mithilfe der Struktur einer [SRestriction](srestriction.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="53e5a-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="53e5a-108">**Positionieren Sie auf die erste Zeile eine Tabelle, die in einer Einschränkung festgelegten Kriterien entspricht**</span><span class="sxs-lookup"><span data-stu-id="53e5a-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="53e5a-109">Rufen Sie die [IMAPITable](imapitable-findrow.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="53e5a-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="53e5a-110">Beginnend mit der Zeile, die durch eine bestimmte Textmarke dargestellt, sucht **FindRow** ein vorwärts oder rückwärts ausgeführt, eine Zeile zu finden, die die in der Einschränkung angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="53e5a-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="53e5a-111">**FindRow** ist hilfreich für die Implementierung von einer Bildlaufleiste angezeigt, die auf Zeichenfolgen anstelle von Bruchzahlen basiert.</span><span class="sxs-lookup"><span data-stu-id="53e5a-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="53e5a-112">Beispielsweise kann ein Client des MAPI-Implementierung der **FindRow** aufrufen, bei der Suche über die integrierte-Adressbuch zum Aktivieren eines Benutzers, durch Eingabe von einem oder mehreren Zeichen, um den ersten Namen zu suchen, der mit der angegebenen Zeichen beginnt.</span><span class="sxs-lookup"><span data-stu-id="53e5a-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="53e5a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53e5a-113">See also</span></span>



[<span data-ttu-id="53e5a-114">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="53e5a-114">MAPI Tables</span></span>](mapi-tables.md)

