---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404680"
---
# <a name="dtbledit"></a><span data-ttu-id="4740d-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="4740d-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="4740d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4740d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4740d-105">Beschreibt ein Bearbeitungssteuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4740d-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4740d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4740d-106">Header file:</span></span>  <br/> |<span data-ttu-id="4740d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4740d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4740d-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="4740d-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="4740d-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="4740d-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="4740d-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="4740d-110">Members</span></span>

 <span data-ttu-id="4740d-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="4740d-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="4740d-112">Ein Offset vom Anfang der **DTBLEDIT-Struktur** zu einem Zeichenzeichenfolgenfilter, der einschränkungen (sofern möglich) zu den Zeichen beschreibt, die in das Bearbeitungssteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="4740d-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="4740d-113">Der Filter wird nicht als regulärer Ausdruck interpretiert, und auf jedes eingegebene Zeichen wird derselbe Filter angewendet.</span><span class="sxs-lookup"><span data-stu-id="4740d-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="4740d-114">Das Format des Filters lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4740d-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="4740d-115">**Zeichen**</span><span class="sxs-lookup"><span data-stu-id="4740d-115">**Character**</span></span>|<span data-ttu-id="4740d-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4740d-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="4740d-117">Jedes Zeichen ist zulässig (z. B.  `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="4740d-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="4740d-118">Definiert eine Reihe von Zeichen (z. B.  `"[0123456789]".` )</span><span class="sxs-lookup"><span data-stu-id="4740d-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="4740d-119">Gibt einen Zeichenbereich an (z. B.  `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="4740d-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="4740d-120">Gibt an, dass diese Zeichen nicht zulässig sind (z. B.  `"[~0-9]"` ).</span><span class="sxs-lookup"><span data-stu-id="4740d-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="4740d-121">Wird verwendet, um eines der vorherigen Symbole anführungszeichen (z. B.  `"[\-\\\[\]]"` bedeutet -, \, [und ] Zeichen sind zulässig).</span><span class="sxs-lookup"><span data-stu-id="4740d-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="4740d-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4740d-122">**ulFlags**</span></span>
  
> <span data-ttu-id="4740d-123">Bitmaske von Flags, die zum Festlegen des Formats des Zeichenfilters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4740d-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="4740d-124">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4740d-124">The following flag can be set:</span></span>
    
<span data-ttu-id="4740d-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4740d-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="4740d-126">Der Filter hat das Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="4740d-126">The filter is in Unicode format.</span></span> <span data-ttu-id="4740d-127">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich der Filter im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="4740d-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="4740d-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="4740d-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="4740d-129">Maximale Anzahl von Zeichen, die der Benutzer in das Textfeld eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="4740d-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="4740d-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="4740d-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="4740d-131">Eigenschaftstag für eine Eigenschaft vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="4740d-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="4740d-132">Das **ulPropTag-Element** identifiziert die string-Eigenschaft, deren Daten im Bearbeitungssteuerelement angezeigt und bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4740d-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4740d-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4740d-133">Remarks</span></span>

<span data-ttu-id="4740d-134">Eine **DTBLEDIT-Struktur** beschreibt ein Bearbeitungssteuerelement einen Bereich in einem Dialogfeld, das alphanumerische Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="4740d-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="4740d-135">Fast alle Dialogfelder verfügen über mindestens ein Bearbeitungssteuerelement.</span><span class="sxs-lookup"><span data-stu-id="4740d-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="4740d-136">Bearbeitungssteuerelemente können von einem Benutzer oder schreibgeschützt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4740d-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="4740d-137">Bearbeitungssteuerelemente können auch ein- oder mehrlinienig sein.</span><span class="sxs-lookup"><span data-stu-id="4740d-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="4740d-138">Steuerelementen für mehrstufige Bearbeitungen ist in der Regel eine Bildlaufleiste zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4740d-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="4740d-139">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4740d-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="4740d-140">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4740d-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4740d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4740d-141">See also</span></span>



[<span data-ttu-id="4740d-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="4740d-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="4740d-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="4740d-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="4740d-144">PidTagControlType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4740d-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="4740d-145">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4740d-145">MAPI Structures</span></span>](mapi-structures.md)

