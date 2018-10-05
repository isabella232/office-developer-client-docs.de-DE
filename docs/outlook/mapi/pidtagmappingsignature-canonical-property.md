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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396225"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="df77c-103">PidTagMappingSignature (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="df77c-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="df77c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df77c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df77c-105">Die Zuordnung Signatur für benannte Eigenschaften eines bestimmten MAPI-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="df77c-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df77c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="df77c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df77c-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="df77c-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="df77c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="df77c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df77c-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="df77c-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="df77c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="df77c-110">Data type:</span></span>  <br/> |<span data-ttu-id="df77c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="df77c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="df77c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="df77c-112">Area:</span></span>  <br/> |<span data-ttu-id="df77c-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="df77c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df77c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df77c-114">Remarks</span></span>

<span data-ttu-id="df77c-115">Es wird empfohlen, diese Eigenschaft für Objekte mit dem benannten Eigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="df77c-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="df77c-116">Eine Clientanwendung sollte überprüfen Sie die Eigenschaft **PR_MAPPING_SIGNATURE** beider übergebener Objekte beim Kopieren mit dem Eigenschaften eines Objekts in einen anderen Namen.</span><span class="sxs-lookup"><span data-stu-id="df77c-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="df77c-117">Verwendung dieser Eigenschaft können Sie minimieren übersetzen zwischen Namen und Bezeichner kopierten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="df77c-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="df77c-118">Wenn diese Eigenschaft für ein bestimmtes MAPI-Objekt nicht vorhanden ist, hat das Objekt eine eigene eindeutige Zuordnung von Namen und Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="df77c-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="df77c-119">In diesem Fall muss der Client die [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methode für das Quellobjekt und dann die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode für das Zielobjekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df77c-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="df77c-120">Wenn zwei Objekte den gleichen Wert **PR_MAPPING_SIGNATURE** sind, muss der Client nicht Name, ID und Name-ID übersetzen.</span><span class="sxs-lookup"><span data-stu-id="df77c-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="df77c-121">Der Client kann die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode auf das Ziel einfach auf die Quelle, und klicken Sie dann die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df77c-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="df77c-122">Dies ist hilfreich für Clients, die benutzerdefinierte Kopieren von benannten Eigenschaften ausführen, und der Anbieter die [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps](imapiprop-copyprops.md) -Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="df77c-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="df77c-123">Weitere Informationen zu benannten Eigenschaften und Zuordnung von Namen und Bezeichner finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="df77c-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="df77c-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="df77c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df77c-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="df77c-125">Protocol specifications</span></span>

<span data-ttu-id="df77c-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df77c-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df77c-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="df77c-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df77c-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df77c-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df77c-129">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="df77c-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df77c-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="df77c-130">Header files</span></span>

<span data-ttu-id="df77c-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df77c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="df77c-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="df77c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="df77c-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df77c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="df77c-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="df77c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df77c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df77c-135">See also</span></span>



[<span data-ttu-id="df77c-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="df77c-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="df77c-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df77c-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df77c-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df77c-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df77c-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="df77c-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df77c-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="df77c-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

