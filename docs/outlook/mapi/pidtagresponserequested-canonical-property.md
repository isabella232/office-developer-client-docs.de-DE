---
title: PidTagResponseRequested (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponseRequested
api_type:
- COM
ms.assetid: e52bb48c-7107-4ac4-b030-885409759ee7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 77c724affd2057ca6347d752323c5ba0a3094ecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330156"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="bc316-103">PidTagResponseRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc316-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="bc316-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc316-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc316-105">Enthält TRUE, wenn der Nachrichtensender eine Antwort auf eine Besprechungsanfrage erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="bc316-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc316-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bc316-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc316-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="bc316-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="bc316-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bc316-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc316-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="bc316-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="bc316-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bc316-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc316-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bc316-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bc316-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bc316-112">Area:</span></span>  <br/> |<span data-ttu-id="bc316-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="bc316-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc316-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc316-114">Remarks</span></span>

<span data-ttu-id="bc316-115">Diese Eigenschaft wird für Besprechungsanfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc316-115">This property is used for meeting requests.</span></span> <span data-ttu-id="bc316-116">Die empfangende Clientanwendung sollte den Benutzer bitten, die Anforderung zu akzeptieren oder zu ablehnen, und diese Antwort dann an den Absender zurücksendet.</span><span class="sxs-lookup"><span data-stu-id="bc316-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc316-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bc316-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc316-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bc316-118">Protocol specifications</span></span>

<span data-ttu-id="bc316-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc316-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc316-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bc316-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc316-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc316-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc316-122">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bc316-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="bc316-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc316-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc316-124">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="bc316-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="bc316-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc316-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc316-126">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="bc316-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc316-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="bc316-127">Header files</span></span>

<span data-ttu-id="bc316-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc316-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc316-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bc316-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc316-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc316-130">Mapitags.h</span></span>
  
> <span data-ttu-id="bc316-131">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bc316-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc316-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc316-132">See also</span></span>



[<span data-ttu-id="bc316-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc316-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc316-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="bc316-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc316-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bc316-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc316-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bc316-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

