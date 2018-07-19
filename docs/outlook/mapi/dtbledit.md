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
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791603"
---
# <a name="dtbledit"></a><span data-ttu-id="95990-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="95990-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="95990-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95990-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95990-105">Beschreibt ein Edit-Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95990-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95990-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="95990-106">Header file:</span></span>  <br/> |<span data-ttu-id="95990-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95990-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="95990-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="95990-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="95990-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="95990-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="95990-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="95990-110">Members</span></span>

 <span data-ttu-id="95990-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="95990-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="95990-112">Ein Offset ab dem Anfang der **DTBLEDIT** -Struktur zu einem Zeichen Zeichenfolge Filter, der Einschränkungen, falls vorhanden, auf die Zeichen beschreibt, die in das Bearbeitungssteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="95990-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="95990-113">Der Filter wird nicht als regulärer Ausdruck interpretiert und der gleiche Filter auf jedes eingegebene Zeichen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="95990-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="95990-114">Das Format des Filters lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="95990-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="95990-115">**Zeichen**</span><span class="sxs-lookup"><span data-stu-id="95990-115">**Character**</span></span>|<span data-ttu-id="95990-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95990-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="95990-117">Ein beliebiges Zeichen ist zulässig (z. B. `"*"`).</span><span class="sxs-lookup"><span data-stu-id="95990-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="95990-118">Definiert eine Reihe von Zeichen (z. B. `"[0123456789]".`)</span><span class="sxs-lookup"><span data-stu-id="95990-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="95990-119">Gibt einen Bereich von Zeichen (z. B. `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="95990-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="95990-120">Gibt an, dass diese Zeichen nicht zulässig sind (beispielsweise `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="95990-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="95990-121">Verwendet, um die vorherigen Zeichen quote (z. B. `"[\-\\\[\]]"` bedeutet-, \, [, und] Zeichen sind zulässig).</span><span class="sxs-lookup"><span data-stu-id="95990-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="95990-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="95990-122">**ulFlags**</span></span>
  
> <span data-ttu-id="95990-123">Bitmaske aus Flags verwendet, um das Format des Filters Zeichen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="95990-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="95990-124">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="95990-124">The following flag can be set:</span></span>
    
<span data-ttu-id="95990-125">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="95990-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="95990-126">Der Filter ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="95990-126">The filter is in Unicode format.</span></span> <span data-ttu-id="95990-127">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Filter im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="95990-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="95990-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="95990-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="95990-129">Maximale Anzahl von Zeichen, die der Benutzer in das Textfeld eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="95990-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="95990-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="95990-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="95990-131">Eigenschaftentag für eine Eigenschaft vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="95990-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="95990-132">Der **UlPropTag** Member identifiziert die Zeichenfolgeneigenschaft, deren Daten angezeigt und im Bearbeitungssteuerelement bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="95990-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="95990-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95990-133">Remarks</span></span>

<span data-ttu-id="95990-134">Eine Struktur **DTBLEDIT** beschreibt ein Edit-Steuerelement einen Bereich in einem Dialogfeld, das alphanumerische Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="95990-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="95990-135">Nahezu alle Dialogfelder verfügen über mindestens ein Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="95990-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="95990-136">Bearbeitungssteuerelemente können geändert werden, von einem Benutzer oder schreibgeschützt sein.</span><span class="sxs-lookup"><span data-stu-id="95990-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="95990-137">Bearbeitungssteuerelemente können auch sein, einzelne Zeile oder die MultiLine-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="95990-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="95990-138">Mehrzeilige Bearbeitungssteuerelemente haben in der Regel eine Bildlaufleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95990-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="95990-139">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="95990-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="95990-140">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="95990-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95990-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95990-141">See also</span></span>



[<span data-ttu-id="95990-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="95990-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="95990-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="95990-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="95990-144">PidTagControlType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="95990-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="95990-145">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="95990-145">MAPI Structures</span></span>](mapi-structures.md)

