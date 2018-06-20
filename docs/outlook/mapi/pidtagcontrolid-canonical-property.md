---
title: Kanonische PidTagControlId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 799f83b397cbef9d7dcb6c9a88154b88afe35675
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19794255"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="6d2a0-103">Kanonische PidTagControlId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d2a0-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="6d2a0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d2a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d2a0-105">Enthält einen eindeutigen Bezeichner für ein Steuerelement in einem Dialogfeld verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d2a0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6d2a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d2a0-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="6d2a0-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="6d2a0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6d2a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d2a0-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="6d2a0-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="6d2a0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6d2a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d2a0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6d2a0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6d2a0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6d2a0-112">Area:</span></span>  <br/> |<span data-ttu-id="6d2a0-113">Zeigt die MAPI-Tabelle</span><span class="sxs-lookup"><span data-stu-id="6d2a0-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d2a0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6d2a0-114">Remarks</span></span>

<span data-ttu-id="6d2a0-115">Diese Eigenschaft enthält einen eindeutigen Bezeichner für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="6d2a0-116">Dieser Bezeichner sollte eine [GUID](guid.md) -Struktur und den Wert vom Typ **LONG**binary enthalten.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="6d2a0-117">Alle Steuerelemente im Dialogfeld sollte dieselbe **GUID** zum Identifizieren des Dienstanbieters verwenden, und jedes Steuerelement sollte eine eindeutige verwenden **LONG** -Wert, um sicherzustellen, dass die Steuerelemente nicht kollidieren.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="6d2a0-118">Diese Eigenschaft wird in Benachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-118">This property is used in notifications.</span></span> <span data-ttu-id="6d2a0-119">Senden von Benachrichtigungen für die Anzeige-Tabelle müssen beispielsweise zur eindeutigen Identifizierung des Steuerelements so aktualisieren Sie diese Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6d2a0-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6d2a0-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6d2a0-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6d2a0-121">Header files</span></span>

<span data-ttu-id="6d2a0-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d2a0-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d2a0-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d2a0-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d2a0-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6d2a0-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d2a0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d2a0-126">See also</span></span>



[<span data-ttu-id="6d2a0-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d2a0-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d2a0-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d2a0-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d2a0-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6d2a0-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d2a0-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6d2a0-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

