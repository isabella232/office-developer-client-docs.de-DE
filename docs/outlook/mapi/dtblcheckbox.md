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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c6726b852176fa31bf879b5a32b63c35ce2be514
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791587"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="91cd5-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="91cd5-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="91cd5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91cd5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91cd5-105">Enthält Informationen über ein Kontrollkästchen, die in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91cd5-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91cd5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="91cd5-106">Header file:</span></span>  <br/> |<span data-ttu-id="91cd5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91cd5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="91cd5-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="91cd5-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="91cd5-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="91cd5-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="91cd5-110">Members</span><span class="sxs-lookup"><span data-stu-id="91cd5-110">Members</span></span>

 <span data-ttu-id="91cd5-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="91cd5-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="91cd5-112">Die Position im Speicher der Zeichenfolge, die das Kontrollkästchen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="91cd5-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="91cd5-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="91cd5-113">**ulFlags**</span></span>
  
> <span data-ttu-id="91cd5-114">Bitmaske aus Flags verwendet, um das Format der Beschriftung des Kontrollkästchens festzulegen.</span><span class="sxs-lookup"><span data-stu-id="91cd5-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="91cd5-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="91cd5-115">The following flag can be set:</span></span>
    
<span data-ttu-id="91cd5-116">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="91cd5-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="91cd5-117">Die Beschriftung wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="91cd5-117">The label is in Unicode format.</span></span> <span data-ttu-id="91cd5-118">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="91cd5-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="91cd5-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="91cd5-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="91cd5-120">Eigenschaftentag für eine Eigenschaft vom Typ PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="91cd5-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="91cd5-121">Der Wert dieser Eigenschaft wird von den Status des Kontrollkästchens beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="91cd5-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91cd5-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91cd5-122">Remarks</span></span>

<span data-ttu-id="91cd5-123">Eine Struktur **DTBLCHECKBOX** beschreibt ein Kontrollkästchen ein Steuerelement, das einen von zwei Status widerspiegelt: (aktivierte Kontrollkästchen) aktiviert oder deaktiviert (ein leeres Feld).</span><span class="sxs-lookup"><span data-stu-id="91cd5-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="91cd5-124">Der **UlPRPropertyName** -Member beschreibt eine boolesche Eigenschaft, deren Wert bearbeitet wird, indem Sie den Status des Kontrollkästchens ändern.</span><span class="sxs-lookup"><span data-stu-id="91cd5-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="91cd5-125">Wenn das Kontrollkästchen zuerst angezeigt wird, ruft MAPI die **GetProps** -Methode der **IMAPIProp** -Implementierung, die die Tabelle anzeigen zum Abrufen von Standardeigenschaften zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="91cd5-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="91cd5-126">Wenn eine der Eigenschaften in der Struktur **DTBLCHECKBOX** das Eigenschafts-Tag zugeordnet ist, wird der Wert für diese Eigenschaft als Anfangswert das Kontrollkästchen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="91cd5-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="91cd5-127">Kontrollkästchen-Steuerelementen können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="91cd5-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="91cd5-128">Dies ermöglicht einem Benutzer, ändert sich ihr Status.</span><span class="sxs-lookup"><span data-stu-id="91cd5-128">This allows a user to change their states.</span></span> <span data-ttu-id="91cd5-129">Änderbare Kontrollkästchen legen Sie das DT_EDITABLE-Flag im **UlCtlFlags** Mitglied ihrer [DTCTL](dtctl.md) Struktur und in ihre **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="91cd5-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="91cd5-130">Wenn Sie den Zustand ein Kontrollkästchens geändert wird, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) zum Festlegen der Eigenschaft in der Eigenschaft Tag Member der Struktur in den neuen Zustand **DTBLCHECKBOX** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="91cd5-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="91cd5-131">Adressbuch-Dienstanbieter kann beispielsweise eine änderbare Kontrollkästchen-Steuerelement im Dialogfeld Konfiguration die Einstellung der Eigenschaft für einen Empfänger **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) anpassen enthalten.</span><span class="sxs-lookup"><span data-stu-id="91cd5-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="91cd5-132">Wenn der Benutzer das Kontrollkästchen auswählt, wird diese Eigenschaft von MAPI auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="91cd5-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="91cd5-133">Wenn das Kontrollkästchen deaktiviert ist, wird die Eigenschaft auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="91cd5-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="91cd5-134">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="91cd5-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="91cd5-135">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="91cd5-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="91cd5-136">Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="91cd5-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="91cd5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91cd5-137">See also</span></span>



[<span data-ttu-id="91cd5-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="91cd5-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="91cd5-139">Kanonische PidTagControlType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="91cd5-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="91cd5-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="91cd5-140">MAPI Structures</span></span>](mapi-structures.md)

