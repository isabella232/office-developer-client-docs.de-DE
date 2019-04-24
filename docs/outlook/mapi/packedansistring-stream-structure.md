---
title: Packedansistring streamstruktur-Datenstrom Struktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348510"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="ce474-103">Packedansistring streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="ce474-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="ce474-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce474-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce474-105">Die Packedansistring streamstruktur-Datenstrom Struktur enthält eine ANSI-Darstellung einer Zeichenfolge, die auf der ANSI-Codeseite des Computers basiert, auf dem Microsoft Outlook läuft.</span><span class="sxs-lookup"><span data-stu-id="ce474-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="ce474-106">Diese Zeichenfolge wird nicht durch ein NULL-Zeichen beendet.</span><span class="sxs-lookup"><span data-stu-id="ce474-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="ce474-107">Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der unten aufgeführten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ce474-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="ce474-108">Die tatsächlichen Datenelemente, die vorhanden sind, hängen von der Länge der Zeichenfolge in der ANSI-Darstellung ab.</span><span class="sxs-lookup"><span data-stu-id="ce474-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="ce474-109">Bei einer Zeichenfolge, deren ANSI-Darstellung kleiner als 255 Byte ist, sind die folgenden Datenelemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="ce474-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="ce474-110">Length: BYTE (1 Byte), die Länge der ANSI-Darstellung der Zeichenfolge in Byte.</span><span class="sxs-lookup"><span data-stu-id="ce474-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="ce474-111">Characters: ein Array von CHAR.</span><span class="sxs-lookup"><span data-stu-id="ce474-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="ce474-112">Die Anzahl dieses Arrays ist gleich dem length-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="ce474-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="ce474-113">Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ce474-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="ce474-114">Für eine Zeichenfolge, deren ANSI-Darstellung 255 bis 65535 Byte enthält, lauten die folgenden Datenelemente:</span><span class="sxs-lookup"><span data-stu-id="ce474-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="ce474-115">Prefix: BYTE (1 Byte), der Wert von 255 (0xFF).</span><span class="sxs-lookup"><span data-stu-id="ce474-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="ce474-116">Length: WORD (2 Bytes), die Länge der ANSI-Darstellung der Zeichenfolge in Byte.</span><span class="sxs-lookup"><span data-stu-id="ce474-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="ce474-117">Characters: ein Array von CHAR.</span><span class="sxs-lookup"><span data-stu-id="ce474-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="ce474-118">Die Anzahl dieses Arrays ist gleich dem length-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="ce474-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="ce474-119">Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ce474-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce474-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce474-120">See also</span></span>



[<span data-ttu-id="ce474-121">Outlook-Elemente und-Felder</span><span class="sxs-lookup"><span data-stu-id="ce474-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="ce474-122">Stream-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ce474-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="ce474-123">FieldDefinition streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="ce474-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

