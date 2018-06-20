---
title: Kanonische PidTagControlFlags-Eigenschaft
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
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794261"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="a49af-103">Kanonische PidTagControlFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a49af-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a49af-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a49af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a49af-105">Enthält eine Bitmaske aus Flags, die das Verhalten der ein Steuerelement in einem Dialogfeld erstellt aus einer Tabelle anzeigen zum Steuern.</span><span class="sxs-lookup"><span data-stu-id="a49af-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a49af-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a49af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a49af-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a49af-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="a49af-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a49af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a49af-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="a49af-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="a49af-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a49af-110">Data type:</span></span>  <br/> |<span data-ttu-id="a49af-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a49af-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a49af-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a49af-112">Area:</span></span>  <br/> |<span data-ttu-id="a49af-113">Zeigt die MAPI-Tabelle</span><span class="sxs-lookup"><span data-stu-id="a49af-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a49af-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a49af-114">Remarks</span></span>

<span data-ttu-id="a49af-115">Für diese Eigenschaft kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a49af-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="a49af-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="a49af-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="a49af-117">Das Steuerelement kann Double-Byte-Zeichen (DBCS) Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a49af-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="a49af-118">Dieses Kennzeichen werden mit Edit-Steuerelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="a49af-118">This flag is used with edit controls.</span></span> <span data-ttu-id="a49af-119">Es kann mehrere-Byte-Zeichensätze.</span><span class="sxs-lookup"><span data-stu-id="a49af-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="a49af-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="a49af-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="a49af-121">Das Steuerelement bearbeitet werden kann. der Wert mit dem Steuerelement zugeordnet ist, kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a49af-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="a49af-122">Wenn dieses Flag nicht festgelegt ist, ist das Steuerelement schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a49af-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="a49af-123">Dieser Wert wird ignoriert, Label, Gruppenfeld, standard-Taste, mehrwertigen Dropdown-Listenfeld und Listenfeld-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a49af-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="a49af-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="a49af-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="a49af-125">Das Edit-Steuerelement kann mehrere Zeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a49af-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="a49af-126">Dies bedeutet, dass eine Absatzmarke innerhalb des Steuerelements eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a49af-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="a49af-127">Dieses Kennzeichen ist gültig für Bearbeitungssteuerelemente nur.</span><span class="sxs-lookup"><span data-stu-id="a49af-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="a49af-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="a49af-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="a49af-129">Bearbeiten von Steuerelementen gilt.</span><span class="sxs-lookup"><span data-stu-id="a49af-129">Applies to edit controls.</span></span> <span data-ttu-id="a49af-130">Das Edit-Steuerelement wird wie ein Kennwort behandelt.</span><span class="sxs-lookup"><span data-stu-id="a49af-130">The edit control is treated like a password.</span></span> <span data-ttu-id="a49af-131">Der Wert wird unter Verwendung von Sternchen anstelle von Echos die eingegebenen Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a49af-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="a49af-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="a49af-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="a49af-133">Wenn das Steuerelement Änderungen (DT_EDITABLE) zulässt, muss er einen Wert aufweisen, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a49af-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="a49af-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="a49af-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="a49af-135">Ermöglicht die sofortige Festlegen eines Werts. als ein Wert im Steuerelement geändert wird, ruft MAPI die **SetProps** -Methode für die Eigenschaft im Zusammenhang mit diesem Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="a49af-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="a49af-136">Wenn dieses Flag nicht festgelegt ist, werden die Werte festgelegt, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a49af-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="a49af-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="a49af-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="a49af-138">Wenn eine Auswahl innerhalb des Listenfelds erfolgt, wird die Indexspalte, Listenfelds als Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a49af-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="a49af-139">Immer verwendet mit DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="a49af-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="a49af-140">Diese Eigenschaft wird in den UlCtlFlags Member eines Steuerelements [DTCTL](dtctl.md) Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a49af-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="a49af-141">Die meisten die Steuerelement-Kennzeichen gelten für alle Steuerelemente, die von Benutzereingaben zulassen. wenige gelten nur für das Bearbeitungssteuerelement.</span><span class="sxs-lookup"><span data-stu-id="a49af-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="a49af-142">Steuerelemente, die von Benutzereingaben, wie eine Schaltfläche oder eine Beschriftung, die keine zulassen festgelegt 0 für ihre Flags Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a49af-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="a49af-143">Viele Werte für die Kennzeichen sind selbsterklärend.</span><span class="sxs-lookup"><span data-stu-id="a49af-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="a49af-144">Beispielsweise wenn DT_REQUIRED für ein Steuerelement festgelegt ist, müssen sie einen Wert enthalten, bevor das Dialogfeld geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a49af-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="a49af-145">Entweder der Dienstanbieter angeben eines Werts durch **IMAPIProp** implementieren, oder der Benutzer kann eine eingeben.</span><span class="sxs-lookup"><span data-stu-id="a49af-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="a49af-146">DT_EDITABLE gibt an, dass der Wert für das Steuerelement geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a49af-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="a49af-147">DT_MULTILINE können den Wert für ein Edit-Steuerelement über mehrere Zeilen erstrecken.</span><span class="sxs-lookup"><span data-stu-id="a49af-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="a49af-148">Einige Steuerelement Flags sind nicht so offensichtlich in ihre Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="a49af-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="a49af-149">Wenn ein Steuerelement das Flag DT_SET_IMMEDIATE festlegt, wirkt sich auf alle zu dessen Wert, sobald der Benutzer auf ein neues Steuerelement wechselt.</span><span class="sxs-lookup"><span data-stu-id="a49af-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="a49af-150">MAPI stellt einen einzigen Anruf an die Eigenschaft Schnittstelle [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode für die Eigenschaft des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="a49af-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="a49af-151">Dies ist das Standardverhalten besteht darin, dass Änderungen an Steuerelementwerte wirksam erst, nachdem der Benutzer die Schaltfläche **OK wählt** oder das Dialogfeld schließt verschieben unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="a49af-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="a49af-152">Das Flag DT_SET_IMMEDIATE wird häufig in Kombination mit anzeigebenachrichtigungen-Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="a49af-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="a49af-153">Die folgende Tabelle enthält die Typen von Steuerelementen und alle Werte für die Kennzeichen, die für jeden Typ festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="a49af-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="a49af-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="a49af-154">**Control**</span></span>|<span data-ttu-id="a49af-155">**Gültige Werte für diese Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="a49af-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a49af-156">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a49af-156">Button</span></span>  <br/> |<span data-ttu-id="a49af-157">Muss 0 (null)</span><span class="sxs-lookup"><span data-stu-id="a49af-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="a49af-158">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="a49af-158">Check box</span></span>  <br/> |<span data-ttu-id="a49af-159">DT_EDITABLE DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="a49af-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="a49af-160">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="a49af-160">Combo box</span></span>  <br/> |<span data-ttu-id="a49af-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="a49af-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="a49af-162">Dropdown-Listenfeld</span><span class="sxs-lookup"><span data-stu-id="a49af-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="a49af-163">DT_EDITABLE DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="a49af-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="a49af-164">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="a49af-164">Edit</span></span>  <br/> |<span data-ttu-id="a49af-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="a49af-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="a49af-166">Gruppenfeld</span><span class="sxs-lookup"><span data-stu-id="a49af-166">Group box</span></span>  <br/> |<span data-ttu-id="a49af-167">Muss 0 (null)</span><span class="sxs-lookup"><span data-stu-id="a49af-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="a49af-168">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="a49af-168">Label</span></span>  <br/> |<span data-ttu-id="a49af-169">Muss 0 (null)</span><span class="sxs-lookup"><span data-stu-id="a49af-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="a49af-170">Listenfeld</span><span class="sxs-lookup"><span data-stu-id="a49af-170">List box</span></span>  <br/> |<span data-ttu-id="a49af-171">Muss 0 (null)</span><span class="sxs-lookup"><span data-stu-id="a49af-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="a49af-172">Mehrwertige Dropdown-Listenfeld</span><span class="sxs-lookup"><span data-stu-id="a49af-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="a49af-173">Muss 0 (null)</span><span class="sxs-lookup"><span data-stu-id="a49af-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="a49af-174">Mehrwertige Listenfeld</span><span class="sxs-lookup"><span data-stu-id="a49af-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="a49af-175">Muss 0 (null)</span><span class="sxs-lookup"><span data-stu-id="a49af-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="a49af-176">Seite mit Registerkarten</span><span class="sxs-lookup"><span data-stu-id="a49af-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="a49af-177">Muss 0 (null)</span><span class="sxs-lookup"><span data-stu-id="a49af-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="a49af-178">Optionsfeld</span><span class="sxs-lookup"><span data-stu-id="a49af-178">Radio button</span></span>  <br/> |<span data-ttu-id="a49af-179">Muss 0 (null)</span><span class="sxs-lookup"><span data-stu-id="a49af-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a49af-180">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a49af-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a49af-181">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a49af-181">Header files</span></span>

<span data-ttu-id="a49af-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a49af-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="a49af-183">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a49af-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="a49af-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a49af-184">Mapitags.h</span></span>
  
> <span data-ttu-id="a49af-185">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a49af-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a49af-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a49af-186">See also</span></span>



[<span data-ttu-id="a49af-187">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a49af-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a49af-188">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a49af-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a49af-189">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a49af-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a49af-190">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a49af-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

