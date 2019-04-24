---
title: Kanonische Pidtagcontrolflags (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331864"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="e9827-103">Kanonische Pidtagcontrolflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e9827-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e9827-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9827-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9827-105">Enthält eine Bitmaske von Flags, die das Verhalten eines Steuerelements steuern, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9827-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9827-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e9827-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9827-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e9827-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e9827-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e9827-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9827-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="e9827-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="e9827-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e9827-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9827-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e9827-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e9827-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e9827-112">Area:</span></span>  <br/> |<span data-ttu-id="e9827-113">MAPI-Anzeigetabelle</span><span class="sxs-lookup"><span data-stu-id="e9827-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9827-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9827-114">Remarks</span></span>

<span data-ttu-id="e9827-115">Mindestens eines der folgenden Flags kann für diese Eigenschaft festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e9827-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="e9827-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="e9827-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="e9827-117">Das Steuerelement kann Double-Byte Character Set (DBCS)-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9827-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="e9827-118">Dieses Flag wird mit Bearbeitungssteuerelementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9827-118">This flag is used with edit controls.</span></span> <span data-ttu-id="e9827-119">Es ermöglicht mehr Byte-Zeichensätze.</span><span class="sxs-lookup"><span data-stu-id="e9827-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="e9827-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="e9827-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="e9827-121">Das Steuerelement kann bearbeitet werden; der Wert, der dem Steuerelement zugeordnet ist, kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e9827-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="e9827-122">Wenn dieses Flag nicht festgelegt ist, ist das Steuerelement schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e9827-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="e9827-123">Dieser Wert wird bei Bezeichnung, Gruppenfeld, Standard-Schaltflächen, mehrwertigen Dropdown-Listenfeldern und Listenfeld-Steuerelementen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e9827-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="e9827-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="e9827-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="e9827-125">Das Bearbeitungssteuerelement kann mehrere Zeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9827-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="e9827-126">Dies gibt an, dass ein Rückgabe Zeichen innerhalb des Steuerelements eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9827-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="e9827-127">Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="e9827-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="e9827-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="e9827-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="e9827-129">Gilt für Bearbeitungssteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e9827-129">Applies to edit controls.</span></span> <span data-ttu-id="e9827-130">Das Bearbeitungssteuerelement wird wie ein Kennwort behandelt.</span><span class="sxs-lookup"><span data-stu-id="e9827-130">The edit control is treated like a password.</span></span> <span data-ttu-id="e9827-131">Der Wert wird mit Sternchen angezeigt, statt die eingegebenen tatsächlichen Zeichen wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="e9827-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="e9827-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="e9827-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="e9827-133">Wenn das Steuerelementänderungen (DT_EDITABLE) zulässt, muss es einen Wert aufweisen, bevor [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e9827-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="e9827-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="e9827-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="e9827-135">Ermöglicht die sofortige Einstellung eines Werts; Sobald ein Wert im Steuerelement geändert wird, ruft MAPI die setProps-Methode für die Eigenschaft auf, die diesem Steuerelement zugeordnet ist. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e9827-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="e9827-136">Wenn dieses Flag nicht festgelegt ist, werden die Werte festgelegt, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e9827-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="e9827-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="e9827-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="e9827-138">Wenn im Listenfeld eine Auswahl vorgenommen wird, wird die Indexspalte des Listenfelds als Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e9827-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="e9827-139">Wird immer mit DT_SET_IMMEDIATE verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9827-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="e9827-140">Diese Eigenschaft wird im ulCtlFlags-Element der [DTCTL](dtctl.md) -Struktur eines Steuerelements gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e9827-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="e9827-141">Die meisten der Steuerelement-Flags gelten für alle Steuerelemente, die Benutzereingaben zulassen; einige wenige gelten nur für das Bearbeitungssteuerelement.</span><span class="sxs-lookup"><span data-stu-id="e9827-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="e9827-142">Steuerelemente, die keine Benutzereingabe zulassen, beispielsweise eine Schaltfläche oder eine Bezeichnung, legen 0 für Ihre Steuerelement-Flags fest.</span><span class="sxs-lookup"><span data-stu-id="e9827-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="e9827-143">Viele der Flags-Werte sind selbsterklärend.</span><span class="sxs-lookup"><span data-stu-id="e9827-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="e9827-144">Wenn DT_REQUIRED beispielsweise für ein Steuerelement festgelegt ist, muss es einen Wert enthalten, bevor das Dialogfeld geschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9827-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="e9827-145">Entweder kann der Dienstanbieter einen Wert über die **IMAPIProp** -Implementierung angeben, oder der Benutzer kann eine eingeben.</span><span class="sxs-lookup"><span data-stu-id="e9827-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="e9827-146">DT_EDITABLE gibt an, dass der Wert für das Steuerelement geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9827-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="e9827-147">DT_MULTILINE ermöglicht, dass der Wert für ein Bearbeitungssteuerelement mehrere Zeilen umfasst.</span><span class="sxs-lookup"><span data-stu-id="e9827-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="e9827-148">Einige Steuerelement-Flags sind nicht so offensichtlich.</span><span class="sxs-lookup"><span data-stu-id="e9827-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="e9827-149">Wenn ein Steuerelement das DT_SET_IMMEDIATE-Flag festlegt, wirken sich Änderungen an seinem Wert ab, sobald der Benutzer zu einem neuen Steuerelement wechselt.</span><span class="sxs-lookup"><span data-stu-id="e9827-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="e9827-150">MAPI führt einen einzelnen Aufruf der [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Property-Schnittstelle für die Eigenschaft des Steuerelements aus.</span><span class="sxs-lookup"><span data-stu-id="e9827-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="e9827-151">Dies unterscheidet sich vom Standardverhalten, das bedeutet, dass Änderungen an den Steuerelementwerten erst wirksam werden, wenn der Benutzer die Schaltfläche **OK** auswählt oder das Dialogfeld abschließt.</span><span class="sxs-lookup"><span data-stu-id="e9827-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="e9827-152">Das DT_SET_IMMEDIATE-Flag wird häufig in Kombination mit Anzeige Tabellen Benachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9827-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="e9827-153">In der folgenden Tabelle werden die Typen von Steuerelementen und alle Flagwerte aufgelistet, die für jeden Typ festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="e9827-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="e9827-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="e9827-154">**Control**</span></span>|<span data-ttu-id="e9827-155">**Gültige Werte für diese Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="e9827-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9827-156">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="e9827-156">Button</span></span>  <br/> |<span data-ttu-id="e9827-157">Muss NULL sein</span><span class="sxs-lookup"><span data-stu-id="e9827-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e9827-158">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="e9827-158">Check box</span></span>  <br/> |<span data-ttu-id="e9827-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="e9827-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="e9827-160">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="e9827-160">Combo box</span></span>  <br/> |<span data-ttu-id="e9827-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="e9827-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="e9827-162">Dropdown-Listenfeld</span><span class="sxs-lookup"><span data-stu-id="e9827-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="e9827-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="e9827-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="e9827-164">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="e9827-164">Edit</span></span>  <br/> |<span data-ttu-id="e9827-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="e9827-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="e9827-166">Gruppenfeld</span><span class="sxs-lookup"><span data-stu-id="e9827-166">Group box</span></span>  <br/> |<span data-ttu-id="e9827-167">Muss NULL sein</span><span class="sxs-lookup"><span data-stu-id="e9827-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e9827-168">Label</span><span class="sxs-lookup"><span data-stu-id="e9827-168">Label</span></span>  <br/> |<span data-ttu-id="e9827-169">Muss NULL sein</span><span class="sxs-lookup"><span data-stu-id="e9827-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e9827-170">Listenfeld</span><span class="sxs-lookup"><span data-stu-id="e9827-170">List box</span></span>  <br/> |<span data-ttu-id="e9827-171">Muss NULL sein</span><span class="sxs-lookup"><span data-stu-id="e9827-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e9827-172">MehrWertiges Dropdown-Listenfeld</span><span class="sxs-lookup"><span data-stu-id="e9827-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="e9827-173">Muss NULL sein</span><span class="sxs-lookup"><span data-stu-id="e9827-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e9827-174">MehrWertiges Listenfeld</span><span class="sxs-lookup"><span data-stu-id="e9827-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="e9827-175">Muss NULL sein</span><span class="sxs-lookup"><span data-stu-id="e9827-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e9827-176">Registerkartenseite</span><span class="sxs-lookup"><span data-stu-id="e9827-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="e9827-177">Muss NULL sein</span><span class="sxs-lookup"><span data-stu-id="e9827-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e9827-178">Optionsfeld</span><span class="sxs-lookup"><span data-stu-id="e9827-178">Radio button</span></span>  <br/> |<span data-ttu-id="e9827-179">Muss NULL sein</span><span class="sxs-lookup"><span data-stu-id="e9827-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e9827-180">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e9827-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e9827-181">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e9827-181">Header files</span></span>

<span data-ttu-id="e9827-182">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e9827-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9827-183">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e9827-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9827-184">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e9827-184">Mapitags.h</span></span>
  
> <span data-ttu-id="e9827-185">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e9827-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9827-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9827-186">See also</span></span>



[<span data-ttu-id="e9827-187">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9827-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9827-188">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9827-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9827-189">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e9827-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9827-190">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e9827-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

