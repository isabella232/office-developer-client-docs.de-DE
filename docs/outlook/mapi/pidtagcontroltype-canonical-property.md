---
title: Kanonische pidtagcontroltype (-Eigenschaft
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
# <a name="pidtagcontroltype-canonical-property"></a><span data-ttu-id="35f4d-103">Kanonische pidtagcontroltype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35f4d-103">PidTagControlType Canonical Property</span></span>

  
  
<span data-ttu-id="35f4d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35f4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35f4d-105">Enthält einen Wert, der einen Steuerelementtyp für ein in einem Dialogfeld verwendetes Steuerelement angibt.</span><span class="sxs-lookup"><span data-stu-id="35f4d-105">Contains a value indicating a control type for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35f4d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="35f4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35f4d-107">PR_CONTROL_TYPE</span><span class="sxs-lookup"><span data-stu-id="35f4d-107">PR_CONTROL_TYPE</span></span>  <br/> |
|<span data-ttu-id="35f4d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="35f4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35f4d-109">0x3F02</span><span class="sxs-lookup"><span data-stu-id="35f4d-109">0x3F02</span></span>  <br/> |
|<span data-ttu-id="35f4d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="35f4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="35f4d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="35f4d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="35f4d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="35f4d-112">Area:</span></span>  <br/> |<span data-ttu-id="35f4d-113">MAPI-Anzeigetabelle</span><span class="sxs-lookup"><span data-stu-id="35f4d-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35f4d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35f4d-114">Remarks</span></span>

<span data-ttu-id="35f4d-115">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="35f4d-115">This property can have exactly one of the following values:</span></span>
    
<span data-ttu-id="35f4d-116">DTCT_LABEL (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="35f4d-116">DTCT_LABEL (0x00000000)</span></span>
  
> <span data-ttu-id="35f4d-117">Eine Dialogfeld Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="35f4d-117">A dialog label.</span></span>
   
<span data-ttu-id="35f4d-118">DTCT_EDIT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="35f4d-118">DTCT_EDIT (0x00000001)</span></span>
  
> <span data-ttu-id="35f4d-119">Ein Dialogfeld Bearbeitungstextfeld.</span><span class="sxs-lookup"><span data-stu-id="35f4d-119">A dialog edit text box.</span></span>

<span data-ttu-id="35f4d-120">DTCT_LBX (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="35f4d-120">DTCT_LBX (0x00000002)</span></span>
  
> <span data-ttu-id="35f4d-121">Dialog-Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="35f4d-121">A dialog list box.</span></span>
    
<span data-ttu-id="35f4d-122">DTCT_COMBOBOX (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="35f4d-122">DTCT_COMBOBOX (0x00000003)</span></span>
  
> <span data-ttu-id="35f4d-123">Ein Dialogfeld-Kombinationsfeld.</span><span class="sxs-lookup"><span data-stu-id="35f4d-123">A dialog combo box.</span></span>

<span data-ttu-id="35f4d-124">DTCT_DDLBX (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="35f4d-124">DTCT_DDLBX (0x00000004)</span></span>
  
> <span data-ttu-id="35f4d-125">Ein Dropdown-Listenfeld für Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="35f4d-125">A dialog drop-down list box.</span></span>

<span data-ttu-id="35f4d-126">DTCT_CHECKBOX (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="35f4d-126">DTCT_CHECKBOX (0x00000005)</span></span>
  
> <span data-ttu-id="35f4d-127">Ein Kontrollkästchen für ein Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="35f4d-127">A dialog check box.</span></span>

<span data-ttu-id="35f4d-128">DTCT_GROUPBOX (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="35f4d-128">DTCT_GROUPBOX (0x00000006)</span></span>
  
> <span data-ttu-id="35f4d-129">Dialoggruppen Feld.</span><span class="sxs-lookup"><span data-stu-id="35f4d-129">A dialog group box.</span></span>
  
<span data-ttu-id="35f4d-130">DTCT_BUTTON (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="35f4d-130">DTCT_BUTTON (0x00000007)</span></span>
  
> <span data-ttu-id="35f4d-131">Ein Dialogfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="35f4d-131">A dialog button control.</span></span>
    
<span data-ttu-id="35f4d-132">DTCT_PAGE (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="35f4d-132">DTCT_PAGE (0x00000008)</span></span>
  
> <span data-ttu-id="35f4d-133">Seite mit Registerkarten im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="35f4d-133">A dialog tabbed page.</span></span>
    
<span data-ttu-id="35f4d-134">DTCT_RADIOBUTTON (0x00000009)</span><span class="sxs-lookup"><span data-stu-id="35f4d-134">DTCT_RADIOBUTTON (0x00000009)</span></span>
  
> <span data-ttu-id="35f4d-135">Optionsfeld "Dialog".</span><span class="sxs-lookup"><span data-stu-id="35f4d-135">A dialog radio button.</span></span>
    
<span data-ttu-id="35f4d-136">DTCT_MVLISTBOX (0x0000000B)</span><span class="sxs-lookup"><span data-stu-id="35f4d-136">DTCT_MVLISTBOX (0x0000000B)</span></span>
  
> <span data-ttu-id="35f4d-137">Ein mehrwertiges Listenfeld, das von einer mehrwertigen Eigenschaft vom Typ String aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="35f4d-137">A multivalued list box populated by a multivalued property of type string.</span></span>
    
<span data-ttu-id="35f4d-138">DTCT_MVDDLBX (0x0000000C)</span><span class="sxs-lookup"><span data-stu-id="35f4d-138">DTCT_MVDDLBX (0x0000000C)</span></span>
  
> <span data-ttu-id="35f4d-139">Ein mehrwertiges Dropdown-Listenfeld, das von einer mehrwertigen Eigenschaft vom Typ String aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="35f4d-139">A multivalued drop-down list box populated by a multivalued property of type string.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="35f4d-140">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35f4d-140">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="35f4d-141">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="35f4d-141">Header files</span></span>

<span data-ttu-id="35f4d-142">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="35f4d-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="35f4d-143">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="35f4d-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="35f4d-144">mapitags. h</span><span class="sxs-lookup"><span data-stu-id="35f4d-144">mapitags.h</span></span>
  
> <span data-ttu-id="35f4d-145">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="35f4d-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35f4d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35f4d-146">See also</span></span>



[<span data-ttu-id="35f4d-147">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35f4d-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35f4d-148">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35f4d-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35f4d-149">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="35f4d-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35f4d-150">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="35f4d-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

