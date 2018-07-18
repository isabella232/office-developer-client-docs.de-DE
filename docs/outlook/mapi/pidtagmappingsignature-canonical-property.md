---
title: PidTagMappingSignature (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0a83e0aa8f7ab1eb1f30e3ba97d3ea36f16fd873
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794581"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="80e15-103">PidTagMappingSignature (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="80e15-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="80e15-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80e15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80e15-105">Die Zuordnung Signatur für benannte Eigenschaften eines bestimmten MAPI-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="80e15-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80e15-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="80e15-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80e15-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="80e15-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="80e15-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="80e15-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80e15-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="80e15-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="80e15-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="80e15-110">Data type:</span></span>  <br/> |<span data-ttu-id="80e15-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="80e15-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="80e15-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="80e15-112">Area:</span></span>  <br/> |<span data-ttu-id="80e15-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="80e15-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80e15-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80e15-114">Remarks</span></span>

<span data-ttu-id="80e15-115">Es wird empfohlen, diese Eigenschaft für Objekte mit dem benannten Eigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="80e15-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="80e15-116">Eine Clientanwendung sollte überprüfen Sie die Eigenschaft **PR_MAPPING_SIGNATURE** beider übergebener Objekte beim Kopieren mit dem Eigenschaften eines Objekts in einen anderen Namen.</span><span class="sxs-lookup"><span data-stu-id="80e15-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="80e15-117">Verwendung dieser Eigenschaft können Sie minimieren übersetzen zwischen Namen und Bezeichner kopierten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="80e15-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="80e15-118">Wenn diese Eigenschaft für ein bestimmtes MAPI-Objekt nicht vorhanden ist, hat das Objekt eine eigene eindeutige Zuordnung von Namen und Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="80e15-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="80e15-119">In diesem Fall muss der Client die [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methode für das Quellobjekt und dann die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode für das Zielobjekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="80e15-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="80e15-120">Wenn zwei Objekte den gleichen Wert **PR_MAPPING_SIGNATURE** sind, muss der Client nicht Name, ID und Name-ID übersetzen.</span><span class="sxs-lookup"><span data-stu-id="80e15-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="80e15-121">Der Client kann die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode auf das Ziel einfach auf die Quelle, und klicken Sie dann die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="80e15-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="80e15-122">Dies ist hilfreich für Clients, die benutzerdefinierte Kopieren von benannten Eigenschaften ausführen, und der Anbieter die [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps](imapiprop-copyprops.md) -Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="80e15-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="80e15-123">Weitere Informationen zu benannten Eigenschaften und Zuordnung von Namen und Bezeichner finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="80e15-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="80e15-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="80e15-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80e15-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="80e15-125">Protocol specifications</span></span>

<span data-ttu-id="80e15-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80e15-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80e15-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="80e15-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80e15-128">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80e15-128">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80e15-129">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="80e15-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80e15-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="80e15-130">Header files</span></span>

<span data-ttu-id="80e15-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80e15-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="80e15-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="80e15-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="80e15-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="80e15-133">Mapitags.h</span></span>
  
> <span data-ttu-id="80e15-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="80e15-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80e15-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80e15-135">See also</span></span>



[<span data-ttu-id="80e15-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="80e15-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="80e15-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80e15-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80e15-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80e15-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80e15-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="80e15-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80e15-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="80e15-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

