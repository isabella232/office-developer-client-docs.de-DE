---
title: SkipBlock streamstruktur-Datenstrom Struktur
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
# <a name="skipblock-stream-structure"></a><span data-ttu-id="13520-103">SkipBlock streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="13520-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="13520-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13520-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13520-105">Eine SkipBlock streamstruktur-Stream-Struktur ist ein Datenblock, der mit einer ganzen Zahl beginnt, die die Länge des verbleibenden Blocks angibt.</span><span class="sxs-lookup"><span data-stu-id="13520-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="13520-106">Diese Datenstrom Struktur ist in einem [FieldDefinition streamstruktur](fielddefinition-stream-structure.md) -Stream vorhanden, wenn die Felddefinition im PropDefV2-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="13520-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="13520-107">Der Zweck einer SkipBlock streamstruktur-Datenstrom Struktur hängt von der relativen Position in einer Reihe von like-Strukturen im SkipBlocks Data-Element eines FieldDefinition streamstruktur-Streams ab.</span><span class="sxs-lookup"><span data-stu-id="13520-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="13520-108">Die SkipBlocks-Reihe sollte mindestens eine SkipBlock streamstruktur-Struktur enthalten, die die Reihe beendet und das size-Datenelement gleich 0 aufweist.</span><span class="sxs-lookup"><span data-stu-id="13520-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="13520-109">Wenn die erste Struktur nicht die abschließende Struktur (das heißt, das size-Datenelement ist größer als 0) ist, wird davon ausgegangen, dass die erste Struktur den Feldnamen in Unicode (UTF-16) angibt.</span><span class="sxs-lookup"><span data-stu-id="13520-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="13520-110">Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar folgen einander in der angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="13520-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="13520-111">Größe: DWORD (4 Bytes), die Größe des Inhaltsdaten Elements in Byte.</span><span class="sxs-lookup"><span data-stu-id="13520-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="13520-112">Inhalt: ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="13520-112">Content: An array of BYTE.</span></span> <span data-ttu-id="13520-113">Die Anzahl dieses Arrays entspricht dem Size-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="13520-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="13520-114">Die Bedeutung des Inhaltsdaten Elements hängt vom Speicherort der SkipBlock streamstruktur-Struktur in der Reihe und der Version von Outlook ab.</span><span class="sxs-lookup"><span data-stu-id="13520-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="13520-115">Wenn die erste SkipBlock streamstruktur-Struktur nicht die abschließende Struktur ist, berücksichtigt Outlook die erste SkipBlock streamstruktur-Struktur als [firstskipblockcontent streamstruktur](firstskipblockcontent-stream-structure.md) -Datenstrom Struktur, die den Feldnamen in Unicode angibt.</span><span class="sxs-lookup"><span data-stu-id="13520-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="13520-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13520-116">See also</span></span>



[<span data-ttu-id="13520-117">Outlook-Elemente und-Felder</span><span class="sxs-lookup"><span data-stu-id="13520-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="13520-118">Stream-Strukturen</span><span class="sxs-lookup"><span data-stu-id="13520-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="13520-119">FieldDefinition streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="13520-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="13520-120">Firstskipblockcontent streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="13520-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

