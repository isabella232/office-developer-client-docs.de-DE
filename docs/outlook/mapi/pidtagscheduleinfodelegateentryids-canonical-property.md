---
title: Kanonische Pidtagscheduleinfodelegateentryids (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b2adde7c5ecc75fda25b94d005fabfcd705d5d07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321294"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="84c1f-103">Kanonische Pidtagscheduleinfodelegateentryids (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="84c1f-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="84c1f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84c1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84c1f-105">Enthält die **EntryIDs** der Stellvertretungen.</span><span class="sxs-lookup"><span data-stu-id="84c1f-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84c1f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="84c1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84c1f-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="84c1f-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="84c1f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="84c1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84c1f-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="84c1f-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="84c1f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="84c1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="84c1f-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="84c1f-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="84c1f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="84c1f-112">Area:</span></span>  <br/> |<span data-ttu-id="84c1f-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="84c1f-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84c1f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84c1f-114">Remarks</span></span>

<span data-ttu-id="84c1f-115">Jeder Eintrag muss den Wert der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft des Adressbucheintrags der einzelnen Delegaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="84c1f-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="84c1f-116">Diese Eigenschaft muss im Delegate Information-Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="84c1f-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84c1f-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="84c1f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84c1f-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="84c1f-118">Protocol specifications</span></span>

<span data-ttu-id="84c1f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84c1f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84c1f-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="84c1f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84c1f-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84c1f-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84c1f-122">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="84c1f-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84c1f-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="84c1f-123">Header files</span></span>

<span data-ttu-id="84c1f-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="84c1f-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="84c1f-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="84c1f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="84c1f-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="84c1f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="84c1f-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="84c1f-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84c1f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84c1f-128">See also</span></span>



[<span data-ttu-id="84c1f-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84c1f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84c1f-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84c1f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84c1f-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="84c1f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84c1f-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="84c1f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

