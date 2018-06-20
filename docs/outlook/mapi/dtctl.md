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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 68c621f5f73073ed127767cc1db189769dab227d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791635"
---
# <a name="dtctl"></a><span data-ttu-id="754cc-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="754cc-103">DTCTL</span></span>

<span data-ttu-id="754cc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="754cc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="754cc-105">Beschreibt ein Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="754cc-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="754cc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="754cc-106">Header file:</span></span>  <br/> |<span data-ttu-id="754cc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="754cc-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="754cc-108">Members</span><span class="sxs-lookup"><span data-stu-id="754cc-108">Members</span></span>

<span data-ttu-id="754cc-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="754cc-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="754cc-110">Typ des Steuerelements, die in der **Ctl** -Element enthalten ist, und **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))-Eigenschaft des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="754cc-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="754cc-111">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="754cc-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="754cc-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="754cc-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="754cc-113">Bezeichnungsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-113">Label control.</span></span>
    
<span data-ttu-id="754cc-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="754cc-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="754cc-115">Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-115">Edit control.</span></span>
    
<span data-ttu-id="754cc-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="754cc-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="754cc-117">Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-117">List box control.</span></span>
    
<span data-ttu-id="754cc-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="754cc-119">Kombinationsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-119">Combo box control.</span></span>
    
<span data-ttu-id="754cc-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="754cc-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="754cc-121">Dropdown-Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-121">Drop-down list control.</span></span>
    
<span data-ttu-id="754cc-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="754cc-123">Kontrollkästchen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-123">Check box control.</span></span>
    
<span data-ttu-id="754cc-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="754cc-125">Gruppenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-125">Group box control.</span></span>
    
<span data-ttu-id="754cc-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="754cc-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="754cc-127">Schaltflächen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-127">Button control.</span></span>
    
<span data-ttu-id="754cc-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="754cc-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="754cc-129">Mit Registerkarten-Seitensteuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-129">Tabbed page control.</span></span>
    
<span data-ttu-id="754cc-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="754cc-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="754cc-131">Optionsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-131">Radio button control.</span></span>
    
<span data-ttu-id="754cc-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="754cc-133">Mehrwertiges Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="754cc-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="754cc-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="754cc-135">Mehrwertiges Dropdown-Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="754cc-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="754cc-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="754cc-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="754cc-137">Bitmaske aus Flags, die Beschreibung des Steuerelements Features und **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))-Eigenschaft des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="754cc-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="754cc-138">Diese Flags für Kontrollkästchen, Kombinationsfelder und Listenfelder festgelegt werden können, und Steuerelemente nur bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="754cc-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="754cc-139">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="754cc-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="754cc-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="754cc-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="754cc-141">Die ANSI oder DBCS-Format wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="754cc-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="754cc-142">Dieses Kennzeichen ist gültig für Bearbeitungssteuerelemente nur.</span><span class="sxs-lookup"><span data-stu-id="754cc-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="754cc-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="754cc-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="754cc-144">Benutzer können den Text im Steuerelement ändern.</span><span class="sxs-lookup"><span data-stu-id="754cc-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="754cc-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="754cc-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="754cc-146">Das Steuerelement kann mehrere Textzeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="754cc-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="754cc-147">Dieses Kennzeichen ist gültig für Bearbeitungssteuerelemente nur.</span><span class="sxs-lookup"><span data-stu-id="754cc-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="754cc-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="754cc-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="754cc-149">Das Steuerelement enthält ein Kennwort an. Daher sollte der Inhalt des Steuerelements nicht dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="754cc-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="754cc-150">Dieses Kennzeichen ist gültig für Bearbeitungssteuerelemente nur.</span><span class="sxs-lookup"><span data-stu-id="754cc-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="754cc-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="754cc-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="754cc-152">Das Dialogfeld-Steuerelement ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="754cc-152">The dialog box control is required.</span></span> <span data-ttu-id="754cc-153">Dieses Kennzeichen gilt nur für bearbeiten und Kombinationsfeld-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="754cc-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="754cc-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="754cc-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="754cc-155">Ermöglicht die sofortige Ausgabe eines Werts bei einer Änderung des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="754cc-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="754cc-156">Dies ermöglicht eine abhängigkeitsbeziehung zwischen zwei Steuerelemente eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="754cc-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="754cc-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="754cc-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="754cc-158">Zeiger auf eine Struktur, die eine [GUID](guid.md) -Struktur zur Darstellung der Dienstanbieter und einen Bezeichner für das Steuerelement besteht.</span><span class="sxs-lookup"><span data-stu-id="754cc-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="754cc-159">Die Member **LpbNotif** und **CbNotif** **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))-Eigenschaft des Steuerelements entspricht und werden verwendet, um die Benutzeroberfläche zu benachrichtigen, wenn das Steuerelement hat aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="754cc-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="754cc-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="754cc-160">**cbNotif**</span></span>
  
