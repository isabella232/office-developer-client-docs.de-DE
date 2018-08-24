---
title: PidTagScheduleInfoDelegateNames (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 06462f992ec640992b95b89a618e7d82290eeeef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574503"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="2fa11-103">PidTagScheduleInfoDelegateNames (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2fa11-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="2fa11-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fa11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fa11-105">Enthält die Namen der-Delegaten.</span><span class="sxs-lookup"><span data-stu-id="2fa11-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2fa11-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2fa11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2fa11-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="2fa11-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="2fa11-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2fa11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2fa11-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="2fa11-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="2fa11-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2fa11-110">Data type:</span></span>  <br/> |<span data-ttu-id="2fa11-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2fa11-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2fa11-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2fa11-112">Area:</span></span>  <br/> |<span data-ttu-id="2fa11-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="2fa11-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fa11-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fa11-114">Remarks</span></span>

<span data-ttu-id="2fa11-115">Jeder Eintrag in diese Eigenschaften muss den Wert der Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) der einzelnen Delegaten Adressbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="2fa11-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2fa11-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2fa11-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2fa11-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2fa11-117">Protocol specifications</span></span>

<span data-ttu-id="2fa11-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2fa11-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2fa11-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2fa11-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2fa11-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2fa11-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2fa11-121">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="2fa11-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2fa11-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2fa11-122">Header files</span></span>

<span data-ttu-id="2fa11-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2fa11-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2fa11-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2fa11-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2fa11-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2fa11-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2fa11-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2fa11-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2fa11-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fa11-127">See also</span></span>



[<span data-ttu-id="2fa11-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fa11-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2fa11-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fa11-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2fa11-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2fa11-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2fa11-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2fa11-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

