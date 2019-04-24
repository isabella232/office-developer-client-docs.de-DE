---
title: Kanonische Pidtagscheduleinfodelegatenames (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314938"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="ab996-103">Kanonische Pidtagscheduleinfodelegatenames (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ab996-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="ab996-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab996-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab996-105">Enthält die Namen der Delegaten.</span><span class="sxs-lookup"><span data-stu-id="ab996-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab996-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab996-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab996-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="ab996-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="ab996-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ab996-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab996-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="ab996-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="ab996-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab996-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab996-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab996-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ab996-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab996-112">Area:</span></span>  <br/> |<span data-ttu-id="ab996-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="ab996-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab996-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab996-114">Remarks</span></span>

<span data-ttu-id="ab996-115">Jeder Eintrag in diesen Eigenschaften muss den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Adressbuchs der einzelnen Delegaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="ab996-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ab996-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab996-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab996-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ab996-117">Protocol specifications</span></span>

<span data-ttu-id="ab996-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab996-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab996-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab996-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab996-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab996-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab996-121">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="ab996-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab996-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ab996-122">Header files</span></span>

<span data-ttu-id="ab996-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ab996-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab996-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="ab996-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab996-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ab996-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ab996-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ab996-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab996-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab996-127">See also</span></span>



[<span data-ttu-id="ab996-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab996-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab996-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab996-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab996-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ab996-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab996-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ab996-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

