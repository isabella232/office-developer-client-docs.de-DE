---
title: PidLidBirthdayEventEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBirthdayEventEntryId
api_type:
- COM
ms.assetid: 6807dcfc-d9bd-48a1-a093-3097b2cb107c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d8a142729d1c86c615653b2cbfc708268d4322e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576778"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="7011f-103">PidLidBirthdayEventEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7011f-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7011f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7011f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7011f-105">Gibt die **EntryId** des Termins optional, die das Geburtsdatum des Kontakts darstellt.</span><span class="sxs-lookup"><span data-stu-id="7011f-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7011f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7011f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7011f-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="7011f-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="7011f-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7011f-108">Property set:</span></span>  <br/> |<span data-ttu-id="7011f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="7011f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="7011f-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="7011f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7011f-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="7011f-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="7011f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7011f-112">Data type:</span></span>  <br/> |<span data-ttu-id="7011f-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7011f-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7011f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7011f-114">Area:</span></span>  <br/> |<span data-ttu-id="7011f-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="7011f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7011f-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7011f-116">Remarks</span></span>

<span data-ttu-id="7011f-117">Des Termins werden dies von dieser Eigenschaft angegeben wird muss mit diesem Kontakt verknüpft werden, mithilfe der **DispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **DispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) und ** DispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) Eigenschaften, die im angegebenen [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7011f-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7011f-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7011f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7011f-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7011f-119">Protocol specifications</span></span>

<span data-ttu-id="7011f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7011f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7011f-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7011f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7011f-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7011f-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7011f-123">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7011f-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7011f-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7011f-124">Header files</span></span>

<span data-ttu-id="7011f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7011f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7011f-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7011f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7011f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7011f-127">See also</span></span>



[<span data-ttu-id="7011f-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7011f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7011f-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7011f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7011f-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7011f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7011f-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7011f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