> <span data-ttu-id="754cc-161">Anzahl von Bytes in der Struktur auf den Member **LpbNotif** zeigt.</span><span class="sxs-lookup"><span data-stu-id="754cc-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="754cc-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="754cc-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="754cc-163">Zeiger auf eine Zeichenfolge, die beschreibt, welche Zeichen in einer bearbeiten oder Kombinationsfeld-Steuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="754cc-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="754cc-164">Für andere Arten von Steuerelementen kann der **LpszFilter** Member NULL sein.</span><span class="sxs-lookup"><span data-stu-id="754cc-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="754cc-165">Für bearbeiten und Kombinationsfeld-Steuerelemente sollten sie ein regulärer Ausdruck sein, der auf einem einzelnen Zeichen zu einem Zeitpunkt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="754cc-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="754cc-166">Der gleiche Filter wird auf alle Zeichen im Steuerelement angewendet.</span><span class="sxs-lookup"><span data-stu-id="754cc-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="754cc-167">Das Format der Filterzeichenfolge lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="754cc-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="754cc-168">**Zeichen**</span><span class="sxs-lookup"><span data-stu-id="754cc-168">**Character**</span></span>|<span data-ttu-id="754cc-169">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="754cc-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="754cc-170">Ein beliebiges Zeichen ist zulässig (z. B. `"*"`).</span><span class="sxs-lookup"><span data-stu-id="754cc-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="754cc-171">Definiert eine Reihe von Zeichen (z. B. `"[0123456789]"`.)</span><span class="sxs-lookup"><span data-stu-id="754cc-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="754cc-172">Gibt einen Bereich von Zeichen (z. B. `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="754cc-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="754cc-173">Gibt an, dass diese Zeichen nicht zulässig sind (beispielsweise `"[~0-9]")`.</span><span class="sxs-lookup"><span data-stu-id="754cc-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="754cc-174">Verwendet, um die vorherigen Zeichen quote (z. B. `"[\-\\\[\]]"` bedeutet-, \, [, und] Zeichen sind zulässig).</span><span class="sxs-lookup"><span data-stu-id="754cc-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="754cc-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="754cc-175">**ulItemID**</span></span>
  
> <span data-ttu-id="754cc-176">Wert, der das Steuerelement in das Dialogfeld Feld Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="754cc-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="754cc-177">Für Seiten mit Registerkarten-Steuerelemente des Typs der **UlItemID** DTCT_PAGE wird Mitglied optional den Namen der Komponente für die Seite aus einer String-Ressource zu laden.</span><span class="sxs-lookup"><span data-stu-id="754cc-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="754cc-178">Position und Beschriftung Informationen werden aus dem Dialogfeld Feld Ressource gelesen.</span><span class="sxs-lookup"><span data-stu-id="754cc-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="754cc-179">**CTL**</span><span class="sxs-lookup"><span data-stu-id="754cc-179">**ctl**</span></span>
  
> <span data-ttu-id="754cc-180">Eine Struktur, die die Daten für das Steuerelement enthält und **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))-Eigenschaft des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="754cc-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="754cc-181">Jede Art von Steuerelement verfügt über eine andere Struktur.</span><span class="sxs-lookup"><span data-stu-id="754cc-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="754cc-182">Hinweise</span><span class="sxs-lookup"><span data-stu-id="754cc-182">Remarks</span></span>

<span data-ttu-id="754cc-183">Die Struktur **DTCTL** beschreibt ein Steuerelement eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="754cc-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="754cc-184">Die meisten ihrer Member werden verwendet, um Eigenschaften für das Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="754cc-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="754cc-185">Der **Ctl** -Member ist eine Vereinigung von Strukturen, die mit einer bestimmten Art von Steuerelement verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="754cc-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="754cc-186">Wenn die **DTCTL** -Struktur, die ein Bearbeitungssteuerelement beschreibt ist, zeigen auf eine [DTBLEDIT](dtbledit.md) -Struktur beispielsweise der **Ctl** Member.</span><span class="sxs-lookup"><span data-stu-id="754cc-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="754cc-187">Diese Struktur entspricht **PR_CONTROL_STRUCTURE** -Eigenschaft des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="754cc-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="754cc-188">Die Union hat eine Variable vom Typ LPVOID kompilieren Zeit Initialisierung der Struktur **DTCTL** als erste Member.</span><span class="sxs-lookup"><span data-stu-id="754cc-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="754cc-189">Obwohl die [BuildDisplayTable](builddisplaytable.md) -Funktion die **DTCTL** -Struktur für die Erstellung von der Tabelle anzeigen von Steuerelementressourcen verwendet wird, wird die Struktur **DTCTL** nie in der Anzeige Tabelle selbst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="754cc-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="754cc-190">Diese Struktur stellt nur Informationen zu **BuildDisplayTable**bereit.</span><span class="sxs-lookup"><span data-stu-id="754cc-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="754cc-191">In der **UlCtlFlags** -Member Bearbeitungssteuerelemente vier Flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT wirkt sich nur.</span><span class="sxs-lookup"><span data-stu-id="754cc-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="754cc-192">Zwei andere DT_REQUIRED und DT_SET_IMMEDIATE Einfluss auf ein beliebiges Steuerelement bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="754cc-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="754cc-193">Die Steuerelemente für ein Dialogfeld verfügbar sind Label, Textfeld, Ink-fähigen Textfeld, Liste, Dropdown-Listenfeld, Kombinationsfeld, das Kontrollkästchen, Gruppenfeld, Schaltfläche, Optionsfeld und Seite mit Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="754cc-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="754cc-194">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="754cc-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="754cc-195">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="754cc-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="754cc-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="754cc-196">See also</span></span>

- [<span data-ttu-id="754cc-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="754cc-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="754cc-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="754cc-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="754cc-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="754cc-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="754cc-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="754cc-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="754cc-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="754cc-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="754cc-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="754cc-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="754cc-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="754cc-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="754cc-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="754cc-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="754cc-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="754cc-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="754cc-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="754cc-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="754cc-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="754cc-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="754cc-210">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="754cc-210">MAPI Structures</span></span>](mapi-structures.md)

