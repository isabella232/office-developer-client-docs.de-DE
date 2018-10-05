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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393271"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="a474a-103">PidLidPropertyDefinitionStream (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a474a-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="a474a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a474a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a474a-105">Stellt Definitionen der benutzerdefinierten Felder und Datenbindung Einstellungen für integrierte Felder einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a474a-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a474a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a474a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a474a-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="a474a-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="a474a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="a474a-108">Property set:</span></span>  <br/> |<span data-ttu-id="a474a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a474a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a474a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="a474a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a474a-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="a474a-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="a474a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a474a-112">Data type:</span></span>  <br/> |<span data-ttu-id="a474a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a474a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a474a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a474a-114">Area:</span></span>  <br/> |<span data-ttu-id="a474a-115">Laufzeit-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a474a-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a474a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a474a-116">Remarks</span></span>

<span data-ttu-id="a474a-117">Der Wert der Eigenschaft **PidLidPropertyDefinitionStream** wird als Teil der Definition der benutzerdefiniertes Formular für die Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a474a-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="a474a-118">Der Wert dieser Eigenschaft ist einen binären Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="a474a-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="a474a-119">Informationen zur Struktur dieses Streams finden Sie unter [PropertyDefinition Stream Struktur](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="a474a-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a474a-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a474a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a474a-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a474a-121">Protocol specifications</span></span>

<span data-ttu-id="a474a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a474a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a474a-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a474a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a474a-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a474a-124">Header files</span></span>

<span data-ttu-id="a474a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a474a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a474a-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a474a-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a474a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a474a-127">See also</span></span>



[<span data-ttu-id="a474a-128">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="a474a-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="a474a-129">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="a474a-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="a474a-130">Beispiel für PropertyDefinition-Stream</span><span class="sxs-lookup"><span data-stu-id="a474a-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="a474a-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a474a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a474a-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a474a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a474a-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a474a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a474a-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a474a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

