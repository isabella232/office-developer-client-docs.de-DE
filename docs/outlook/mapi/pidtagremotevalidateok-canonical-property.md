---
title: Kanonische Pidtagremotevalidateok (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424224"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="b0a19-103">Kanonische Pidtagremotevalidateok (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b0a19-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="b0a19-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0a19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0a19-105">Diese Eigenschaft enthält TRUE, wenn die Remoteanzeige berechtigt ist, die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b0a19-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0a19-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b0a19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0a19-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="b0a19-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="b0a19-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b0a19-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0a19-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="b0a19-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="b0a19-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b0a19-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0a19-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b0a19-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b0a19-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b0a19-112">Area:</span></span>  <br/> |<span data-ttu-id="b0a19-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="b0a19-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0a19-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0a19-114">Remarks</span></span>

<span data-ttu-id="b0a19-115">Diese Eigenschaft wird in der Statustabelle angezeigt und bietet eine gewisse Kontrolle über die Transportleistung.</span><span class="sxs-lookup"><span data-stu-id="b0a19-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="b0a19-116">Er kann als eine andere Möglichkeit angesehen werden, um den Remote Viewer in den Leerlauf zu lenken.</span><span class="sxs-lookup"><span data-stu-id="b0a19-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="b0a19-117">Wenn Sie auf TRUE festgelegt ist, kann die Remoteanzeige **IMAPIStatus:: ValidateState** so oft wie gewünscht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b0a19-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="b0a19-118">Der Wert FALSE gibt an, dass die Remoteanzeige keine weiteren Anrufe tätigen kann.</span><span class="sxs-lookup"><span data-stu-id="b0a19-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="b0a19-119">Der Transportanbieter legt diese Eigenschaft normalerweise dynamisch fest, indem der Wert auf FALSE festgelegt wird, um zusätzliche Aufrufe zu deaktivieren, wenn der Transportanbieter über ausreichend Verarbeitungsleistung verfügt.</span><span class="sxs-lookup"><span data-stu-id="b0a19-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="b0a19-120">Wenn der Transportanbieter fertig ist, wird der Wert auf TRUE festgelegt, damit die Clientanwendung weitere **IMAPIStatus:: ValidateState** -Aufrufe durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="b0a19-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b0a19-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b0a19-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b0a19-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b0a19-122">Header files</span></span>

<span data-ttu-id="b0a19-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b0a19-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0a19-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b0a19-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0a19-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b0a19-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b0a19-126">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="b0a19-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0a19-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0a19-127">See also</span></span>



[<span data-ttu-id="b0a19-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0a19-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0a19-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0a19-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0a19-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b0a19-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0a19-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b0a19-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

