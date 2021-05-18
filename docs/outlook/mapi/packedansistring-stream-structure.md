---
title: PackedAnsiString-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404505"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="cbe1b-103">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="cbe1b-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="cbe1b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbe1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbe1b-105">Die Datenstromstruktur PackedAnsiString enthält eine ANSI-Darstellung einer Zeichenfolge basierend auf der ANSI-Codeseite des Computers, auf dem Microsoft Outlook ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="cbe1b-106">Diese Zeichenfolge wird nicht durch ein Nullzeichen beendet.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="cbe1b-107">Datenelemente in diesem Datenstrom werden in der Reihenfolge des Little-Endian-Bytes gespeichert und folgen in der unten aufgeführten Reihenfolge unmittelbar aufeinander.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="cbe1b-108">Die tatsächlich vorhandenen Datenelemente hängen von der Länge der Zeichenfolge in der ANSI-Darstellung ab.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="cbe1b-109">Für eine Zeichenfolge, deren ANSI-Darstellung weniger als 255 Byte enthält, sind die Datenelemente wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cbe1b-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="cbe1b-110">Length: BYTE (1 Byte), die Länge der ANSI-Darstellung der Zeichenfolge in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="cbe1b-111">Characters: Ein Array von CHAR.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="cbe1b-112">Die Anzahl dieses Arrays entspricht dem Length-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="cbe1b-113">Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="cbe1b-114">Für eine Zeichenfolge, deren ANSI-Darstellung 255 bis 65535 Byte enthält, sind die Datenelemente wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cbe1b-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="cbe1b-115">Präfix: BYTE (1 Byte), wert 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="cbe1b-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="cbe1b-116">Länge: WORD (2 Byte), die Länge der ANSI-Darstellung der Zeichenfolge in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="cbe1b-117">Characters: Ein Array von CHAR.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="cbe1b-118">Die Anzahl dieses Arrays entspricht dem Length-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="cbe1b-119">Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbe1b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbe1b-120">See also</span></span>



[<span data-ttu-id="cbe1b-121">Outlook Elemente und Felder</span><span class="sxs-lookup"><span data-stu-id="cbe1b-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="cbe1b-122">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="cbe1b-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="cbe1b-123">FieldDefinition Stream Structure</span><span class="sxs-lookup"><span data-stu-id="cbe1b-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

