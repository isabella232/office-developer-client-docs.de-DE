---
title: PidLidAnniversaryEventEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b20234d079fb38fac878efe92390defcba6e5d1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399627"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="4cd9c-103">PidLidAnniversaryEventEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4cd9c-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4cd9c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cd9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cd9c-105">Gibt die Eintrags-ID des Termins, die das Jahrestag des Kontakts darstellt.</span><span class="sxs-lookup"><span data-stu-id="4cd9c-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4cd9c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4cd9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cd9c-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="4cd9c-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="4cd9c-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4cd9c-108">Property set:</span></span>  <br/> |<span data-ttu-id="4cd9c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="4cd9c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="4cd9c-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4cd9c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4cd9c-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="4cd9c-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="4cd9c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4cd9c-112">Data type:</span></span>  <br/> |<span data-ttu-id="4cd9c-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4cd9c-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4cd9c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4cd9c-114">Area:</span></span>  <br/> |<span data-ttu-id="4cd9c-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="4cd9c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cd9c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4cd9c-116">Remarks</span></span>

<span data-ttu-id="4cd9c-117">Der Termin durch die **DispidAnniversaryEventEID** -Eigenschaft angegebenen muss mit diesen Kontakt verknüpft werden, mithilfe der **DispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) **DispidContactLinkSearchKey** ([ PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), und die Eigenschaften der **DispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), die detaillierte in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4cd9c-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4cd9c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4cd9c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4cd9c-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4cd9c-119">Protocol specifications</span></span>

<span data-ttu-id="4cd9c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cd9c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cd9c-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4cd9c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4cd9c-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cd9c-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cd9c-123">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4cd9c-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4cd9c-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4cd9c-124">Header files</span></span>

<span data-ttu-id="4cd9c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cd9c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cd9c-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4cd9c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cd9c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cd9c-127">See also</span></span>



[<span data-ttu-id="4cd9c-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd9c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cd9c-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd9c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cd9c-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4cd9c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cd9c-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4cd9c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

