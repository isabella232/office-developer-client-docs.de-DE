---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421501"
---
# <a name="dtctl"></a><span data-ttu-id="032de-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="032de-103">DTCTL</span></span>

<span data-ttu-id="032de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="032de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="032de-105">Beschreibt ein Steuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="032de-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="032de-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="032de-106">Header file:</span></span>  <br/> |<span data-ttu-id="032de-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="032de-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a><span data-ttu-id="032de-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="032de-108">Members</span></span>

<span data-ttu-id="032de-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="032de-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="032de-110">Typ des Steuerelements, das im **#A0** enthalten ist und der PR_CONTROL_TYPE **(** [PidTagControlType](pidtagcontroltype-canonical-property.md)) des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="032de-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="032de-111">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="032de-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="032de-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="032de-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="032de-113">Bezeichnungsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-113">Label control.</span></span>
    
<span data-ttu-id="032de-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="032de-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="032de-115">Steuerelement bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="032de-115">Edit control.</span></span>
    
<span data-ttu-id="032de-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="032de-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="032de-117">Listenfeldsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-117">List box control.</span></span>
    
<span data-ttu-id="032de-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="032de-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="032de-119">Kombinationsfeldsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-119">Combo box control.</span></span>
    
<span data-ttu-id="032de-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="032de-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="032de-121">Dropdownlistensteuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-121">Drop-down list control.</span></span>
    
<span data-ttu-id="032de-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="032de-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="032de-123">Kontrollkästchen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-123">Check box control.</span></span>
    
<span data-ttu-id="032de-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="032de-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="032de-125">Gruppenfeldsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-125">Group box control.</span></span>
    
<span data-ttu-id="032de-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="032de-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="032de-127">Schaltflächensteuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-127">Button control.</span></span>
    
<span data-ttu-id="032de-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="032de-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="032de-129">Seitensteuerelement mit Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="032de-129">Tabbed page control.</span></span>
    
<span data-ttu-id="032de-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="032de-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="032de-131">Optionsfeldsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-131">Radio button control.</span></span>
    
<span data-ttu-id="032de-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="032de-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="032de-133">Mehrwertiges Listensteuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="032de-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="032de-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="032de-135">Mehrwertige Dropdownlistensteuerung.</span><span class="sxs-lookup"><span data-stu-id="032de-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="032de-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="032de-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="032de-137">Bitmaske von Flags, die die Features des Steuerelements beschreibt und der **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) -Eigenschaft des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="032de-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="032de-138">Diese Kennzeichen können nur für Kontrollkästchen, Kombinationsfelder, Listenfelder und Bearbeitungssteuerelemente festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="032de-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="032de-139">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="032de-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="032de-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="032de-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="032de-141">Entweder das ANSI- oder das DBCS-Format wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="032de-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="032de-142">Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="032de-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="032de-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="032de-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="032de-144">Ein Benutzer kann den Text im Steuerelement ändern.</span><span class="sxs-lookup"><span data-stu-id="032de-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="032de-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="032de-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="032de-146">Das Steuerelement kann mehrere Textzeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="032de-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="032de-147">Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="032de-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="032de-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="032de-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="032de-149">Das Steuerelement enthält ein Kennwort. Daher sollte der Inhalt des Steuerelements dem Benutzer nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="032de-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="032de-150">Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="032de-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="032de-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="032de-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="032de-152">Das Dialogfeldsteuerelement ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="032de-152">The dialog box control is required.</span></span> <span data-ttu-id="032de-153">Dieses Flag ist nur für Bearbeitungs- und Kombinationsfeldsteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="032de-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="032de-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="032de-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="032de-155">Ermöglicht die sofortige Ausgabe eines Werts bei einer Änderung im Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="032de-156">Dadurch kann eine Abhängigkeitsbeziehung zwischen zwei Steuerelementen hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="032de-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="032de-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="032de-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="032de-158">Zeiger auf eine Struktur, die aus einer [GUID-Struktur](guid.md) besteht, um den Dienstanbieter und einen Bezeichner für das Steuerelement zu repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="032de-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="032de-159">Die **Elemente lpbNotif** und **cbNotif** entsprechen der **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))-Eigenschaft des Steuerelements und werden verwendet, um die Benutzeroberfläche zu benachrichtigen, wenn das Steuerelement aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="032de-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="032de-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="032de-160">**cbNotif**</span></span>
  
