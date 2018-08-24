---
title: Elemente und Felder in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: caa231842c5fd51deb80144f12fdf53e51ccc980
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582875"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="401ae-103">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="401ae-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="401ae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="401ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="401ae-105">Microsoft Outlook bietet Elementtypen, die speziell auf ihre Funktionalität (beispielsweise e-Mail-Elementen, Termine, Kontakte, Aufgaben und Notizen) sind.</span><span class="sxs-lookup"><span data-stu-id="401ae-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="401ae-106">Outlook bietet Standardfelder für jede Art von Element als integrierte Felder bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="401ae-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="401ae-107">Outlook kann der Benutzer zum Erstellen von benutzerdefinierter Feldern, als benutzerdefinierte Felder bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="401ae-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="401ae-108">Jedes Feld ist einen Datentyp und einen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="401ae-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="401ae-109">Beispiele für Datentypen sind **Währung**, **Datum/Uhrzeit**, **Dauer**, **ganze Zahl**, **Schlüsselwörter**und **Text**.</span><span class="sxs-lookup"><span data-stu-id="401ae-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="401ae-110">Benutzer können benutzerdefinierte Felder im Formular-Designer in Outlook mit definieren.</span><span class="sxs-lookup"><span data-stu-id="401ae-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="401ae-111">Auf Ebene der Programmierbarkeit wird jedes Element durch ein [IMessage](imessageimapiprop.md) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="401ae-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="401ae-112">Jedes benutzerdefinierte Feld ist eine Definition für ein Feld und einen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="401ae-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="401ae-113">Definition für ein Feld</span><span class="sxs-lookup"><span data-stu-id="401ae-113">Field Definition</span></span>

<span data-ttu-id="401ae-114">Eine Definition für ein Feld enthält den Namen, Datentyp und andere Informationen über das Feld.</span><span class="sxs-lookup"><span data-stu-id="401ae-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="401ae-115">Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft des entsprechenden **IMessage** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="401ae-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="401ae-116">Die **PidLidPropertyDefinitionStream** -Eigenschaft enthält einen binären Datenstrom bekannt als [PropertyDefinition](propertydefinition-stream-structure.md) , die die Felddefinitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="401ae-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="401ae-117">Weitere Informationen zu Stream Strukturen Felddefinitionen finden Sie unter [Stream-Strukturen](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="401ae-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="401ae-118">Feldwert</span><span class="sxs-lookup"><span data-stu-id="401ae-118">Field Value</span></span>

<span data-ttu-id="401ae-119">Jedes benutzerdefinierte Feld eines Elements ist einen Wert, der in einer entsprechenden benannten Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="401ae-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="401ae-120">Mit dem Namen der Eigenschaft in die PS_PUBLIC_STRINGS-Eigenschaft festgelegt ist und eine Unicode-Zeichenfolge als Eigenschaftenname hat.</span><span class="sxs-lookup"><span data-stu-id="401ae-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="401ae-121">Der Datentyp der Eigenschaft entspricht dem Typ des Felds.</span><span class="sxs-lookup"><span data-stu-id="401ae-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="401ae-122">Wenn die Eigenschaft nicht im **IMessage** -Objekt vorhanden ist, geht Outlook einen angemessene Standardwert für die Eigenschaft aus.</span><span class="sxs-lookup"><span data-stu-id="401ae-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="401ae-123">Beispielsweise wird vorausgesetzt für einen Typ String Outlook eine leere Zeichenfolge, wenn die Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="401ae-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="401ae-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="401ae-124">See also</span></span>



[<span data-ttu-id="401ae-125">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="401ae-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="401ae-126">Beispiel für PropertyDefinition-Stream</span><span class="sxs-lookup"><span data-stu-id="401ae-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="401ae-127">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="401ae-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="401ae-128">PropertyDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="401ae-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="401ae-129">FieldDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="401ae-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="401ae-130">SkipBlock-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="401ae-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="401ae-131">FirstSkipBlockContent-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="401ae-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="401ae-132">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="401ae-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="401ae-133">PackedUnicodeString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="401ae-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

