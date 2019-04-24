---
title: Kanonische Pidlidbirthdayevententryid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 90d1dc8a9ce7f94238e8754cfbcaf88b702928f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342021"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="5bad0-103">Kanonische Pidlidbirthdayevententryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5bad0-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5bad0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bad0-105">Gibt die **Eintrags** -Nr. eines optionalen Termins an, der den Geburtstag des Kontakts darstellt.</span><span class="sxs-lookup"><span data-stu-id="5bad0-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bad0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5bad0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bad0-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="5bad0-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="5bad0-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="5bad0-108">Property set:</span></span>  <br/> |<span data-ttu-id="5bad0-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5bad0-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5bad0-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="5bad0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5bad0-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="5bad0-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="5bad0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5bad0-112">Data type:</span></span>  <br/> |<span data-ttu-id="5bad0-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5bad0-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5bad0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5bad0-114">Area:</span></span>  <br/> |<span data-ttu-id="5bad0-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="5bad0-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bad0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bad0-116">Remarks</span></span>

<span data-ttu-id="5bad0-117">Der von dieser Eigenschaft angegebene Termin muss mit dem **dispidApptStateFlags** ([Pidlidcontactlinkentry (](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([pidlidcontactlinksearchkey (](pidlidcontactlinksearchkey-canonical-property.md)) und \*\* dispidContactLinkName\*\* ([pidlidcontactlinkname (](pidlidcontactlinkname-canonical-property.md))-Eigenschaft gemäß [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5bad0-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5bad0-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5bad0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5bad0-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5bad0-119">Protocol specifications</span></span>

<span data-ttu-id="5bad0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bad0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bad0-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="5bad0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5bad0-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bad0-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bad0-123">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5bad0-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5bad0-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5bad0-124">Header files</span></span>

<span data-ttu-id="5bad0-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5bad0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bad0-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5bad0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bad0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bad0-127">See also</span></span>



[<span data-ttu-id="5bad0-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5bad0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bad0-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5bad0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bad0-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5bad0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bad0-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5bad0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

