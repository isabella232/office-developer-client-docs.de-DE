---
title: PropertyDefinition Stream-Struktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 289227ee171c2325cad0ed321dab4f635a0ca724
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795336"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="ef598-103">PropertyDefinition Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="ef598-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="ef598-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef598-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef598-105">Eine PropertyDefinition Stream-Struktur ist ein Array von [FieldDefinition](fielddefinition-stream-structure.md) Stream Strukturen, die Definitionen für alle benutzerdefinierten Felder in einem Microsoft Outlook-Element und Datenbindung Einstellungen für einige integrierte Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef598-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="ef598-106">Sie können die PropertyDefinition Stream Struktur programmgesteuert bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ef598-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="ef598-107">Jedoch können Sie ähnliche Ergebnisse erzielen, mithilfe des Outlook-Formular-Designers und insbesondere das Dialogfeld **Eigenschaften** für ein datengebundenes Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ef598-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="ef598-108">Felddefinitionen in einer PropertyDefinition Stream-Struktur kann eine der folgenden beiden Formate: PropDefV1 und PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="ef598-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="ef598-109">Outlook unterstützt PropDefV1 und PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="ef598-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="ef598-110">Alle Felddefinitionen in einer einzelnen PropertyDefinition Stream Struktur müssen das gleiche Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ef598-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="ef598-111">Weitere Informationen dazu, wie PropDefV1 und PropDefV2 unterscheiden finden Sie unter [FieldDefinition Stream Struktur](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="ef598-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="ef598-112">Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef598-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="ef598-113">Version: WORD (2 Bytes), das Format der Felddefinitionen in der PropertyDefinition stream Struktur.</span><span class="sxs-lookup"><span data-stu-id="ef598-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="ef598-114">In der folgenden Tabelle sind die möglichen Werte.</span><span class="sxs-lookup"><span data-stu-id="ef598-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="ef598-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ef598-115">**Value**</span></span>|<span data-ttu-id="ef598-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef598-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="ef598-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="ef598-117">0x0102</span></span>  <br/> |<span data-ttu-id="ef598-118">PropDefV1-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ef598-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="ef598-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="ef598-119">0x0103</span></span>  <br/> |<span data-ttu-id="ef598-120">PropDefV2-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ef598-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="ef598-121">FieldDefinitionCount: DWORD-Wert (4 Bytes), die Anzahl der Felddefinitionen in diesen Stream.</span><span class="sxs-lookup"><span data-stu-id="ef598-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="ef598-122">Dies ist die Anzahl der Elemente in der FieldDefinitions Data-Element.</span><span class="sxs-lookup"><span data-stu-id="ef598-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="ef598-123">FieldDefinitions: Ein Array von FieldDefinition Stream Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ef598-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="ef598-124">Die Anzahl der dieses Array ist gleich der FieldDefinitionCount Data-Element.</span><span class="sxs-lookup"><span data-stu-id="ef598-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef598-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef598-125">See also</span></span>

- [<span data-ttu-id="ef598-126">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="ef598-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="ef598-127">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="ef598-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="ef598-128">Beispiel für PropertyDefinition-Stream</span><span class="sxs-lookup"><span data-stu-id="ef598-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="ef598-129">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="ef598-129">Stream Structures</span></span>](stream-structures.md)

