---
title: PackedAnsiString-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5494558db65e19891848264c170ba85a55c5df71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793330"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="6fa5c-103">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="6fa5c-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="6fa5c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6fa5c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6fa5c-105">Die PackedAnsiString Stream-Datenstruktur enthält eine ANSI-Darstellung einer Zeichenfolge, die basierend auf der ANSI-Codeseite des Computers, auf dem Microsoft Outlook ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="6fa5c-106">Diese Zeichenfolge wird durch ein Null-Zeichen nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="6fa5c-107">Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der folgenden Reihenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="6fa5c-108">Die tatsächlichen Datenelemente, die vorhanden hängen die Länge der Zeichenfolge in ANSI-Darstellung.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="6fa5c-109">Nach einer Zeichenfolge, deren Darstellung ANSI höchstens 255 Bytes enthält, werden die Elemente wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6fa5c-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="6fa5c-110">Länge: BYTE (1 Byte), die Länge als Byteanzahl angegeben, der die ANSI-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="6fa5c-111">Zeichen: Ein Array von CHAR.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="6fa5c-112">Die Anzahl der dieses Array ist gleich der Länge Data-Element.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="6fa5c-113">Die Daten im Array ist die ANSI-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="6fa5c-114">Nach einer Zeichenfolge, deren Darstellung ANSI 255 und 65535 Bytes enthält, werden die Elemente wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6fa5c-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="6fa5c-115">Präfix: BYTE (1 Byte) der Wert der 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="6fa5c-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="6fa5c-116">Länge: Wort (2 Bytes), die Länge als Byteanzahl angegeben, der die ANSI-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="6fa5c-117">Zeichen: Ein Array von CHAR.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="6fa5c-118">Die Anzahl der dieses Array ist gleich der Länge Data-Element.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="6fa5c-119">Die Daten im Array ist die ANSI-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6fa5c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fa5c-120">See also</span></span>



[<span data-ttu-id="6fa5c-121">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="6fa5c-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="6fa5c-122">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="6fa5c-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="6fa5c-123">FieldDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="6fa5c-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

