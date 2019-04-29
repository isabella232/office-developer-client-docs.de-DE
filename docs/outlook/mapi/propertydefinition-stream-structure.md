---
title: PropertyDefinition-Datenstrom Struktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438589"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="8135b-103">PropertyDefinition-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="8135b-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="8135b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8135b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8135b-105">Eine PropertyDefinition-Datenstrom Struktur ist ein Array von [FieldDefinition streamstruktur](fielddefinition-stream-structure.md) -Datenstrom Strukturen, die Definitionen für alle benutzerdefinierten Felder in einem Microsoft Outlook-Element enthalten, sowie Datenbindungseinstellungen für einige integrierte Felder.</span><span class="sxs-lookup"><span data-stu-id="8135b-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="8135b-106">Sie können die PropertyDefinition-Datenstrom Strukturprogramm gesteuert bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8135b-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="8135b-107">Sie können jedoch ähnliche Ergebnisse erzielen, indem Sie den Outlook-Formular-Designer und insbesondere das Dialogfeld **Eigenschaften** für ein datengebundenes Steuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="8135b-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="8135b-108">Felddefinitionen in einer PropertyDefinition-Datenstrom Struktur können eines von zwei Formaten sein: PropDefV1 und PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="8135b-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="8135b-109">Outlook unterstützt sowohl PropDefV1 als auch PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="8135b-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="8135b-110">Alle Felddefinitionen in einer einzelnen PropertyDefinition-Datenstrom Struktur müssen das gleiche Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8135b-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="8135b-111">Weitere Informationen dazu, wie PropDefV1 und PropDefV2 unterschiedlich sind, finden Sie unter [FieldDefinition streamstruktur](fielddefinition-stream-structure.md)-streamstruktur.</span><span class="sxs-lookup"><span data-stu-id="8135b-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="8135b-112">Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar folgen einander in der angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="8135b-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="8135b-113">Version: WORD (2 Bytes), das Format der Felddefinitionen in der PropertyDefinition-Datenstrom Struktur.</span><span class="sxs-lookup"><span data-stu-id="8135b-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="8135b-114">In der folgenden Tabelle sind die möglichen Werte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8135b-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="8135b-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8135b-115">**Value**</span></span>|<span data-ttu-id="8135b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8135b-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="8135b-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="8135b-117">0x0102</span></span>  <br/> |<span data-ttu-id="8135b-118">Format ist PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="8135b-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="8135b-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="8135b-119">0x0103</span></span>  <br/> |<span data-ttu-id="8135b-120">Format ist PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="8135b-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="8135b-121">FieldDefinitionCount: DWORD (4 Bytes), die Anzahl der Felddefinitionen in diesem Stream.</span><span class="sxs-lookup"><span data-stu-id="8135b-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="8135b-122">Dies ist die Anzahl von Array-Elementen im FieldDefinitions-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="8135b-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="8135b-123">FieldDefinitions: ein Array von FieldDefinition streamstruktur-Stream-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="8135b-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="8135b-124">Die Anzahl dieses Arrays ist gleich dem FieldDefinitionCount-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="8135b-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8135b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8135b-125">See also</span></span>

- [<span data-ttu-id="8135b-126">Outlook-Elemente und-Felder</span><span class="sxs-lookup"><span data-stu-id="8135b-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="8135b-127">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="8135b-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="8135b-128">PropertyDefinition-Stream-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8135b-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="8135b-129">Stream-Strukturen</span><span class="sxs-lookup"><span data-stu-id="8135b-129">Stream Structures</span></span>](stream-structures.md)

