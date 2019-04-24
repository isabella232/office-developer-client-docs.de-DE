---
title: Kanonische Pidtagcontrolid (-Eigenschaft
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
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334741"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="359eb-103">Kanonische Pidtagcontrolid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="359eb-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="359eb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="359eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="359eb-105">Enthält einen eindeutigen Bezeichner für ein Steuerelement, das in einem Dialogfeldverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="359eb-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="359eb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="359eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="359eb-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="359eb-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="359eb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="359eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="359eb-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="359eb-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="359eb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="359eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="359eb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="359eb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="359eb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="359eb-112">Area:</span></span>  <br/> |<span data-ttu-id="359eb-113">MAPI-Anzeigetabelle</span><span class="sxs-lookup"><span data-stu-id="359eb-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="359eb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="359eb-114">Remarks</span></span>

<span data-ttu-id="359eb-115">Diese Eigenschaft enthält einen eindeutigen Bezeichner für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="359eb-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="359eb-116">Dieser Bezeichner sollte eine [GUID](guid.md) -Struktur und einen Binary-Wert vom Typ **Long**enthalten.</span><span class="sxs-lookup"><span data-stu-id="359eb-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="359eb-117">Alle Steuerelemente im Dialogfeld sollten dieselbe **GUID** verwenden, um den Dienstanbieter zu identifizieren, und jedes Steuerelement sollte einen eindeutigen **Long** -Wert verwenden, um sicherzustellen, dass die Steuerelemente nicht kollidieren.</span><span class="sxs-lookup"><span data-stu-id="359eb-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="359eb-118">Diese Eigenschaft wird in Benachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="359eb-118">This property is used in notifications.</span></span> <span data-ttu-id="359eb-119">Benachrichtigungen, die in der Anzeigetabelle gesendet werden, müssen beispielsweise diese Eigenschaft festlegen, um das zu aktualisierende Steuerelement eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="359eb-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="359eb-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="359eb-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="359eb-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="359eb-121">Header files</span></span>

<span data-ttu-id="359eb-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="359eb-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="359eb-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="359eb-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="359eb-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="359eb-124">Mapitags.h</span></span>
  
> <span data-ttu-id="359eb-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="359eb-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="359eb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="359eb-126">See also</span></span>



[<span data-ttu-id="359eb-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="359eb-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="359eb-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="359eb-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="359eb-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="359eb-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="359eb-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="359eb-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

