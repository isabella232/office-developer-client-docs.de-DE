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
# <a name="dtblcombobox"></a><span data-ttu-id="42dab-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="42dab-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="42dab-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42dab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42dab-105">Beschreibt ein Kombinationsfeld-Steuerelement, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42dab-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42dab-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="42dab-106">Header file:</span></span>  <br/> |<span data-ttu-id="42dab-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="42dab-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="42dab-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="42dab-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="42dab-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="42dab-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a><span data-ttu-id="42dab-110">Members</span><span class="sxs-lookup"><span data-stu-id="42dab-110">Members</span></span>

 <span data-ttu-id="42dab-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="42dab-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="42dab-112">Ein Offset vom Anfang der **DTBLCOMBOBOX** -Struktur zu einem Zeichenfolgenfilter, der ggf. Einschränkungen für die Zeichen beschreibt, die in das Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="42dab-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="42dab-113">Der Filter wird nicht als regulärer Ausdruck interpretiert, und auf jedes eingegebene Zeichen wird derselbe Filter angewendet.</span><span class="sxs-lookup"><span data-stu-id="42dab-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="42dab-114">Das Format des Filters lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="42dab-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="42dab-115">**Zeichen**</span><span class="sxs-lookup"><span data-stu-id="42dab-115">**Character**</span></span>|<span data-ttu-id="42dab-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42dab-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="42dab-117">Ein beliebiges Zeichen ist zulässig (Beispiels `"*"`Weise).</span><span class="sxs-lookup"><span data-stu-id="42dab-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="42dab-118">Definiert eine Gruppe von Zeichen (beispielsweise `"[0123456789]"`).</span><span class="sxs-lookup"><span data-stu-id="42dab-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="42dab-119">Gibt einen Zeichentyp an (beispielsweise `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="42dab-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="42dab-120">Gibt an, dass diese Zeichen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="42dab-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="42dab-121">(Beispiel: `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="42dab-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="42dab-122">Wird verwendet, um eines der vorherigen Symbole zu zitieren ( `"[\-\\\[\]]"` beispielsweise sind \, means-, [und] characters zulässig).</span><span class="sxs-lookup"><span data-stu-id="42dab-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="42dab-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="42dab-123">**ulFlags**</span></span>
  
> <span data-ttu-id="42dab-124">Bitmaske von Flags, die zum Festlegen des Formats des Zeichenfolgen Filters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42dab-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="42dab-125">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="42dab-125">The following flag can be set:</span></span>
    
<span data-ttu-id="42dab-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="42dab-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="42dab-127">Der Filter ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="42dab-127">The filter is in Unicode format.</span></span> <span data-ttu-id="42dab-128">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Filter im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="42dab-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="42dab-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="42dab-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="42dab-130">Maximale Anzahl von Zeichen, die in das Textfeld des Kombinationsfelds eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="42dab-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="42dab-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="42dab-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="42dab-132">Property-Tag für eine Eigenschaft vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="42dab-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="42dab-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="42dab-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="42dab-134">Property-Tag für eine Eigenschaft vom Typ PT_OBJECT, auf der eine **IMAPITable** -Schnittstelle mithilfe eines **OpenProperty** -Aufrufs geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="42dab-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="42dab-135">Die Tabelle muss eine Spalte mit einer Eigenschaft aufweisen, die denselben Typ hat wie die Eigenschaft, die vom **ulPRPropertyName** -Element angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42dab-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="42dab-136">Die Zeilen der Tabelle werden zum Auffüllen der Liste verwendet.</span><span class="sxs-lookup"><span data-stu-id="42dab-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42dab-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42dab-137">Remarks</span></span>

<span data-ttu-id="42dab-138">Eine **DTBLCOMBOBOX** -Struktur beschreibt ein Kombinationsfeld ein Steuerelement, das aus einer Liste und einem Auswahlfeld besteht.</span><span class="sxs-lookup"><span data-stu-id="42dab-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="42dab-139">In der Liste werden die Informationen angezeigt, aus denen ein Benutzer auswählen kann, und das Feldauswahl zeigt die aktuelle Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="42dab-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="42dab-140">Das Auswahlfeld ist ein Bearbeitungssteuerelement, mit dem auch Text eingegeben werden kann, der noch nicht in der Liste aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="42dab-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="42dab-141">Die beiden Elemente des Property-Tags arbeiten zusammen, um die Listenanzeige mit dem Bearbeitungssteuerelement zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="42dab-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="42dab-142">Wenn MAPI das Kombinationsfeld zuerst anzeigt, wird die **OpenProperty** -Methode der **IMAPIProp** -Implementierung aufgerufen, die der Anzeigetabelle zugeordnet ist, um die vom **ulPRTableName** -Element dargestellte Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42dab-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="42dab-143">Diese Tabelle enthält eine Spalte eine Spalte mit Werten für die vom **ulPRPropertyName** -Element dargestellte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="42dab-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="42dab-144">Daher muss diese Spalte denselben Typ wie die **ulPRPropertyName** -Eigenschaft aufweisen, und beide Spalten müssen Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="42dab-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="42dab-145">Die Werte für die Spalte werden im Listenabschnitt des Kombinationsfelds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42dab-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="42dab-146">Daher ist **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)) kein gültiges Property-Tag für **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="42dab-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="42dab-147">Wenn ein Benutzer eine der Zeilen auswählt oder neue Daten in das Textfeld eingibt, wird die **ulPRPropertyName** -Eigenschaft auf den ausgewählten oder eingegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42dab-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="42dab-148">Um einen Anfangswert für das Bearbeitungssteuerelement anzuzeigen, ruft MAPI [IMAPIProp::](imapiprop-getprops.md) GetProps auf, um die Eigenschaftswerte für die Anzeigetabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42dab-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="42dab-149">Wenn eine der abgerufenen Eigenschaften mit der vom **ulPRPropertyName** -Element dargestellten Eigenschaft übereinstimmt, wird deren Wert zum Anfangswert.</span><span class="sxs-lookup"><span data-stu-id="42dab-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="42dab-150">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="42dab-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="42dab-151">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="42dab-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42dab-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42dab-152">See also</span></span>



[<span data-ttu-id="42dab-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="42dab-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="42dab-154">Kanonische Pidtagcontroltype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="42dab-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="42dab-155">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="42dab-155">MAPI Structures</span></span>](mapi-structures.md)

