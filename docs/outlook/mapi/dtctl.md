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
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339410"
---
# <a name="dtctl"></a><span data-ttu-id="98536-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="98536-103">DTCTL</span></span>

<span data-ttu-id="98536-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98536-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98536-105">Beschreibt ein Steuerelement, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98536-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98536-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="98536-106">Header file:</span></span>  <br/> |<span data-ttu-id="98536-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="98536-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="98536-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="98536-108">Members</span></span>

<span data-ttu-id="98536-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="98536-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="98536-110">Der Typ des Steuerelements, das im **CTL** -Element enthalten ist und der **PR_CONTROL_TYPE** ([pidtagcontroltype (](pidtagcontroltype-canonical-property.md))-Eigenschaft des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="98536-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="98536-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="98536-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="98536-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="98536-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="98536-113">Bezeichnungsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-113">Label control.</span></span>
    
<span data-ttu-id="98536-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="98536-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="98536-115">Bearbeitungssteuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-115">Edit control.</span></span>
    
<span data-ttu-id="98536-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="98536-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="98536-117">Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-117">List box control.</span></span>
    
<span data-ttu-id="98536-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="98536-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="98536-119">Kombinationsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-119">Combo box control.</span></span>
    
<span data-ttu-id="98536-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="98536-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="98536-121">Dropdownlisten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-121">Drop-down list control.</span></span>
    
<span data-ttu-id="98536-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="98536-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="98536-123">Kontrollkästchen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-123">Check box control.</span></span>
    
<span data-ttu-id="98536-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="98536-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="98536-125">Gruppenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-125">Group box control.</span></span>
    
<span data-ttu-id="98536-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="98536-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="98536-127">Schaltflächen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-127">Button control.</span></span>
    
<span data-ttu-id="98536-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="98536-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="98536-129">Seitensteuerelement mit Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="98536-129">Tabbed page control.</span></span>
    
<span data-ttu-id="98536-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="98536-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="98536-131">Optionsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-131">Radio button control.</span></span>
    
<span data-ttu-id="98536-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="98536-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="98536-133">Mehrwertiges Listensteuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="98536-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="98536-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="98536-135">Dropdownlisten-Steuerelement mit mehreren Werten.</span><span class="sxs-lookup"><span data-stu-id="98536-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="98536-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="98536-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="98536-137">Bitmaske von Flags, die die Features des Steuerelements beschreibt und der **PR_CONTROL_FLAGS** ([pidtagcontrolflags (](pidtagcontrolflags-canonical-property.md))-Eigenschaft des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="98536-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="98536-138">Diese Flags können nur für Kontrollkästchen, Kombinationsfelder, Listenfelder und Bearbeitungssteuerelemente festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="98536-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="98536-139">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="98536-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="98536-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="98536-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="98536-141">Das ANSI-oder das DBCS-Format wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="98536-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="98536-142">Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="98536-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="98536-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="98536-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="98536-144">Ein Benutzer kann den Text im Steuerelement ändern.</span><span class="sxs-lookup"><span data-stu-id="98536-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="98536-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="98536-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="98536-146">Das Steuerelement kann mehrere Textzeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="98536-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="98536-147">Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="98536-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="98536-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="98536-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="98536-149">Das Steuerelement enthält ein Kennwort; Daher sollte dem Benutzer der Inhalt des Steuerelements nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="98536-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="98536-150">Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="98536-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="98536-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="98536-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="98536-152">Das Dialogfeld-Steuerelement ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98536-152">The dialog box control is required.</span></span> <span data-ttu-id="98536-153">Dieses Flag ist nur für Bearbeitungs-und Kombinationsfeld-Steuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="98536-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="98536-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="98536-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="98536-155">Ermöglicht die sofortige Ausgabe eines Werts bei einer Änderung im Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="98536-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="98536-156">Dadurch kann eine Abhängigkeitsbeziehung zwischen zwei Steuerelementen hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="98536-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="98536-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="98536-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="98536-158">Zeiger auf eine Struktur, die aus einer [GUID](guid.md) -Struktur besteht, die den Dienstanbieter und einen Bezeichner für das Steuerelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="98536-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="98536-159">Die **lpbNotif** -und **cbNotif** -Member entsprechen der **PR_CONTROL_ID** ([pidtagcontrolid (](pidtagcontrolid-canonical-property.md))-Eigenschaft des Steuerelements und werden verwendet, um die Benutzeroberfläche zu benachrichtigen, wenn das Steuerelement aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="98536-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="98536-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="98536-160">**cbNotif**</span></span>
  
> <span data-ttu-id="98536-161">Die Anzahl der Bytes in der Struktur, auf die durch das **lpbNotif** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="98536-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="98536-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="98536-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="98536-163">Zeiger auf eine Zeichenfolge, die beschreibt, welche Zeichen in ein Bearbeitungs-oder Kombinationsfeld-Steuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="98536-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="98536-164">Bei anderen Steuerelementtypen kann das **lpszFilter** -Element NULL sein.</span><span class="sxs-lookup"><span data-stu-id="98536-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="98536-165">Bei Bearbeitungs-und Kombinationsfeld-Steuerelementen sollte es sich um einen regulären Ausdruck handeln, der jeweils auf ein einzelnes Zeichen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="98536-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="98536-166">Derselbe Filter wird auf alle Zeichen im Steuerelement angewendet.</span><span class="sxs-lookup"><span data-stu-id="98536-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="98536-167">Das Format der Filterzeichenfolge lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="98536-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="98536-168">**Zeichen**</span><span class="sxs-lookup"><span data-stu-id="98536-168">**Character**</span></span>|<span data-ttu-id="98536-169">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98536-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="98536-170">Ein beliebiges Zeichen ist zulässig (Beispiels `"*"`Weise).</span><span class="sxs-lookup"><span data-stu-id="98536-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="98536-171">Definiert eine Gruppe von Zeichen (beispielsweise `"[0123456789]"`.)</span><span class="sxs-lookup"><span data-stu-id="98536-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="98536-172">Gibt einen Zeichentyp an (beispielsweise `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="98536-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="98536-173">Gibt an, dass diese Zeichen nicht zulässig sind (zum `"[~0-9]")`Beispiel.</span><span class="sxs-lookup"><span data-stu-id="98536-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="98536-174">Wird verwendet, um eines der vorherigen Symbole zu zitieren ( `"[\-\\\[\]]"` beispielsweise sind \, means-, [und] characters zulässig).</span><span class="sxs-lookup"><span data-stu-id="98536-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="98536-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="98536-175">**ulItemID**</span></span>
  
> <span data-ttu-id="98536-176">Wert, der das Steuerelement in der Dialogfeldressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="98536-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="98536-177">Bei Registerkarten-Steuerelementen vom Typ DTCT_PAGE wird optional das **ulItemID** -Element verwendet, um den Komponentennamen für die Seite aus einer String-Ressource zu laden.</span><span class="sxs-lookup"><span data-stu-id="98536-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="98536-178">Positions-und Beschriftungsinformationen werden aus der Dialogfeldressource gelesen.</span><span class="sxs-lookup"><span data-stu-id="98536-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="98536-179">**veraltete**</span><span class="sxs-lookup"><span data-stu-id="98536-179">**ctl**</span></span>
  
> <span data-ttu-id="98536-180">Eine Struktur, die die Daten für das Steuerelement enthält und der **PR_CONTROL_STRUCTURE** ([pidtagcontrolstructure (](pidtagcontrolstructure-canonical-property.md))-Eigenschaft des Steuerelements entspricht.</span><span class="sxs-lookup"><span data-stu-id="98536-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="98536-181">Jeder Steuerelementtyp hat eine andere Struktur.</span><span class="sxs-lookup"><span data-stu-id="98536-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98536-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98536-182">Remarks</span></span>

<span data-ttu-id="98536-183">Die **DTCTL** -Struktur beschreibt ein Steuerelement eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="98536-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="98536-184">Die meisten seiner Member werden verwendet, um Eigenschaften für das Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="98536-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="98536-185">Der **CTL** -Member ist eine Vereinigung von Strukturen, die sich auf einen bestimmten Steuerelementtyp beziehen.</span><span class="sxs-lookup"><span data-stu-id="98536-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="98536-186">Wenn die **DTCTL** -Struktur ein Edit-Steuerelement beschreibt, zeigt der **CTL** -Member beispielsweise auf eine [DTBLEDIT](dtbledit.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="98536-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="98536-187">Diese Struktur entspricht der **PR_CONTROL_STRUCTURE** -Eigenschaft des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="98536-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="98536-188">Die Union hat als erster Member eine Variable vom Typ LPVOID, um die Kompilierungszeit Initialisierung der **DTCTL** -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="98536-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="98536-189">Obwohl die [BuildDisplayTable](builddisplaytable.md) -Funktion die **DTCTL** -Struktur zum Erstellen der Anzeigetabelle aus den Steuerelementressourcen verwendet, wird die **DTCTL** -Struktur nie in der Anzeigetabelle selbst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98536-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="98536-190">Diese Struktur liefert nur Informationen an **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="98536-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="98536-191">Im **ulCtlFlags** -Element betreffen vier Flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT nur Bearbeitungssteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="98536-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="98536-192">Zwei weitere DT_REQUIRED und DT_SET_IMMEDIATE wirken sich auf ein bearbeitbares Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="98536-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="98536-193">Zu den verfügbaren Steuerelementen für ein Dialogfeld gehören die Bezeichnungen, das Textfeld, das Textfeld, die Liste, die Dropdownliste, das Kombinationsfeld, das Kontrollkästchen, das Gruppenfeld, die Schaltfläche, die Optionsschaltfläche und die Registerkartenseite.</span><span class="sxs-lookup"><span data-stu-id="98536-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="98536-194">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="98536-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="98536-195">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="98536-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98536-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98536-196">See also</span></span>

- [<span data-ttu-id="98536-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="98536-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="98536-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="98536-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="98536-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="98536-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="98536-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="98536-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="98536-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="98536-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="98536-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="98536-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="98536-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="98536-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="98536-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="98536-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="98536-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="98536-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="98536-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="98536-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="98536-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="98536-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="98536-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="98536-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="98536-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="98536-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="98536-210">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="98536-210">MAPI Structures</span></span>](mapi-structures.md)

