---
title: SkipBlock Stream Structure
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435544"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="c1dd0-103">SkipBlock Stream Structure</span><span class="sxs-lookup"><span data-stu-id="c1dd0-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="c1dd0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1dd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1dd0-105">Eine SkipBlock-Streamstruktur ist ein Datenblock, der mit einer ganzen Zahl beginnt, die die Länge des verbleibenden Teils des Blocks angibt.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="c1dd0-106">Diese Datenstromstruktur ist in einem [FieldDefinition-Stream](fielddefinition-stream-structure.md) vorhanden, wenn die Felddefinition im PropDefV2-Format ist.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="c1dd0-107">Der Zweck einer SkipBlock-Streamstruktur hängt von ihrer relativen Position in einer Reihe von gleich großen Strukturen im SkipBlocks-Datenelement eines FieldDefinition-Datenstroms ab.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="c1dd0-108">Die SkipBlocks-Reihe sollte mindestens eine SkipBlock-Struktur enthalten, die die Datenreihe beendet und das Size-Datenelement gleich 0 hat.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="c1dd0-109">Wenn die erste Struktur nicht die Abschlussstruktur ist (d. h. das Size data-Element ist größer als 0), geht Outlook davon aus, dass die erste Struktur den Feldnamen in Unicode (UTF-16) angibt.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="c1dd0-110">Datenelemente in diesem Datenstrom werden in der Bytereihenfolge des Little-Endian-Elements gespeichert und folgen sofort in der unten angegebenen Reihenfolge aufeinander.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="c1dd0-111">Größe: DWORD (4 Byte), die Größe des Content-Datenelements in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="c1dd0-112">Inhalt: Ein Array von BYTE.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-112">Content: An array of BYTE.</span></span> <span data-ttu-id="c1dd0-113">Die Anzahl dieses Arrays entspricht dem Size-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="c1dd0-114">Die Bedeutung des Inhaltsdatenelements hängt vom Speicherort der SkipBlock-Struktur in der Datenreihe und der Version des Outlook.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="c1dd0-115">Wenn die erste SkipBlock-Struktur nicht die Abschlussstruktur ist, betrachtet Outlook die erste SkipBlock-Struktur als [FirstSkipBlockContent-Streamstruktur,](firstskipblockcontent-stream-structure.md) die den Feldnamen in Unicode angibt.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c1dd0-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1dd0-116">See also</span></span>



[<span data-ttu-id="c1dd0-117">Outlook Elemente und Felder</span><span class="sxs-lookup"><span data-stu-id="c1dd0-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="c1dd0-118">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="c1dd0-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="c1dd0-119">FieldDefinition Stream Structure</span><span class="sxs-lookup"><span data-stu-id="c1dd0-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="c1dd0-120">FirstSkipBlockContent Stream Structure</span><span class="sxs-lookup"><span data-stu-id="c1dd0-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

