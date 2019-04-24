---
title: Kanonische Pidtagmappingsignature (-Eigenschaft
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
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342546"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="9e3d5-103">Kanonische Pidtagmappingsignature (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e3d5-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="9e3d5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e3d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e3d5-105">Enthält die Zuordnungs Signatur für benannte Eigenschaften eines bestimmten MAPI-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e3d5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9e3d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e3d5-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="9e3d5-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="9e3d5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9e3d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e3d5-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="9e3d5-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="9e3d5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9e3d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e3d5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9e3d5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9e3d5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9e3d5-112">Area:</span></span>  <br/> |<span data-ttu-id="9e3d5-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="9e3d5-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e3d5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e3d5-114">Remarks</span></span>

<span data-ttu-id="9e3d5-115">Es wird empfohlen, dass Objekte mit benannten Eigenschaften diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="9e3d5-116">Eine Clientanwendung sollte die **PR_MAPPING_SIGNATURE** -Eigenschaft beider Objekte beim Kopieren benannter Eigenschaften von einem Objekt in ein anderes überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="9e3d5-117">Die Verwendung dieser Eigenschaft kann die Übersetzung zwischen den Namen und Bezeichnern der kopierten Eigenschaften minimieren.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="9e3d5-118">Wenn diese Eigenschaft für ein bestimmtes MAPI-Objekt nicht vorhanden ist, weist das Objekt eine eigene eindeutige Zuordnung von Namen und Bezeichnern auf.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="9e3d5-119">In diesem Fall muss der Client die [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methode für das Source-Objekt und dann die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode für das Zielobjekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="9e3d5-120">Wenn zwei Objekte den gleichen **PR_MAPPING_SIGNATURE** -Wert haben, muss der Clientname nicht in Bezeichner und Bezeichner konvertieren.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="9e3d5-121">Der Client kann einfach die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode für die Quelle und dann die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode für das Ziel aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="9e3d5-122">Dies ist für Clients geeignet, die benutzerdefinierte Kopien benannter Eigenschaften ausführen, und für Anbieter, die die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -und [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="9e3d5-123">Weitere Informationen zu benannten Eigenschaften und zur Zuordnung von Namen und Bezeichnern finden Sie unter [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9e3d5-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9e3d5-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9e3d5-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e3d5-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9e3d5-125">Protocol specifications</span></span>

<span data-ttu-id="9e3d5-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e3d5-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e3d5-127">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e3d5-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e3d5-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e3d5-129">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e3d5-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="9e3d5-130">Header files</span></span>

<span data-ttu-id="9e3d5-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9e3d5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e3d5-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e3d5-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9e3d5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9e3d5-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9e3d5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e3d5-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e3d5-135">See also</span></span>



[<span data-ttu-id="9e3d5-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="9e3d5-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="9e3d5-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e3d5-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e3d5-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e3d5-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e3d5-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9e3d5-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e3d5-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9e3d5-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

