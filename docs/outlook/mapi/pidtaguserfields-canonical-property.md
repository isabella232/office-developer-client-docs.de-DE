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
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360739"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="2854c-103">PidTagUserFields (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2854c-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="2854c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2854c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2854c-105">Enthält den Namen, den Datentyp und andere Informationen zu einem benutzerdefinierten Feld.</span><span class="sxs-lookup"><span data-stu-id="2854c-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2854c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2854c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2854c-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="2854c-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="2854c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2854c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2854c-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="2854c-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="2854c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2854c-110">Data type:</span></span>  <br/> |<span data-ttu-id="2854c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2854c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2854c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2854c-112">Area:</span></span>  <br/> |<span data-ttu-id="2854c-113">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="2854c-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2854c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2854c-114">Remarks</span></span>

<span data-ttu-id="2854c-115">Für jedes Element speichert Outlook definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) des entsprechenden **IMessage-Objekts.**</span><span class="sxs-lookup"><span data-stu-id="2854c-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="2854c-116">Die **PidLidPropertyDefinitionStream-Eigenschaft** enthält einen binären Datenstrom mit dem Namen [PropertyDefinition](propertydefinition-stream-structure.md), der die Felddefinitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="2854c-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="2854c-117">Weitere Informationen zu Streamstrukturen für Felddefinitionen finden Sie unter [Stream Structures](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="2854c-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="2854c-118">Für jeden Ordner speichert Outlook die Definitionen aller benutzerdefinierten Felder in diesem Ordner in der **PidTagUserFields-Eigenschaft** einer zugeordneten Nachricht der Nachrichtenklasse IPC.MS. REN. USERFIELDS – Jeder Ordner, der davon ausgegangen wird, dass er nur eine Nachricht dieser Klasse in der zugehörigen Inhaltstabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="2854c-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2854c-119">Der Satz von benutzerdefinierten Feldern in einem Ordner ist möglicherweise nicht unbedingt mit den Benutzerdefinierten Feldern in den einzelnen Elementen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="2854c-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="2854c-120">Der Satz von benutzerdefinierten Feldern in einem Ordner wird an verschiedenen Stellen in der benutzerdefinierten Outlook angezeigt, z. B. an der Feld-Auswahl des Ordners.</span><span class="sxs-lookup"><span data-stu-id="2854c-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="2854c-121">Die **PidTagUserFields-Eigenschaft** der Nachricht enthält einen binären **Datenstrom, FolderUserFields**, der die Ordnerfelddefinitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="2854c-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="2854c-122">Weitere Informationen zu Streamstrukturen für Ordnerfelddefinitionen finden Sie unter [Folder Fields Stream Structures](folder-fields-stream-structures.md) und [folderUserFields Stream Sample](folderuserfields-stream-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2854c-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="2854c-123">Abschnittsüberschrift</span><span class="sxs-lookup"><span data-stu-id="2854c-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2854c-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2854c-124">Protocol specifications</span></span>

<span data-ttu-id="2854c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2854c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2854c-126">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2854c-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2854c-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="2854c-127">Header files</span></span>

<span data-ttu-id="2854c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2854c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2854c-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2854c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2854c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2854c-130">See also</span></span>



[<span data-ttu-id="2854c-131">Outlook Elemente und Felder</span><span class="sxs-lookup"><span data-stu-id="2854c-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="2854c-132">Hinzufügen einer Definition für ein new User-Defined Field</span><span class="sxs-lookup"><span data-stu-id="2854c-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="2854c-133">PropertyDefinition Stream Sample</span><span class="sxs-lookup"><span data-stu-id="2854c-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="2854c-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2854c-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2854c-135">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="2854c-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2854c-136">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2854c-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2854c-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2854c-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

