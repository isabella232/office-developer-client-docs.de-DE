---
title: PidTagControlFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430882"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="b28fb-103">PidTagControlFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b28fb-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="b28fb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b28fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b28fb-105">Enthält eine Bitmaske mit Flags, die das Verhalten eines Steuerelements steuern, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b28fb-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b28fb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b28fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b28fb-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="b28fb-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="b28fb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b28fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b28fb-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="b28fb-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="b28fb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b28fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="b28fb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b28fb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b28fb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b28fb-112">Area:</span></span>  <br/> |<span data-ttu-id="b28fb-113">MAPI-Anzeigetabelle</span><span class="sxs-lookup"><span data-stu-id="b28fb-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b28fb-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b28fb-114">Remarks</span></span>

<span data-ttu-id="b28fb-115">Mindestens eines der folgenden Kennzeichen kann für diese Eigenschaft festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b28fb-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="b28fb-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="b28fb-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="b28fb-117">Das Steuerelement kann Double-Byte Zeichensatz (Character Set, DBCS) enthalten.</span><span class="sxs-lookup"><span data-stu-id="b28fb-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="b28fb-118">Dieses Flag wird mit Bearbeitungssteuerelementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b28fb-118">This flag is used with edit controls.</span></span> <span data-ttu-id="b28fb-119">Sie ermöglicht Mehrere-Byte-Zeichensätze.</span><span class="sxs-lookup"><span data-stu-id="b28fb-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="b28fb-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="b28fb-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="b28fb-121">Das Steuerelement kann bearbeitet werden. der dem Steuerelement zugeordnete Wert kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b28fb-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="b28fb-122">Wenn dieses Flag nicht festgelegt ist, ist das Steuerelement schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b28fb-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="b28fb-123">Dieser Wert wird für Bezeichnungs-, Gruppenfeld-, Standard-Pushschaltfläche, mehrwertige Dropdownlistenfeld- und Listenfeldsteuerelemente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b28fb-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="b28fb-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="b28fb-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="b28fb-125">Das Bearbeitungssteuerelement kann mehrere Zeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b28fb-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="b28fb-126">Dies bedeutet, dass innerhalb des Steuerelements ein Rückgabezeichen eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b28fb-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="b28fb-127">Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="b28fb-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="b28fb-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="b28fb-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="b28fb-129">Gilt für Bearbeitungssteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="b28fb-129">Applies to edit controls.</span></span> <span data-ttu-id="b28fb-130">Das Bearbeitungssteuerelement wird wie ein Kennwort behandelt.</span><span class="sxs-lookup"><span data-stu-id="b28fb-130">The edit control is treated like a password.</span></span> <span data-ttu-id="b28fb-131">Der Wert wird mithilfe von Sternchen angezeigt, anstatt die tatsächlich eingegebenen Zeichen zu echosen.</span><span class="sxs-lookup"><span data-stu-id="b28fb-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="b28fb-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="b28fb-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="b28fb-133">Wenn das Steuerelement Änderungen zulässt (DT_EDITABLE), muss es einen Wert haben, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b28fb-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="b28fb-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="b28fb-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="b28fb-135">Ermöglicht das sofortige Festlegen eines Werts. Sobald sich ein Wert im Steuerelement ändert, ruft MAPI die **SetProps-Methode** für die diesem Steuerelement zugeordnete Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="b28fb-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="b28fb-136">Wenn dieses Flag nicht festgelegt ist, werden die Werte festgelegt, wenn das Dialogfeld nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b28fb-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="b28fb-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="b28fb-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="b28fb-138">Wenn innerhalb des Listenfelds eine Auswahl getroffen wird, wird die Indexspalte dieses Listenfelds als Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b28fb-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="b28fb-139">Wird immer mit DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="b28fb-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="b28fb-140">Diese Eigenschaft wird im ulCtlFlags-Element der [DTCTL-Struktur](dtctl.md) eines Steuerelements gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b28fb-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="b28fb-141">Die meisten Steuerelementflags gelten für alle Steuerelemente, die Benutzereingaben zulassen. einige gelten nur für das Bearbeitungssteuerelement.</span><span class="sxs-lookup"><span data-stu-id="b28fb-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="b28fb-142">Steuerelemente, die keine Benutzereingaben zulassen, z. B. eine Schaltfläche oder eine Bezeichnung, legen 0 für ihre Steuerelementflags fest.</span><span class="sxs-lookup"><span data-stu-id="b28fb-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="b28fb-143">Viele der Kennzeichenwerte sind selbsterklärend.</span><span class="sxs-lookup"><span data-stu-id="b28fb-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="b28fb-144">Wenn z. B. DT_REQUIRED für ein Steuerelement festgelegt ist, muss es einen Wert enthalten, bevor das Dialogfeld verworfen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b28fb-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="b28fb-145">Entweder kann der Dienstanbieter einen Wert über seine **IMAPIProp-Implementierung** liefern, oder der Benutzer kann einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="b28fb-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="b28fb-146">DT_EDITABLE gibt an, dass der Wert für das Steuerelement geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b28fb-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="b28fb-147">DT_MULTILINE kann der Wert für ein Bearbeitungssteuerelement mehrere Zeilen umfassen.</span><span class="sxs-lookup"><span data-stu-id="b28fb-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="b28fb-148">Einige Steuerelementflags sind in ihrer Bedeutung nicht so offensichtlich.</span><span class="sxs-lookup"><span data-stu-id="b28fb-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="b28fb-149">Wenn ein Steuerelement das DT_SET_IMMEDIATE, wirken sich alle Änderungen an seinem Wert aus, sobald der Benutzer zu einem neuen Steuerelement wechselt.</span><span class="sxs-lookup"><span data-stu-id="b28fb-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="b28fb-150">MAPI macht einen einzelnen Aufruf der [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Eigenschaft des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="b28fb-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="b28fb-151">Dies ist anders als das Standardverhalten, bei dem Änderungen an Steuerelementwerten erst wirksam werden, wenn der Benutzer die Schaltfläche **OK** auswählt oder das Dialogfeld schließt.</span><span class="sxs-lookup"><span data-stu-id="b28fb-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="b28fb-152">Das DT_SET_IMMEDIATE wird häufig in Kombination mit Anzeigetabelle Benachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b28fb-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="b28fb-153">In der folgenden Tabelle sind die Typen von Steuerelementen und alle Kennzeichenwerte aufgeführt, die für jeden Typ festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="b28fb-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="b28fb-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="b28fb-154">**Control**</span></span>|<span data-ttu-id="b28fb-155">**Gültige Werte für diese Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="b28fb-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b28fb-156">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="b28fb-156">Button</span></span>  <br/> |<span data-ttu-id="b28fb-157">Muss null sein</span><span class="sxs-lookup"><span data-stu-id="b28fb-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="b28fb-158">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="b28fb-158">Check box</span></span>  <br/> |<span data-ttu-id="b28fb-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="b28fb-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="b28fb-160">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="b28fb-160">Combo box</span></span>  <br/> |<span data-ttu-id="b28fb-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="b28fb-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="b28fb-162">Dropdownlistenfeld</span><span class="sxs-lookup"><span data-stu-id="b28fb-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="b28fb-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="b28fb-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="b28fb-164">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="b28fb-164">Edit</span></span>  <br/> |<span data-ttu-id="b28fb-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="b28fb-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="b28fb-166">Gruppenfeld</span><span class="sxs-lookup"><span data-stu-id="b28fb-166">Group box</span></span>  <br/> |<span data-ttu-id="b28fb-167">Muss null sein</span><span class="sxs-lookup"><span data-stu-id="b28fb-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="b28fb-168">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="b28fb-168">Label</span></span>  <br/> |<span data-ttu-id="b28fb-169">Muss null sein</span><span class="sxs-lookup"><span data-stu-id="b28fb-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="b28fb-170">Listenfeld</span><span class="sxs-lookup"><span data-stu-id="b28fb-170">List box</span></span>  <br/> |<span data-ttu-id="b28fb-171">Muss null sein</span><span class="sxs-lookup"><span data-stu-id="b28fb-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="b28fb-172">Dropdownlistenfeld für mehrwertige Werte</span><span class="sxs-lookup"><span data-stu-id="b28fb-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="b28fb-173">Muss null sein</span><span class="sxs-lookup"><span data-stu-id="b28fb-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="b28fb-174">Listenfeld mit mehreren Bewertungswerten</span><span class="sxs-lookup"><span data-stu-id="b28fb-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="b28fb-175">Muss null sein</span><span class="sxs-lookup"><span data-stu-id="b28fb-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="b28fb-176">Registerkartenseite</span><span class="sxs-lookup"><span data-stu-id="b28fb-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="b28fb-177">Muss null sein</span><span class="sxs-lookup"><span data-stu-id="b28fb-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="b28fb-178">Optionsfeld</span><span class="sxs-lookup"><span data-stu-id="b28fb-178">Radio button</span></span>  <br/> |<span data-ttu-id="b28fb-179">Muss null sein</span><span class="sxs-lookup"><span data-stu-id="b28fb-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b28fb-180">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b28fb-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b28fb-181">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b28fb-181">Header files</span></span>

<span data-ttu-id="b28fb-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b28fb-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="b28fb-183">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b28fb-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="b28fb-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b28fb-184">Mapitags.h</span></span>
  
> <span data-ttu-id="b28fb-185">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b28fb-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b28fb-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b28fb-186">See also</span></span>



[<span data-ttu-id="b28fb-187">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b28fb-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b28fb-188">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b28fb-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b28fb-189">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b28fb-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b28fb-190">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b28fb-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

