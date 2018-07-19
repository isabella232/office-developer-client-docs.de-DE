---
title: PidTagOriginCheck (kanonische Eigenschaft)
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
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794745"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="52d53-103">PidTagOriginCheck (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="52d53-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="52d53-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52d53-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52d53-105">Enthält einen binären Überprüfung-Wert, mit der einen Delivery Report Empfänger Ursprung der ursprünglichen Nachricht überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="52d53-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52d53-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="52d53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52d53-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="52d53-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="52d53-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="52d53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52d53-109">0 x 0027</span><span class="sxs-lookup"><span data-stu-id="52d53-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="52d53-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="52d53-110">Data type:</span></span>  <br/> |<span data-ttu-id="52d53-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="52d53-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="52d53-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="52d53-112">Area:</span></span>  <br/> |<span data-ttu-id="52d53-113">Server</span><span class="sxs-lookup"><span data-stu-id="52d53-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52d53-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52d53-114">Remarks</span></span>

<span data-ttu-id="52d53-115">Diese Eigenschaft bietet eine Möglichkeit für ein Drittanbieter, wie ein Message Transfer Agent (MTA) oder ein messaging-Benutzer empfangen eines Unzustellbarkeitsberichts die gesendete Nachricht Origin überprüfen.</span><span class="sxs-lookup"><span data-stu-id="52d53-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="52d53-116">Auf einer empfangenen Nachricht vorhanden sind, sollten diese Eigenschaft auf eine beliebige Übermittlungsbericht generiert, die als Antwort auf die Nachricht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="52d53-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="52d53-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="52d53-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="52d53-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="52d53-118">Header files</span></span>

<span data-ttu-id="52d53-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52d53-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="52d53-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="52d53-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="52d53-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52d53-121">Mapitags.h</span></span>
  
> <span data-ttu-id="52d53-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="52d53-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52d53-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52d53-123">See also</span></span>



[<span data-ttu-id="52d53-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52d53-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52d53-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52d53-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52d53-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="52d53-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52d53-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="52d53-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

