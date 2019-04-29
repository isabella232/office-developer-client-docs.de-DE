---
title: Kanonische Pidtagorigincheck (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435761"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="cab34-103">Kanonische Pidtagorigincheck (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cab34-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="cab34-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cab34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cab34-105">Enthält einen binären Überprüfungs Wert, der es einem Zustellungs Berichtsempfänger ermöglicht, den Ursprung der ursprünglichen Nachricht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cab34-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cab34-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cab34-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cab34-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="cab34-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="cab34-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cab34-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cab34-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="cab34-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="cab34-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cab34-110">Data type:</span></span>  <br/> |<span data-ttu-id="cab34-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cab34-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cab34-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cab34-112">Area:</span></span>  <br/> |<span data-ttu-id="cab34-113">Server</span><span class="sxs-lookup"><span data-stu-id="cab34-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cab34-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cab34-114">Remarks</span></span>

<span data-ttu-id="cab34-115">Diese Eigenschaft bietet einem Drittanbieter, beispielsweise einem MTA (Message Transfer Agent) oder einem Messagingbenutzer, der einen Zustellungsbericht empfängt, die Möglichkeit, den Ursprung der übermittelten Nachricht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cab34-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="cab34-116">Wenn diese Eigenschaft für eine empfangene Nachricht vorhanden ist, sollte Sie in einen beliebigen Übermittlungsbericht kopiert werden, der als Antwort auf die Nachricht generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cab34-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cab34-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cab34-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cab34-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cab34-118">Header files</span></span>

<span data-ttu-id="cab34-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cab34-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cab34-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cab34-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cab34-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cab34-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cab34-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="cab34-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cab34-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cab34-123">See also</span></span>



[<span data-ttu-id="cab34-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cab34-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cab34-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cab34-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cab34-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cab34-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cab34-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cab34-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

