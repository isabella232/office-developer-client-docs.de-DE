---
title: PackedUnicodeString-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b4dcdcb50fb04410ed93940b46ea7a0d74fff41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793333"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="311e3-103">PackedUnicodeString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="311e3-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="311e3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="311e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="311e3-105">Die PackedUnicodeString Stream-Datenstruktur enthält eine Unicode (UTF-16) Darstellung einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="311e3-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="311e3-106">Diese Zeichenfolge wird durch ein Null-Zeichen nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="311e3-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="311e3-107">Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der folgenden Reihenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="311e3-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="311e3-108">Die tatsächlichen Datenelemente, die vorhanden hängen die Länge der Zeichenfolge in UTF-16 Darstellung.</span><span class="sxs-lookup"><span data-stu-id="311e3-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="311e3-109">Nach einer Zeichenfolge, deren Darstellung UTF-16 weniger als 255 WCHARs so lang wie enthält, werden die Elemente wie folgt:</span><span class="sxs-lookup"><span data-stu-id="311e3-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="311e3-110">Länge: BYTE (1 Byte), die Länge in WCHARs so lang wie, Anzahl der UTF-16 Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="311e3-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="311e3-111">Zeichen: Ein Array von WCHAR.</span><span class="sxs-lookup"><span data-stu-id="311e3-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="311e3-112">Die Anzahl der dieses Array ist gleich der Länge Data-Element.</span><span class="sxs-lookup"><span data-stu-id="311e3-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="311e3-113">Die Daten im Array ist die UTF-16-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="311e3-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="311e3-114">Nach einer Zeichenfolge, deren Darstellung UTF-16 255 und 65535 WCHARs so lang wie enthält, werden die Elemente wie folgt:</span><span class="sxs-lookup"><span data-stu-id="311e3-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="311e3-115">Präfix: BYTE (1 Byte) der Wert der 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="311e3-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="311e3-116">Länge: Wort (2 Bytes), die Länge in WCHARs so lang wie, Anzahl der UTF-16 Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="311e3-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="311e3-117">Zeichen: Ein Array von WCHAR.</span><span class="sxs-lookup"><span data-stu-id="311e3-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="311e3-118">Die Anzahl der dieses Array ist gleich der Länge Data-Element.</span><span class="sxs-lookup"><span data-stu-id="311e3-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="311e3-119">Die Daten im Array ist die UTF-16-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="311e3-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="311e3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="311e3-120">See also</span></span>



[<span data-ttu-id="311e3-121">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="311e3-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="311e3-122">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="311e3-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="311e3-123">FieldDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="311e3-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

