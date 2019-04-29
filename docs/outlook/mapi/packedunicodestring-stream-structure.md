---
title: Packedunicodestring streamstruktur-Datenstrom Struktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422614"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="d25d4-103">Packedunicodestring streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="d25d4-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="d25d4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d25d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d25d4-105">Die Packedunicodestring streamstruktur-Datenstrom Struktur enthält eine Unicode-Darstellung (UTF-16) einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d25d4-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="d25d4-106">Diese Zeichenfolge wird nicht durch ein NULL-Zeichen beendet.</span><span class="sxs-lookup"><span data-stu-id="d25d4-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="d25d4-107">Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der unten aufgeführten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d25d4-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="d25d4-108">Die vorhandenen Datenelemente hängen von der Länge der Zeichenfolge in der UTF-16-Darstellung ab.</span><span class="sxs-lookup"><span data-stu-id="d25d4-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="d25d4-109">Für eine Zeichenfolge, deren UTF-16-Darstellung kleiner als 255 WCHARs, sind die folgenden Datenelemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="d25d4-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="d25d4-110">Length: BYTE (1 Byte), die Länge in der Anzahl von WCHARs, der UTF-16-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d25d4-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="d25d4-111">Characters: ein Array von Typ WCHAR.</span><span class="sxs-lookup"><span data-stu-id="d25d4-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="d25d4-112">Die Anzahl dieses Arrays ist gleich dem length-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="d25d4-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="d25d4-113">Die Daten im Array sind die UTF-16-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d25d4-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="d25d4-114">Für eine Zeichenfolge, deren UTF-16-Darstellung 255 bis 65535 WCHARs enthält, lauten die folgenden Datenelemente:</span><span class="sxs-lookup"><span data-stu-id="d25d4-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="d25d4-115">Prefix: BYTE (1 Byte), der Wert von 255 (0xFF).</span><span class="sxs-lookup"><span data-stu-id="d25d4-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="d25d4-116">Length: WORD (2 Bytes), die Länge (in WCHARs) der UTF-16-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d25d4-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="d25d4-117">Characters: ein Array von Typ WCHAR.</span><span class="sxs-lookup"><span data-stu-id="d25d4-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="d25d4-118">Die Anzahl dieses Arrays ist gleich dem length-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="d25d4-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="d25d4-119">Die Daten im Array sind die UTF-16-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d25d4-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d25d4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d25d4-120">See also</span></span>



[<span data-ttu-id="d25d4-121">Outlook-Elemente und-Felder</span><span class="sxs-lookup"><span data-stu-id="d25d4-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="d25d4-122">Stream-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d25d4-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="d25d4-123">FieldDefinition streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="d25d4-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

