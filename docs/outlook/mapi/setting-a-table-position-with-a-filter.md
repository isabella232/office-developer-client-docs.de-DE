---
title: Festlegen einer Tabellen Position mit einem Filter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316044"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="0221f-103">Festlegen einer Tabellen Position mit einem Filter</span><span class="sxs-lookup"><span data-stu-id="0221f-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="0221f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0221f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0221f-105">Tabellen Benutzer können den Cursor in eine Zeile verschieben, die mit einem Satz von Filterkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0221f-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="0221f-106">Filter können auf einer Vielzahl von Richtlinien basieren, wie beispielsweise Spalten Eigenschaftswerte, Bitmasken oder unter Objekte.</span><span class="sxs-lookup"><span data-stu-id="0221f-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="0221f-107">Filter werden in MAPI mithilfe einer [SRestriction](srestriction.md) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="0221f-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="0221f-108">**So positionieren Sie eine Tabelle auf der ersten Zeile, die den Kriterien entspricht, die in einer Einschränkung festgelegt sind**</span><span class="sxs-lookup"><span data-stu-id="0221f-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="0221f-109">Rufen Sie die [IMAPITable:: FindRow](imapitable-findrow.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="0221f-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="0221f-110">Beginnend mit der Zeile, die durch eine bestimmte Textmarke dargestellt wird, sucht **FindRow** entweder nach vorn oder rückwärts, um eine Zeile zu suchen, die den in der Einschränkung angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="0221f-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="0221f-111">**FindRow** kann für die Implementierung einer Bildlaufleiste, die auf Zeichen Zeichenfolgen basiert, anstelle von Bruchwerten hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="0221f-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="0221f-112">Beispielsweise kann ein Client die MAPI-Implementierung von **FindRow** aufrufen, wenn er das integrierte Adressbuch durchsucht, um einen Benutzer durch Eingabe eines oder mehrerer Zeichen zu aktivieren, um den ersten Namen zu finden, der mit den angegebenen Zeichen beginnt.</span><span class="sxs-lookup"><span data-stu-id="0221f-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0221f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0221f-113">See also</span></span>



[<span data-ttu-id="0221f-114">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="0221f-114">MAPI Tables</span></span>](mapi-tables.md)

