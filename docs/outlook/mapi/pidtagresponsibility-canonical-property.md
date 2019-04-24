---
title: Kanonische Pidtagresponsibility (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330121"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="5e482-103">Kanonische Pidtagresponsibility (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5e482-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="5e482-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e482-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e482-105">Enthält TRUE, wenn ein Transportanbieter bereits die Verantwortung für die Zustellung der Nachricht an diesen Empfänger übernommen hat, und FALSE, wenn der MAPI-Spooler der Ansicht ist, dass dieser Transportanbieter die Verantwortung übernehmen soll.</span><span class="sxs-lookup"><span data-stu-id="5e482-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e482-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5e482-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e482-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="5e482-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="5e482-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5e482-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e482-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="5e482-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="5e482-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5e482-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e482-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5e482-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5e482-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5e482-112">Area:</span></span>  <br/> |<span data-ttu-id="5e482-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="5e482-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e482-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e482-114">Remarks</span></span>

<span data-ttu-id="5e482-115">Wenn der MAPI-Spooler eine ausgehende Nachricht an einen Transportanbieter über [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), wird diese Eigenschaft auf false für alle Empfänger festgelegt, für die der MAPI-Spooler der Ansicht ist, dass der Transportanbieter zuständig ist, und true für alle andere Empfänger.</span><span class="sxs-lookup"><span data-stu-id="5e482-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="5e482-116">Der Transportanbieter sollte versuchen, alle Empfänger zu behandeln, bei denen **PR_RESPONSIBILITY** auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5e482-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="5e482-117">Nach dem erfolgreichen senden oder ausschließenden Senden eines Empfängers durch den Transportanbieter sollte diese Eigenschaft in der Quellnachricht auf TRUE festgelegt werden, um anzugeben, dass Sie die Verantwortung für diesen Empfänger übernommen hat.</span><span class="sxs-lookup"><span data-stu-id="5e482-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="5e482-118">Wenn ein Transportanbieter nach der Untersuchung eines Empfängers entscheidet, dass er nicht verarbeitet werden kann oder sollte, sollte **PR_RESPONSIBILITY** auf false festgelegt bleiben.</span><span class="sxs-lookup"><span data-stu-id="5e482-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="5e482-119">Der MAPI-Spooler sucht dann nach einem anderen Transportanbieter, der diesen Empfänger verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="5e482-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="5e482-120">Der MAPI-Spooler erstellt schließlich einen Unzustellbarkeitsbericht für alle Empfänger, für die kein Transportanbieter die Verantwortung übernimmt.</span><span class="sxs-lookup"><span data-stu-id="5e482-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="5e482-121">Wenn der Transportanbieter versucht, die Nachricht zu übermitteln, muss Sie die [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode aufrufen, um MAPI die Gründe für den Fehler anzuzeigen, damit MAPI einen Unzustellbarkeitsbericht generieren kann.</span><span class="sxs-lookup"><span data-stu-id="5e482-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e482-122">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5e482-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e482-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5e482-123">Protocol specifications</span></span>

<span data-ttu-id="5e482-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e482-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e482-125">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5e482-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e482-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e482-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e482-127">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="5e482-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e482-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5e482-128">Header files</span></span>

<span data-ttu-id="5e482-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5e482-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e482-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5e482-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e482-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5e482-131">Mapitags.h</span></span>
  
> <span data-ttu-id="5e482-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5e482-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e482-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e482-133">See also</span></span>



[<span data-ttu-id="5e482-134">Kanonische PidTagDeleteAfterSubmit-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5e482-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="5e482-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e482-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e482-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e482-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e482-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5e482-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e482-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5e482-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

