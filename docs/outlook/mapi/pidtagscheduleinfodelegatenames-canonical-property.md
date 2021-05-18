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
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314938"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="f3186-103">PidTagScheduleInfoDelegateNames (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f3186-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="f3186-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3186-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3186-105">Enthält die Namen der Stellvertreter.</span><span class="sxs-lookup"><span data-stu-id="f3186-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3186-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f3186-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3186-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="f3186-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="f3186-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f3186-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3186-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="f3186-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="f3186-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f3186-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3186-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f3186-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f3186-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f3186-112">Area:</span></span>  <br/> |<span data-ttu-id="f3186-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="f3186-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3186-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3186-114">Remarks</span></span>

<span data-ttu-id="f3186-115">Jeder Eintrag in diesen Eigenschaften muss den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft des Adressbuchs jeder Stellvertretung enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3186-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f3186-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f3186-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3186-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f3186-117">Protocol specifications</span></span>

<span data-ttu-id="f3186-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3186-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3186-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f3186-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3186-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3186-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3186-121">Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="f3186-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3186-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f3186-122">Header files</span></span>

<span data-ttu-id="f3186-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3186-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3186-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f3186-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3186-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3186-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f3186-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f3186-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3186-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3186-127">See also</span></span>



[<span data-ttu-id="f3186-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3186-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3186-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f3186-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3186-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f3186-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3186-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f3186-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

