---
title: PidTagSubmitFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339354"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="9fdc3-103">PidTagSubmitFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9fdc3-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="9fdc3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fdc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fdc3-105">Enthält eine Bitmaske mit Flags, die Details zu einer Nachrichtenübermittlung angibt.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9fdc3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9fdc3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9fdc3-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9fdc3-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="9fdc3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9fdc3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9fdc3-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="9fdc3-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="9fdc3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9fdc3-110">Data type:</span></span>  <br/> |<span data-ttu-id="9fdc3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9fdc3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9fdc3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9fdc3-112">Area:</span></span>  <br/> |<span data-ttu-id="9fdc3-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="9fdc3-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fdc3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fdc3-114">Remarks</span></span>

<span data-ttu-id="9fdc3-115">Mindestens eines der folgenden Flags kann für die PR_SUBMIT_FLAGS **festgelegt** werden:</span><span class="sxs-lookup"><span data-stu-id="9fdc3-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="9fdc3-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="9fdc3-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="9fdc3-117">Im MAPI-Spooler ist die Nachricht derzeit gesperrt.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="9fdc3-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="9fdc3-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="9fdc3-119">Die Nachricht muss vorverarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-119">The message needs preprocessing.</span></span> <span data-ttu-id="9fdc3-120">Wenn der MAPI-Spooler diese Nachricht vorverarbeitet hat, sollte er die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="9fdc3-121">Der Nachrichtenspeicheranbieter erkennt, dass der Spooler anstelle der Clientanwendung **SubmitMessage** aufgerufen hat, das Flag entfernt und die Nachrichtenübermittlung fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9fdc3-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9fdc3-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9fdc3-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9fdc3-123">Protocol specifications</span></span>

<span data-ttu-id="9fdc3-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fdc3-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fdc3-125">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9fdc3-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fdc3-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fdc3-127">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9fdc3-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9fdc3-128">Header files</span></span>

<span data-ttu-id="9fdc3-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9fdc3-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="9fdc3-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="9fdc3-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9fdc3-131">Mapitags.h</span></span>
  
> <span data-ttu-id="9fdc3-132">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9fdc3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fdc3-133">See also</span></span>



[<span data-ttu-id="9fdc3-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="9fdc3-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="9fdc3-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9fdc3-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9fdc3-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9fdc3-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9fdc3-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9fdc3-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9fdc3-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9fdc3-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

