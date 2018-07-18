---
title: PidTagRemoteValidateOk (kanonische Eigenschaft)
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d8d986554352e05398a843723ee802bb4969e5ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794950"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="7a867-103">PidTagRemoteValidateOk (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7a867-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="7a867-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a867-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a867-105">Diese Eigenschaft enthält True, wenn der remote-Viewer zulässig ist, die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a867-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a867-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7a867-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a867-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="7a867-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="7a867-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="7a867-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a867-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="7a867-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="7a867-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7a867-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a867-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7a867-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7a867-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7a867-112">Area:</span></span>  <br/> |<span data-ttu-id="7a867-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="7a867-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a867-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a867-114">Remarks</span></span>

<span data-ttu-id="7a867-115">Diese Eigenschaft wird in der Tabelle "Status" und einige Kontrolle über die Transport Leistung bietet.</span><span class="sxs-lookup"><span data-stu-id="7a867-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="7a867-116">Es kann als eine andere Möglichkeit, leiten den remote Viewer, im Leerlauf betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="7a867-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="7a867-117">Wenn sie auf "true" festgelegt ist, kann die remote-Ansicht so oft wie gewünscht **IMAPIStatus::ValidateState** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a867-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="7a867-118">Der Wert FALSE gibt an, dass keine weitere Aufrufe der remote-Viewer nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a867-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="7a867-119">Der Transportdienst festgelegt, dass in der Regel diese Eigenschaft dynamisch durch Festlegen des Werts auf false fest, um zusätzliche Anrufe deaktivieren, wenn der Adressbuchhierarchie eine ausreichende Menge der Verarbeitung ausführen hat.</span><span class="sxs-lookup"><span data-stu-id="7a867-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="7a867-120">Klicken Sie nach Abschluss der Adressbuchhierarchie wird dann den Wert auf TRUE, um die Clientanwendung auf Weitere **IMAPIStatus::ValidateState** tätigen können.</span><span class="sxs-lookup"><span data-stu-id="7a867-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7a867-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a867-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7a867-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7a867-122">Header files</span></span>

<span data-ttu-id="7a867-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a867-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a867-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7a867-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a867-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a867-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7a867-126">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7a867-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a867-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a867-127">See also</span></span>



[<span data-ttu-id="7a867-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a867-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a867-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a867-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a867-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7a867-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a867-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7a867-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

