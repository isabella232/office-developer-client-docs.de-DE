---
title: SkipBlock-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b7be498473ef86b11006702f85089f0f95bb2e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580901"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="b8b71-103">SkipBlock-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="b8b71-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="b8b71-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8b71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8b71-105">Eine SkipBlock Stream-Struktur ist ein Block von Daten, die mit einer ganzen Zahl beginnt, der die Länge des den verbleibenden Teil des Blocks angibt.</span><span class="sxs-lookup"><span data-stu-id="b8b71-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="b8b71-106">Diese Struktur Stream ist in einem Stream [FieldDefinition](fielddefinition-stream-structure.md) vorhanden, wenn die Felddefinition im PropDefV2-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="b8b71-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="b8b71-107">Der Zweck der eine SkipBlock Stream-Struktur hängt die relative Position in einer Reihe von wie Strukturen in der SkipBlocks Data-Element eines FieldDefinition Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b8b71-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="b8b71-108">Die Datenreihe SkipBlocks sollte mindestens eine SkipBlock Struktur enthalten, die beendet die Datenreihe und hat das Datenelement Größe gleich 0.</span><span class="sxs-lookup"><span data-stu-id="b8b71-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="b8b71-109">Wenn die erste Struktur nicht die abschließende Struktur ist (d. h., das Größe der Data-Element ist größer als 0), Outlook geht davon aus, die erste Struktur gibt der Name des Felds in Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="b8b71-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="b8b71-110">Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b8b71-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="b8b71-111">Größe: DWORD-Wert (4 Bytes), die Größe des Elements Inhaltsdaten als Byteanzahl angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8b71-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="b8b71-112">Inhalt: Ein Array von BYTE.</span><span class="sxs-lookup"><span data-stu-id="b8b71-112">Content: An array of BYTE.</span></span> <span data-ttu-id="b8b71-113">Die Anzahl der dieses Array ist gleich der Größe der Data-Element.</span><span class="sxs-lookup"><span data-stu-id="b8b71-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="b8b71-114">Die Bedeutung des Elements Inhaltsdaten hängt davon ab, den Speicherort der SkipBlock Struktur in der Datenreihe und die Version von Outlook.</span><span class="sxs-lookup"><span data-stu-id="b8b71-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="b8b71-115">Ist die erste SkipBlock-Struktur nicht den Abbruch Struktur, betrachtet Outlook die erste SkipBlock Struktur als der [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) Stream-Struktur, die in Unicode der Name des Felds angibt.</span><span class="sxs-lookup"><span data-stu-id="b8b71-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b8b71-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8b71-116">See also</span></span>



[<span data-ttu-id="b8b71-117">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="b8b71-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="b8b71-118">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="b8b71-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="b8b71-119">FieldDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="b8b71-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="b8b71-120">FirstSkipBlockContent-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="b8b71-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

