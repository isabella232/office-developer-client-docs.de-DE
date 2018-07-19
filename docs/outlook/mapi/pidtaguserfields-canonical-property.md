---
title: PidTagUserFields (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5abfd9c98c5a83ca45792f094d0c9573b8affb85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795276"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="03415-103">PidTagUserFields (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="03415-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="03415-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03415-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03415-105">Enthält den Namen, Datentyp und andere Informationen zu einem benutzerdefinierten Feld.</span><span class="sxs-lookup"><span data-stu-id="03415-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03415-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="03415-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03415-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="03415-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="03415-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="03415-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03415-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="03415-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="03415-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="03415-110">Data type:</span></span>  <br/> |<span data-ttu-id="03415-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="03415-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="03415-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="03415-112">Area:</span></span>  <br/> |<span data-ttu-id="03415-113">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="03415-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03415-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03415-114">Remarks</span></span>

<span data-ttu-id="03415-115">Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft des entsprechenden **IMessage** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="03415-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="03415-116">Die **PidLidPropertyDefinitionStream** -Eigenschaft enthält einen binären Datenstrom bekannt als [PropertyDefinition](propertydefinition-stream-structure.md), die die Felddefinitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="03415-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="03415-117">Weitere Informationen zu Stream Strukturen Felddefinitionen finden Sie unter [Stream-Strukturen](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="03415-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="03415-118">Für jeden Ordner speichert Outlook die Definitionen aller benutzerdefinierten Felder in dem Ordner, in der **PidTagUserFields** -Eigenschaft einer zugeordneten Nachricht der Nachrichtenklasse IPC.MS. REN. BENUTZERFELDER - davon ausgegangen, dass jeder Ordner nicht mehr als eine Nachricht dieser Klasse in der Inhaltstabelle zugeordneten enthalten.</span><span class="sxs-lookup"><span data-stu-id="03415-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03415-119">Der Satz von benutzerdefinierten Feldern in einem Ordner möglicherweise nicht unbedingt die Sätze von benutzerdefinierten Feldern in den einzelnen Elemente überein.</span><span class="sxs-lookup"><span data-stu-id="03415-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="03415-120">An verschiedenen Stellen in der Outlook-Benutzeroberfläche, wie des Ordners Feldauswahl wird der Satz von benutzerdefinierten Feldern in einem Ordner angezeigt.</span><span class="sxs-lookup"><span data-stu-id="03415-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="03415-121">Die Nachricht **PidTagUserFields** -Eigenschaft enthält einen binären Datenstrom, **FolderUserFields**, die Felddefinitionen Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="03415-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="03415-122">Weitere Informationen zu Stream Strukturen für Ordner Felddefinitionen finden Sie unter [Ordner Felder Stream Strukturen](folder-fields-stream-structures.md) und die [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span><span class="sxs-lookup"><span data-stu-id="03415-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="03415-123">Abschnittsüberschrift</span><span class="sxs-lookup"><span data-stu-id="03415-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03415-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="03415-124">Protocol specifications</span></span>

<span data-ttu-id="03415-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03415-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03415-126">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="03415-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03415-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="03415-127">Header files</span></span>

<span data-ttu-id="03415-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03415-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="03415-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="03415-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03415-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03415-130">See also</span></span>



[<span data-ttu-id="03415-131">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="03415-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="03415-132">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="03415-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="03415-133">Beispiel für PropertyDefinition-Stream</span><span class="sxs-lookup"><span data-stu-id="03415-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="03415-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03415-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03415-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03415-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03415-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="03415-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03415-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="03415-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

