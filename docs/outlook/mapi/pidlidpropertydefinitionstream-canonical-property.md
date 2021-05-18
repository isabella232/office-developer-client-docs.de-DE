---
title: PidLidPropertyDefinitionStream (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b5ddb87111cfb0039cb1150338945615bbd5afc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315939"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="429d6-103">PidLidPropertyDefinitionStream (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="429d6-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="429d6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="429d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="429d6-105">Stellt Definitionen von benutzerdefinierten Feldern und Datenbindungseinstellungen von integrierten Feldern einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="429d6-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="429d6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="429d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="429d6-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="429d6-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="429d6-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="429d6-108">Property set:</span></span>  <br/> |<span data-ttu-id="429d6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="429d6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="429d6-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="429d6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="429d6-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="429d6-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="429d6-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="429d6-112">Data type:</span></span>  <br/> |<span data-ttu-id="429d6-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="429d6-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="429d6-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="429d6-114">Area:</span></span>  <br/> |<span data-ttu-id="429d6-115">Laufzeitkonfiguration</span><span class="sxs-lookup"><span data-stu-id="429d6-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="429d6-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="429d6-116">Remarks</span></span>

<span data-ttu-id="429d6-117">Der Wert der **PidLidPropertyDefinitionStream-Eigenschaft** wird als Teil der benutzerdefinierten Formulardefinition für die Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="429d6-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="429d6-118">Der Wert dieser Eigenschaft ist ein binärer Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="429d6-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="429d6-119">Informationen zur Struktur dieses Datenstroms finden Sie unter [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="429d6-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="429d6-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="429d6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="429d6-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="429d6-121">Protocol specifications</span></span>

<span data-ttu-id="429d6-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="429d6-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="429d6-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="429d6-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="429d6-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="429d6-124">Header files</span></span>

<span data-ttu-id="429d6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="429d6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="429d6-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="429d6-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="429d6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="429d6-127">See also</span></span>



[<span data-ttu-id="429d6-128">Outlook-Elemente und -Felder</span><span class="sxs-lookup"><span data-stu-id="429d6-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="429d6-129">Hinzufügen einer Definition für ein new User-Defined Field</span><span class="sxs-lookup"><span data-stu-id="429d6-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="429d6-130">PropertyDefinition Stream Sample</span><span class="sxs-lookup"><span data-stu-id="429d6-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="429d6-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="429d6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="429d6-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="429d6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="429d6-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="429d6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="429d6-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="429d6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