> <span data-ttu-id="032de-161">Anzahl der Bytes in der Struktur, auf die das **lpbNotif-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="032de-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="032de-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="032de-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="032de-163">Zeiger auf eine Zeichenzeichenfolge, die beschreibt, welche Zeichen in ein Bearbeitungs- oder Kombinationsfeldsteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="032de-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="032de-164">Bei anderen Steuerelementtypen kann **das lpszFilter-Element** NULL sein.</span><span class="sxs-lookup"><span data-stu-id="032de-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="032de-165">Für Bearbeitungs- und Kombinationsfeldsteuerelemente sollte es sich um einen regulären Ausdruck, der für ein einzelnes Zeichen gleichzeitig gilt, sein.</span><span class="sxs-lookup"><span data-stu-id="032de-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="032de-166">Der gleiche Filter wird auf alle Zeichen im Steuerelement angewendet.</span><span class="sxs-lookup"><span data-stu-id="032de-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="032de-167">Das Format der Filterzeichenfolge lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="032de-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="032de-168">**Zeichen**</span><span class="sxs-lookup"><span data-stu-id="032de-168">**Character**</span></span>|<span data-ttu-id="032de-169">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="032de-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="032de-170">Jedes Zeichen ist zulässig (z. B. `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="032de-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="032de-171">Definiert eine Reihe von Zeichen (z. B. `"[0123456789]"` .)</span><span class="sxs-lookup"><span data-stu-id="032de-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="032de-172">Gibt einen Zeichenbereich an (z. B. `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="032de-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="032de-173">Gibt an, dass diese Zeichen nicht zulässig sind (z. B. `"[~0-9]")` .</span><span class="sxs-lookup"><span data-stu-id="032de-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="032de-174">Wird verwendet, um eines der vorherigen Symbole anführungszeichen (z. B. `"[\-\\\[\]]"` bedeutet -, \, [und ] Zeichen sind zulässig).</span><span class="sxs-lookup"><span data-stu-id="032de-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="032de-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="032de-175">**ulItemID**</span></span>
  
> <span data-ttu-id="032de-176">Wert, der das Steuerelement in der Dialogfeldressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="032de-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="032de-177">Bei Registerkartenseitensteuerelementen vom Typ DTCT_PAGE wird das **ulItemID-Element** optional zum Laden des Komponentennamens für die Seite aus einer Zeichenfolgenressource verwendet.</span><span class="sxs-lookup"><span data-stu-id="032de-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="032de-178">Positions- und Bezeichnungsinformationen werden aus der Dialogfeldressource gelesen.</span><span class="sxs-lookup"><span data-stu-id="032de-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="032de-179">**ctl**</span><span class="sxs-lookup"><span data-stu-id="032de-179">**ctl**</span></span>
  
> <span data-ttu-id="032de-180">Eine Struktur, die die Daten für das Steuerelement enthält und der PR_CONTROL_STRUCTURE **(** [PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="032de-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="032de-181">Jeder Steuerelementtyp hat eine andere Struktur.</span><span class="sxs-lookup"><span data-stu-id="032de-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="032de-182">Hinweise</span><span class="sxs-lookup"><span data-stu-id="032de-182">Remarks</span></span>

<span data-ttu-id="032de-183">Die **DTCTL-Struktur** beschreibt ein Steuerelement eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="032de-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="032de-184">Die meisten Elemente werden zum Festlegen von Eigenschaften für das Steuerelement verwendet.</span><span class="sxs-lookup"><span data-stu-id="032de-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="032de-185">Das **#A0** ist eine Vereinigung von Strukturen, die sich auf einen bestimmten Steuerelementtyp beziehen.</span><span class="sxs-lookup"><span data-stu-id="032de-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="032de-186">Wenn die **DTCTL-Struktur** beispielsweise ein Bearbeitungssteuerelement beschreibt, zeigt das **#A0** auf eine [DTBLEDIT-Struktur.](dtbledit.md)</span><span class="sxs-lookup"><span data-stu-id="032de-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="032de-187">Diese Struktur entspricht der  PR_CONTROL_STRUCTURE Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="032de-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="032de-188">Die Union verfügt als erstes Mitglied über eine Variable vom Typ LPVOID, um die Initialisierung der Kompilierungszeit der **DTCTL-Struktur zu** ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="032de-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="032de-189">Obwohl die [BuildDisplayTable-Funktion](builddisplaytable.md) die **DTCTL-Struktur** zum Erstellen der Anzeigetabelle aus Steuerelementressourcen verwendet, wird die **DTCTL-Struktur** niemals in der Anzeigetabelle selbst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="032de-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="032de-190">Diese Struktur stellt nur Informationen für **BuildDisplayTable zur Verfügung.**</span><span class="sxs-lookup"><span data-stu-id="032de-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="032de-191">Im **ulCtlFlags-Element** werden vier Flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT nur Bearbeitungssteuerelemente betreffen.</span><span class="sxs-lookup"><span data-stu-id="032de-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="032de-192">Zwei weitere DT_REQUIRED und DT_SET_IMMEDIATE sich auf ein bearbeitbares Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="032de-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="032de-193">Die für ein Dialogfeld verfügbaren Steuerelemente sind Bezeichnung, Textfeld, Freihandtextfeld, Liste, Dropdownliste, Kombinationsfeld, Kontrollkästchen, Gruppenfeld, Schaltfläche, Optionsfeld und Registerkartenseite.</span><span class="sxs-lookup"><span data-stu-id="032de-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="032de-194">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="032de-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="032de-195">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="032de-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="032de-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="032de-196">See also</span></span>

- [<span data-ttu-id="032de-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="032de-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="032de-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="032de-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="032de-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="032de-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="032de-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="032de-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="032de-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="032de-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="032de-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="032de-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="032de-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="032de-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="032de-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="032de-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="032de-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="032de-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="032de-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="032de-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="032de-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="032de-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="032de-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="032de-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="032de-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="032de-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="032de-210">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="032de-210">MAPI Structures</span></span>](mapi-structures.md)

