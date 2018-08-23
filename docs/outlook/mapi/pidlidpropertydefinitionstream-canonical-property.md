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
ms.openlocfilehash: 23850e7da71125642abd8484fb45b8ec23264748
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587649"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="52554-103">PidLidPropertyDefinitionStream (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="52554-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="52554-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52554-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52554-105">Stellt Definitionen der benutzerdefinierten Felder und Datenbindung Einstellungen für integrierte Felder einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="52554-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52554-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="52554-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52554-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="52554-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="52554-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="52554-108">Property set:</span></span>  <br/> |<span data-ttu-id="52554-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="52554-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="52554-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="52554-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="52554-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="52554-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="52554-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="52554-112">Data type:</span></span>  <br/> |<span data-ttu-id="52554-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="52554-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="52554-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="52554-114">Area:</span></span>  <br/> |<span data-ttu-id="52554-115">Laufzeit-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="52554-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52554-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="52554-116">Remarks</span></span>

<span data-ttu-id="52554-117">Der Wert der Eigenschaft **PidLidPropertyDefinitionStream** wird als Teil der Definition der benutzerdefiniertes Formular für die Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="52554-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="52554-118">Der Wert dieser Eigenschaft ist einen binären Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="52554-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="52554-119">Informationen zur Struktur dieses Streams finden Sie unter [PropertyDefinition Stream Struktur](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="52554-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52554-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="52554-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52554-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="52554-121">Protocol specifications</span></span>

<span data-ttu-id="52554-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52554-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52554-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="52554-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52554-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="52554-124">Header files</span></span>

<span data-ttu-id="52554-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52554-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="52554-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="52554-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52554-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52554-127">See also</span></span>



[<span data-ttu-id="52554-128">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="52554-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="52554-129">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="52554-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="52554-130">Beispiel für PropertyDefinition-Stream</span><span class="sxs-lookup"><span data-stu-id="52554-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="52554-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52554-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52554-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52554-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52554-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="52554-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52554-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="52554-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

