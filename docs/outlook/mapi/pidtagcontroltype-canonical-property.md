---
title: PidTagControlType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734203"
---
# <a name="pidtagcontroltype-canonical-property"></a><span data-ttu-id="9ba92-103">PidTagControlType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9ba92-103">PidTagControlType Canonical Property</span></span>

  
  
<span data-ttu-id="9ba92-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ba92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ba92-105">Enthält einen Wert, der einen Steuerelementtyp für ein Steuerelement angibt, das in einem Dialogfeld verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ba92-105">Contains a value indicating a control type for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ba92-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9ba92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ba92-107">PR_CONTROL_TYPE</span><span class="sxs-lookup"><span data-stu-id="9ba92-107">PR_CONTROL_TYPE</span></span>  <br/> |
|<span data-ttu-id="9ba92-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9ba92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ba92-109">0x3F02</span><span class="sxs-lookup"><span data-stu-id="9ba92-109">0x3F02</span></span>  <br/> |
|<span data-ttu-id="9ba92-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9ba92-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ba92-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9ba92-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9ba92-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9ba92-112">Area:</span></span>  <br/> |<span data-ttu-id="9ba92-113">MAPI-Anzeigetabelle</span><span class="sxs-lookup"><span data-stu-id="9ba92-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ba92-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ba92-114">Remarks</span></span>

<span data-ttu-id="9ba92-115">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="9ba92-115">This property can have exactly one of the following values:</span></span>
    
<span data-ttu-id="9ba92-116">DTCT_LABEL (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="9ba92-116">DTCT_LABEL (0x00000000)</span></span>
  
> <span data-ttu-id="9ba92-117">Eine Dialogbeschriftung.</span><span class="sxs-lookup"><span data-stu-id="9ba92-117">A dialog label.</span></span>
   
<span data-ttu-id="9ba92-118">DTCT_EDIT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9ba92-118">DTCT_EDIT (0x00000001)</span></span>
  
> <span data-ttu-id="9ba92-119">Ein Dialogfeld Bearbeiten eines Textfelds.</span><span class="sxs-lookup"><span data-stu-id="9ba92-119">A dialog edit text box.</span></span>

<span data-ttu-id="9ba92-120">DTCT_LBX (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9ba92-120">DTCT_LBX (0x00000002)</span></span>
  
> <span data-ttu-id="9ba92-121">Ein Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9ba92-121">A dialog list box.</span></span>
    
<span data-ttu-id="9ba92-122">DTCT_COMBOBOX (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="9ba92-122">DTCT_COMBOBOX (0x00000003)</span></span>
  
> <span data-ttu-id="9ba92-123">Ein Dialogfeld-Kombinationsfeld.</span><span class="sxs-lookup"><span data-stu-id="9ba92-123">A dialog combo box.</span></span>

<span data-ttu-id="9ba92-124">DTCT_DDLBX (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="9ba92-124">DTCT_DDLBX (0x00000004)</span></span>
  
> <span data-ttu-id="9ba92-125">Ein Dropdownlistenfeld des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="9ba92-125">A dialog drop-down list box.</span></span>

<span data-ttu-id="9ba92-126">DTCT_CHECKBOX (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="9ba92-126">DTCT_CHECKBOX (0x00000005)</span></span>
  
> <span data-ttu-id="9ba92-127">Ein Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9ba92-127">A dialog check box.</span></span>

<span data-ttu-id="9ba92-128">DTCT_GROUPBOX (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="9ba92-128">DTCT_GROUPBOX (0x00000006)</span></span>
  
> <span data-ttu-id="9ba92-129">Ein Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9ba92-129">A dialog group box.</span></span>
  
<span data-ttu-id="9ba92-130">DTCT_BUTTON (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="9ba92-130">DTCT_BUTTON (0x00000007)</span></span>
  
> <span data-ttu-id="9ba92-131">Ein Dialogfeldschaltfläche-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9ba92-131">A dialog button control.</span></span>
    
<span data-ttu-id="9ba92-132">DTCT_PAGE (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="9ba92-132">DTCT_PAGE (0x00000008)</span></span>
  
> <span data-ttu-id="9ba92-133">Eine Seite mit Registerkarten im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9ba92-133">A dialog tabbed page.</span></span>
    
<span data-ttu-id="9ba92-134">DTCT_RADIOBUTTON (0x00000009)</span><span class="sxs-lookup"><span data-stu-id="9ba92-134">DTCT_RADIOBUTTON (0x00000009)</span></span>
  
> <span data-ttu-id="9ba92-135">Ein Dialogfeld-Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="9ba92-135">A dialog radio button.</span></span>
    
<span data-ttu-id="9ba92-136">DTCT_MVLISTBOX (0x0000000B)</span><span class="sxs-lookup"><span data-stu-id="9ba92-136">DTCT_MVLISTBOX (0x0000000B)</span></span>
  
> <span data-ttu-id="9ba92-137">Ein mehrwertiges Listenfeld, das von einer mehrwertigen Eigenschaft vom Typ string aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="9ba92-137">A multivalued list box populated by a multivalued property of type string.</span></span>
    
<span data-ttu-id="9ba92-138">DTCT_MVDDLBX (0x0000000C)</span><span class="sxs-lookup"><span data-stu-id="9ba92-138">DTCT_MVDDLBX (0x0000000C)</span></span>
  
> <span data-ttu-id="9ba92-139">Ein mehrwertiges Dropdownlistenfeld, das von einer mehrwertigen Eigenschaft vom Typ string aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="9ba92-139">A multivalued drop-down list box populated by a multivalued property of type string.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9ba92-140">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9ba92-140">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9ba92-141">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9ba92-141">Header files</span></span>

<span data-ttu-id="9ba92-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ba92-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ba92-143">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9ba92-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ba92-144">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ba92-144">mapitags.h</span></span>
  
> <span data-ttu-id="9ba92-145">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9ba92-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ba92-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ba92-146">See also</span></span>



[<span data-ttu-id="9ba92-147">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ba92-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ba92-148">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9ba92-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ba92-149">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9ba92-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ba92-150">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9ba92-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

