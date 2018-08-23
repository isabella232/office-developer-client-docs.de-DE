---
title: PidTagScheduleInfoDelegateEntryIds (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f7521d387fa45c191a67f2a20320fac700baed37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567216"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="87531-103">PidTagScheduleInfoDelegateEntryIds (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="87531-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="87531-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87531-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87531-105">Enthält den **EntryIDs** Stellvertretungen.</span><span class="sxs-lookup"><span data-stu-id="87531-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87531-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="87531-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87531-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="87531-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="87531-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="87531-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87531-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="87531-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="87531-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="87531-110">Data type:</span></span>  <br/> |<span data-ttu-id="87531-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="87531-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="87531-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="87531-112">Area:</span></span>  <br/> |<span data-ttu-id="87531-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="87531-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87531-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="87531-114">Remarks</span></span>

<span data-ttu-id="87531-115">Jeder Eintrag muss den Wert der Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) der einzelnen Delegaten Adresseintrag Adressbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="87531-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="87531-116">Diese Eigenschaft muss im Delegaten Informationen-Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87531-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87531-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="87531-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87531-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="87531-118">Protocol specifications</span></span>

<span data-ttu-id="87531-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87531-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87531-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="87531-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87531-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87531-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87531-122">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="87531-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87531-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="87531-123">Header files</span></span>

<span data-ttu-id="87531-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87531-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="87531-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="87531-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="87531-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="87531-126">Mapitags.h</span></span>
  
> <span data-ttu-id="87531-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="87531-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87531-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87531-128">See also</span></span>



[<span data-ttu-id="87531-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87531-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87531-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87531-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87531-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="87531-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87531-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="87531-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

