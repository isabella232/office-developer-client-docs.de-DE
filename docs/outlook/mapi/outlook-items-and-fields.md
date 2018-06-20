---
title: Outlook-Elemente und Felder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 71c67c37cc4f9cd3ddd7a55c37c4ebd6ddd35cfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793329"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="2e2e1-103">Outlook-Elemente und Felder</span><span class="sxs-lookup"><span data-stu-id="2e2e1-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="2e2e1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e2e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e2e1-105">Microsoft Outlook bietet Elementtypen, die speziell auf ihre Funktionalität (beispielsweise e-Mail-Elementen, Termine, Kontakte, Aufgaben und Notizen) sind.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="2e2e1-106">Outlook bietet Standardfelder für jede Art von Element als integrierte Felder bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="2e2e1-107">Outlook kann der Benutzer zum Erstellen von benutzerdefinierter Feldern, als benutzerdefinierte Felder bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="2e2e1-108">Jedes Feld ist einen Datentyp und einen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="2e2e1-109">Beispiele für Datentypen sind **Währung**, **Datum/Uhrzeit**, **Dauer**, **ganze Zahl**, **Schlüsselwörter**und **Text**.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="2e2e1-110">Benutzer können benutzerdefinierte Felder im Formular-Designer in Outlook mit definieren.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="2e2e1-111">Auf Ebene der Programmierbarkeit wird jedes Element durch ein [IMessage](imessageimapiprop.md) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="2e2e1-112">Jedes benutzerdefinierte Feld ist eine Definition für ein Feld und einen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="2e2e1-113">Definition für ein Feld</span><span class="sxs-lookup"><span data-stu-id="2e2e1-113">Field Definition</span></span>

<span data-ttu-id="2e2e1-114">Eine Definition für ein Feld enthält den Namen, Datentyp und andere Informationen über das Feld.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="2e2e1-115">Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft des entsprechenden **IMessage** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="2e2e1-116">Die **PidLidPropertyDefinitionStream** -Eigenschaft enthält einen binären Datenstrom bekannt als [PropertyDefinition](propertydefinition-stream-structure.md) , die die Felddefinitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="2e2e1-117">Weitere Informationen zu Stream Strukturen Felddefinitionen finden Sie unter [Stream-Strukturen](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="2e2e1-118">Feldwert</span><span class="sxs-lookup"><span data-stu-id="2e2e1-118">Field Value</span></span>

<span data-ttu-id="2e2e1-119">Jedes benutzerdefinierte Feld eines Elements ist einen Wert, der in einer entsprechenden benannten Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="2e2e1-120">Mit dem Namen der Eigenschaft in die PS_PUBLIC_STRINGS-Eigenschaft festgelegt ist und eine Unicode-Zeichenfolge als Eigenschaftenname hat.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="2e2e1-121">Der Datentyp der Eigenschaft entspricht dem Typ des Felds.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="2e2e1-122">Wenn die Eigenschaft nicht im **IMessage** -Objekt vorhanden ist, geht Outlook einen angemessene Standardwert für die Eigenschaft aus.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="2e2e1-123">Beispielsweise wird vorausgesetzt für einen Typ String Outlook eine leere Zeichenfolge, wenn die Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e2e1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e2e1-124">See also</span></span>



[<span data-ttu-id="2e2e1-125">Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="2e2e1-126">PropertyDefinition Stream-Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e2e1-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="2e2e1-127">Stream-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2e2e1-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="2e2e1-128">PropertyDefinition Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="2e2e1-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="2e2e1-129">FieldDefinition Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="2e2e1-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="2e2e1-130">SkipBlock Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="2e2e1-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="2e2e1-131">FirstSkipBlockContent Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="2e2e1-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="2e2e1-132">PackedAnsiString Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="2e2e1-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="2e2e1-133">PackedUnicodeString Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="2e2e1-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

