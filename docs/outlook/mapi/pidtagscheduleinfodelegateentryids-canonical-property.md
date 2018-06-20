---
title: Kanonische PidTagScheduleInfoDelegateEntryIds-Eigenschaft
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
ms.openlocfilehash: 8ea60fb989cd85b23e6dd9302bc03a9b5befd20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795076"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="ff26e-103">Kanonische PidTagScheduleInfoDelegateEntryIds-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff26e-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="ff26e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff26e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff26e-105">Enthält den **EntryIDs** Stellvertretungen.</span><span class="sxs-lookup"><span data-stu-id="ff26e-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff26e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ff26e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff26e-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="ff26e-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="ff26e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ff26e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff26e-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="ff26e-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="ff26e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ff26e-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff26e-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff26e-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff26e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ff26e-112">Area:</span></span>  <br/> |<span data-ttu-id="ff26e-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="ff26e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff26e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ff26e-114">Remarks</span></span>

<span data-ttu-id="ff26e-115">Jeder Eintrag muss den Wert der Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) der einzelnen Delegaten Adresseintrag Adressbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff26e-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="ff26e-116">Diese Eigenschaft muss im Delegaten Informationen-Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ff26e-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ff26e-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ff26e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff26e-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ff26e-118">Protocol specifications</span></span>

<span data-ttu-id="ff26e-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff26e-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff26e-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ff26e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff26e-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff26e-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff26e-122">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="ff26e-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff26e-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ff26e-123">Header files</span></span>

<span data-ttu-id="ff26e-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff26e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff26e-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ff26e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff26e-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff26e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ff26e-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ff26e-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff26e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff26e-128">See also</span></span>



[<span data-ttu-id="ff26e-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff26e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff26e-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff26e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff26e-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ff26e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff26e-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ff26e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

