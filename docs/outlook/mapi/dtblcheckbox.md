---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436832"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="af27c-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="af27c-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="af27c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af27c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af27c-105">Enthält Informationen zu einem Kontrollkästchen, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="af27c-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af27c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="af27c-106">Header file:</span></span>  <br/> |<span data-ttu-id="af27c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af27c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="af27c-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="af27c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="af27c-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="af27c-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="af27c-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="af27c-110">Members</span></span>

 <span data-ttu-id="af27c-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="af27c-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="af27c-112">Position im Arbeitsspeicher der Zeichenzeichenfolge, die mit dem Kontrollkästchen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="af27c-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="af27c-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="af27c-113">**ulFlags**</span></span>
  
> <span data-ttu-id="af27c-114">Bitmaske von Flags, die zum Festlegen des Formats der Kontrollkästchenbeschriftung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af27c-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="af27c-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="af27c-115">The following flag can be set:</span></span>
    
<span data-ttu-id="af27c-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af27c-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="af27c-117">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="af27c-117">The label is in Unicode format.</span></span> <span data-ttu-id="af27c-118">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="af27c-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="af27c-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="af27c-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="af27c-120">Eigenschaftstag für eine Eigenschaft vom Typ PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="af27c-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="af27c-121">Der Wert dieser Eigenschaft wird vom Status des Kontrollkästchens beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="af27c-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af27c-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af27c-122">Remarks</span></span>

<span data-ttu-id="af27c-123">Eine **DTBLCHECKBOX-Struktur** beschreibt ein Kontrollkästchen eines Steuerelements, das einen der beiden Zustände widerspiegelt: aktiviert (ein aktiviertes Kontrollkästchen) oder deaktiviert (ein leeres Feld).</span><span class="sxs-lookup"><span data-stu-id="af27c-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="af27c-124">Das **UlPRPropertyName-Element** beschreibt eine boolesche Eigenschaft, deren Wert durch Ändern des Status des Kontrollkästchens geändert wird.</span><span class="sxs-lookup"><span data-stu-id="af27c-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="af27c-125">Wenn das Kontrollkästchen zum ersten Mal angezeigt wird, ruft MAPI die **GetProps-Methode** der **IMAPIProp-Implementierung** auf, die der Anzeigetabelle zugeordnet ist, um eine Reihe von Standardeigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="af27c-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="af27c-126">Wenn eine der Eigenschaften dem Eigenschaftstag in der **DTBLCHECKBOX-Struktur** zu ordnet, wird der Wert für diese Eigenschaft als Anfangswert des Kontrollkästchens angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af27c-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="af27c-127">Kontrollkästchensteuerelemente können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="af27c-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="af27c-128">Dadurch kann ein Benutzer seine Zustände ändern.</span><span class="sxs-lookup"><span data-stu-id="af27c-128">This allows a user to change their states.</span></span> <span data-ttu-id="af27c-129">Modifizierbare Kontrollkästchen legen das DT_EDITABLE-Flag im **ulCtlFlags-Element** der [DTCTL-Struktur](dtctl.md) und in der **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="af27c-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="af27c-130">Wenn ein Kontrollkästchen seinen Status ändert, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um die im Eigenschaftstagm member der **DTBLCHECKBOX-Struktur** identifizierte Eigenschaft auf den neuen Zustand zu setzen.</span><span class="sxs-lookup"><span data-stu-id="af27c-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="af27c-131">Ein **Adressbuchanbieter** kann z. B. ein modifizierbares Kontrollkästchensteuerelement in sein Konfigurationsdialogfeld hinzufügen, um die Einstellung der PR_SEND_RICH_INFO ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))-Eigenschaft eines Empfängers anzupassen.</span><span class="sxs-lookup"><span data-stu-id="af27c-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="af27c-132">Wenn der Benutzer das Kontrollkästchen auswählt, legt MAPI diese Eigenschaft auf TRUE fest.</span><span class="sxs-lookup"><span data-stu-id="af27c-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="af27c-133">Wenn das Kontrollkästchen deaktiviert ist, wird die Eigenschaft auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="af27c-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="af27c-134">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="af27c-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="af27c-135">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="af27c-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="af27c-136">Informationen zu Eigenschaftstypen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="af27c-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af27c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af27c-137">See also</span></span>



[<span data-ttu-id="af27c-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="af27c-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="af27c-139">PidTagControlType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="af27c-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="af27c-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="af27c-140">MAPI Structures</span></span>](mapi-structures.md)

