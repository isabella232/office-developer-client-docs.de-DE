---
title: Festlegen einer Tabellenposition mit einem Filter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565592"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="3c249-103">Festlegen einer Tabellenposition mit einem Filter</span><span class="sxs-lookup"><span data-stu-id="3c249-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="3c249-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c249-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c249-105">Tabelle Benutzer können den Cursor an eine Zeile setzen, die einen Satz von Filterkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3c249-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="3c249-106">Filter können verschiedene Richtlinien wie Spaltenwerte-Eigenschaft, Bitmasken oder Unterobjekte basieren.</span><span class="sxs-lookup"><span data-stu-id="3c249-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="3c249-107">Filter werden in MAPI mithilfe der Struktur einer [SRestriction](srestriction.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="3c249-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="3c249-108">**Positionieren Sie auf die erste Zeile eine Tabelle, die in einer Einschränkung festgelegten Kriterien entspricht**</span><span class="sxs-lookup"><span data-stu-id="3c249-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="3c249-109">Rufen Sie die [IMAPITable](imapitable-findrow.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3c249-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="3c249-110">Beginnend mit der Zeile, die durch eine bestimmte Textmarke dargestellt, sucht **FindRow** ein vorwärts oder rückwärts ausgeführt, eine Zeile zu finden, die die in der Einschränkung angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="3c249-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="3c249-111">**FindRow** ist hilfreich für die Implementierung von einer Bildlaufleiste angezeigt, die auf Zeichenfolgen anstelle von Bruchzahlen basiert.</span><span class="sxs-lookup"><span data-stu-id="3c249-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="3c249-112">Beispielsweise kann ein Client des MAPI-Implementierung der **FindRow** aufrufen, bei der Suche über die integrierte-Adressbuch zum Aktivieren eines Benutzers, durch Eingabe von einem oder mehreren Zeichen, um den ersten Namen zu suchen, der mit der angegebenen Zeichen beginnt.</span><span class="sxs-lookup"><span data-stu-id="3c249-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3c249-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c249-113">See also</span></span>



[<span data-ttu-id="3c249-114">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="3c249-114">MAPI Tables</span></span>](mapi-tables.md)

