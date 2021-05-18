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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406976"
---
# <a name="dtblcombobox"></a><span data-ttu-id="50038-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="50038-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="50038-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50038-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50038-105">Beschreibt ein Kombinationsfeldsteuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="50038-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50038-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="50038-106">Header file:</span></span>  <br/> |<span data-ttu-id="50038-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50038-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="50038-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="50038-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="50038-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="50038-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a><span data-ttu-id="50038-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="50038-110">Members</span></span>

 <span data-ttu-id="50038-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="50038-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="50038-112">Ein Offset vom Anfang der **DTBLCOMBOBOX-Struktur** zu einem Zeichenzeichenfolgenfilter, der einschränkungen (sofern möglich) zu den Zeichen beschreibt, die in das Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="50038-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="50038-113">Der Filter wird nicht als regulärer Ausdruck interpretiert, und auf jedes eingegebene Zeichen wird derselbe Filter angewendet.</span><span class="sxs-lookup"><span data-stu-id="50038-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="50038-114">Das Format des Filters lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="50038-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="50038-115">**Zeichen**</span><span class="sxs-lookup"><span data-stu-id="50038-115">**Character**</span></span>|<span data-ttu-id="50038-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50038-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="50038-117">Jedes Zeichen ist zulässig (z. B.  `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="50038-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="50038-118">Definiert eine Reihe von Zeichen (z. B.  `"[0123456789]"` ).</span><span class="sxs-lookup"><span data-stu-id="50038-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="50038-119">Gibt einen Zeichenbereich an (z. B.  `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="50038-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="50038-120">Gibt an, dass diese Zeichen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="50038-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="50038-121">(z. B.  `"[~0-9]"` ).</span><span class="sxs-lookup"><span data-stu-id="50038-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="50038-122">Wird verwendet, um eines der vorherigen Symbole anführungszeichen (z. B.  `"[\-\\\[\]]"` bedeutet -, \, [und ] Zeichen sind zulässig).</span><span class="sxs-lookup"><span data-stu-id="50038-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="50038-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="50038-123">**ulFlags**</span></span>
  
> <span data-ttu-id="50038-124">Bitmaske von Flags, die zum Festlegen des Formats des Zeichenzeichenfolgenfilters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50038-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="50038-125">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="50038-125">The following flag can be set:</span></span>
    
<span data-ttu-id="50038-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50038-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="50038-127">Der Filter hat das Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="50038-127">The filter is in Unicode format.</span></span> <span data-ttu-id="50038-128">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich der Filter im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="50038-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="50038-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="50038-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="50038-130">Maximale Anzahl von Zeichen, die im Textfeld des Kombinationsfelds eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="50038-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="50038-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="50038-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="50038-132">Eigenschaftstag für eine Eigenschaft vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="50038-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="50038-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="50038-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="50038-134">Eigenschaftstag für eine Eigenschaft vom Typ PT_OBJECT, auf der eine **IMAPITable-Schnittstelle** mithilfe eines **OpenProperty-Aufrufs geöffnet werden** kann.</span><span class="sxs-lookup"><span data-stu-id="50038-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="50038-135">Die Tabelle muss eine Spalte mit einer Eigenschaft enthalten, die denselben Typ wie die vom **ulPRPropertyName-Element identifizierte Eigenschaft** hat.</span><span class="sxs-lookup"><span data-stu-id="50038-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="50038-136">Die Zeilen der Tabelle werden zum Auffüllen der Liste verwendet.</span><span class="sxs-lookup"><span data-stu-id="50038-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="50038-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50038-137">Remarks</span></span>

<span data-ttu-id="50038-138">Eine **DTBLCOMBOBOX-Struktur** beschreibt ein Kombinationsfeld ein Steuerelement, das aus einer Liste und einem Auswahlfeld besteht.</span><span class="sxs-lookup"><span data-stu-id="50038-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="50038-139">In der Liste werden die Informationen angezeigt, aus denen ein Benutzer auswählen kann, und das Auswahlfeld zeigt die aktuelle Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="50038-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="50038-140">Das Auswahlfeld ist ein Bearbeitungssteuerelement, das auch zum Eingeben von Text verwendet werden kann, der noch nicht in der Liste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="50038-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="50038-141">Die beiden Eigenschaftentagmitglieder arbeiten zusammen, um die Listenanzeige mit dem Bearbeitungssteuerelement zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="50038-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="50038-142">Wenn MAPI das Kombinationsfeld zum ersten Mal anzeigt, ruft es die **OpenProperty-Methode** der **IMAPIProp-Implementierung** auf, die der Anzeigetabelle zugeordnet ist, um die Tabelle abzurufen, die durch das **ulPRTableName-Element** dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50038-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="50038-143">Diese Tabelle hat eine Spalte eine Spalte, die Werte für die Eigenschaft enthält, die durch das **ulPRPropertyName-Element dargestellt** wird.</span><span class="sxs-lookup"><span data-stu-id="50038-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="50038-144">Daher muss diese Spalte denselben Typ wie die **ulPRPropertyName-Eigenschaft** haben, und beide Spalten müssen Zeichenzeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="50038-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="50038-145">Die Werte für die Spalte werden im Listenabschnitt des Kombinationsfelds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="50038-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="50038-146">Daher ist **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) kein gültiges Eigenschaftstag für **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="50038-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="50038-147">Wenn ein Benutzer eine der Zeilen auswählt oder neue Daten in das Textfeld einbetritt, wird die **ulPRPropertyName-Eigenschaft** auf den ausgewählten oder eingegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50038-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="50038-148">Um einen anfänglichen Wert für das Bearbeitungssteuerelement anzuzeigen, ruft MAPI [IMAPIProp::GetProps](imapiprop-getprops.md) auf, um die Eigenschaftswerte für die Anzeigetabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50038-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="50038-149">Wenn eine der abgerufenen Eigenschaften der Eigenschaft entspricht, die durch das **element ulPRPropertyName** dargestellt wird, wird ihr Wert zum Anfangswert.</span><span class="sxs-lookup"><span data-stu-id="50038-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="50038-150">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="50038-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="50038-151">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="50038-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50038-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50038-152">See also</span></span>



[<span data-ttu-id="50038-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="50038-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="50038-154">PidTagControlType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="50038-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="50038-155">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="50038-155">MAPI Structures</span></span>](mapi-structures.md)

