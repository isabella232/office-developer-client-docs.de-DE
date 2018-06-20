---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3a5188ea9f83d05722c6b5ab81d9e796b33ef254
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791592"
---
# <a name="dtblcombobox"></a><span data-ttu-id="c73b2-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="c73b2-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="c73b2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c73b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c73b2-105">Beschreibt ein Kombinationsfeld-Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c73b2-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c73b2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c73b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="c73b2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c73b2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c73b2-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="c73b2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="c73b2-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="c73b2-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a><span data-ttu-id="c73b2-110">Members</span><span class="sxs-lookup"><span data-stu-id="c73b2-110">Members</span></span>

 <span data-ttu-id="c73b2-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="c73b2-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="c73b2-112">Ein Offset ab dem Anfang der **DTBLCOMBOBOX** -Struktur zu einem Zeichen Zeichenfolge Filter, der Einschränkungen, wenn vorhanden, um die Zeichen, die in des Kombinationsfelds eingegeben werden können Bearbeitungssteuerelement beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c73b2-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="c73b2-113">Der Filter wird nicht als regulärer Ausdruck interpretiert und der gleiche Filter auf jedes eingegebene Zeichen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c73b2-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="c73b2-114">Das Format des Filters lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c73b2-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="c73b2-115">**Zeichen**</span><span class="sxs-lookup"><span data-stu-id="c73b2-115">**Character**</span></span>|<span data-ttu-id="c73b2-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c73b2-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="c73b2-117">Ein beliebiges Zeichen ist zulässig (z. B. `"*"`).</span><span class="sxs-lookup"><span data-stu-id="c73b2-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="c73b2-118">Definiert eine Reihe von Zeichen (z. B. `"[0123456789]"`).</span><span class="sxs-lookup"><span data-stu-id="c73b2-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="c73b2-119">Gibt einen Bereich von Zeichen (z. B. `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="c73b2-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="c73b2-120">Gibt an, dass diese Zeichen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c73b2-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="c73b2-121">(z. B. `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="c73b2-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="c73b2-122">Verwendet, um die vorherigen Zeichen quote (z. B. `"[\-\\\[\]]"` bedeutet-, \, [, und] Zeichen sind zulässig).</span><span class="sxs-lookup"><span data-stu-id="c73b2-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="c73b2-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c73b2-123">**ulFlags**</span></span>
  
> <span data-ttu-id="c73b2-124">Bitmaske aus Flags verwendet, um das Format des Filters Zeichen Zeichenfolge festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c73b2-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="c73b2-125">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c73b2-125">The following flag can be set:</span></span>
    
<span data-ttu-id="c73b2-126">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c73b2-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c73b2-127">Der Filter ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="c73b2-127">The filter is in Unicode format.</span></span> <span data-ttu-id="c73b2-128">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Filter im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="c73b2-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="c73b2-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="c73b2-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="c73b2-130">Maximale Anzahl von Zeichen, die im Textfeld des Kombinationsfelds eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="c73b2-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="c73b2-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="c73b2-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="c73b2-132">Eigenschaftentag für eine Eigenschaft vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="c73b2-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="c73b2-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="c73b2-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="c73b2-134">Eigenschaftentag für eine Eigenschaft vom Typ PT_OBJECT auf dem eine **IMAPITable** -Schnittstelle mithilfe eines Anrufs **OpenProperty** geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c73b2-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="c73b2-135">Die Tabelle muss eine Spalte mit einer Eigenschaft besitzen, die denselben Typ aufweist wie die-Eigenschaft, die durch das **UlPRPropertyName** -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c73b2-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="c73b2-136">Die Zeilen der Tabelle dienen zum Auffüllen der Liste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c73b2-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c73b2-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c73b2-137">Remarks</span></span>

<span data-ttu-id="c73b2-138">Eine Struktur **DTBLCOMBOBOX** beschreibt ein Kombinationsfeld ein Steuerelement, das eine Liste und ein Auswahlfeld besteht.</span><span class="sxs-lookup"><span data-stu-id="c73b2-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="c73b2-139">Die Liste enthält die Informationen, die von dem ein Benutzer kann auswählen, und im Auswahlfeld zeigt die aktuelle Auswahl.</span><span class="sxs-lookup"><span data-stu-id="c73b2-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="c73b2-140">Im Auswahlfeld ist ein Bearbeitungssteuerelement, die auch für die Texteingabe noch nicht in der Liste verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c73b2-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="c73b2-141">Zwei-Eigenschaft Tag Mitglieder arbeiten zusammen, um die Anzeige der Browserliste mit dem Bearbeitungssteuerelement zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="c73b2-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="c73b2-142">Wenn MAPI zunächst das Kombinationsfeld angezeigt wird, ruft es die **OpenProperty** -Methode der **IMAPIProp** -Implementierung, die die Tabelle anzeigen zum Abrufen der Tabelle, dargestellt durch das **UlPRTableName** -Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c73b2-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="c73b2-143">Diese Tabelle hat eine Spalte eine Spalte, die Werte für die Eigenschaft, dargestellt durch das **UlPRPropertyName** -Element enthält.</span><span class="sxs-lookup"><span data-stu-id="c73b2-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="c73b2-144">Aus diesem Grund diese Spalte muss vom gleichen Typ wie die **UlPRPropertyName** -Eigenschaft, und beide Spalten müssen Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="c73b2-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="c73b2-145">Die Werte für die Spalte werden im Listenabschnitt des Kombinationsfelds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c73b2-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="c73b2-146">Aus diesem Grund ist **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) keine gültige Eigenschaftentag für **UlPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="c73b2-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="c73b2-147">Wenn ein Benutzer eine der Zeilen auswählt, oder neue Daten in das Textfeld eingegeben, wird die **UlPRPropertyName** -Eigenschaft auf den ausgewählten oder eingegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c73b2-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="c73b2-148">Um einen Anfangswert für das Bearbeitungssteuerelement anzuzeigen, ruft MAPI [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen der Eigenschaftswerte für die Anzeige-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c73b2-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="c73b2-149">Wenn der abgerufenen Eigenschaften die Eigenschaft, dargestellt durch das **UlPRPropertyName** -Element entspricht, wird ihr Wert der Anfangswert.</span><span class="sxs-lookup"><span data-stu-id="c73b2-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="c73b2-150">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c73b2-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c73b2-151">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c73b2-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c73b2-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c73b2-152">See also</span></span>



[<span data-ttu-id="c73b2-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c73b2-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="c73b2-154">Kanonische PidTagControlType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c73b2-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="c73b2-155">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c73b2-155">MAPI Structures</span></span>](mapi-structures.md)
