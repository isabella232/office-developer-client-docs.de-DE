---
title: PidTagControlId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416020"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="8a4af-103">PidTagControlId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8a4af-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="8a4af-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a4af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a4af-105">Enthält einen eindeutigen Bezeichner für ein Steuerelement, das in einem Dialogfeld verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a4af-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a4af-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8a4af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a4af-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="8a4af-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="8a4af-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8a4af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a4af-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="8a4af-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="8a4af-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8a4af-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a4af-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a4af-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a4af-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8a4af-112">Area:</span></span>  <br/> |<span data-ttu-id="8a4af-113">MAPI-Anzeigetabelle</span><span class="sxs-lookup"><span data-stu-id="8a4af-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a4af-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8a4af-114">Remarks</span></span>

<span data-ttu-id="8a4af-115">Diese Eigenschaft enthält einen eindeutigen Bezeichner für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8a4af-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="8a4af-116">Dieser Bezeichner sollte eine [GUID-Struktur](guid.md) und einen binären Wert vom Typ **LONG enthalten.**</span><span class="sxs-lookup"><span data-stu-id="8a4af-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="8a4af-117">Alle Steuerelemente im Dialogfeld sollten dieselbe **GUID** verwenden, um den Dienstanbieter zu identifizieren, und jedes Steuerelement sollte einen eindeutigen **LONG-Wert** verwenden, um sicherzustellen, dass die Steuerelemente nicht kollidieren.</span><span class="sxs-lookup"><span data-stu-id="8a4af-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="8a4af-118">Diese Eigenschaft wird in Benachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a4af-118">This property is used in notifications.</span></span> <span data-ttu-id="8a4af-119">Beispielsweise müssen in der Anzeigetabelle gesendete Benachrichtigungen diese Eigenschaft so festlegen, dass das zu aktualisierende Steuerelement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8a4af-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8a4af-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8a4af-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8a4af-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8a4af-121">Header files</span></span>

<span data-ttu-id="8a4af-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a4af-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a4af-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a4af-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a4af-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8a4af-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8a4af-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a4af-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a4af-126">See also</span></span>



[<span data-ttu-id="8a4af-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8a4af-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a4af-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8a4af-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a4af-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8a4af-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a4af-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8a4af-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

