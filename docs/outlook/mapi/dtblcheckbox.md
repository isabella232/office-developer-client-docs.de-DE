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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287269"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="5895e-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="5895e-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="5895e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5895e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5895e-105">Enthält Informationen zu einem Kontrollkästchen, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5895e-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5895e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5895e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5895e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5895e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5895e-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="5895e-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="5895e-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="5895e-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="5895e-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="5895e-110">Members</span></span>

 <span data-ttu-id="5895e-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="5895e-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="5895e-112">Position im Arbeitsspeicher der Zeichenfolge, die mit dem Kontrollkästchen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5895e-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="5895e-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5895e-113">**ulFlags**</span></span>
  
> <span data-ttu-id="5895e-114">Bitmaske von Flags, die zum Festlegen des Formats der Kontrollkästchenbeschriftung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5895e-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="5895e-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5895e-115">The following flag can be set:</span></span>
    
<span data-ttu-id="5895e-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5895e-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5895e-117">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="5895e-117">The label is in Unicode format.</span></span> <span data-ttu-id="5895e-118">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="5895e-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="5895e-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="5895e-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="5895e-120">Property-Tag für eine Eigenschaft vom Typ PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="5895e-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="5895e-121">Der Wert dieser Eigenschaft hängt vom Status des Kontrollkästchens ab.</span><span class="sxs-lookup"><span data-stu-id="5895e-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5895e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5895e-122">Remarks</span></span>

<span data-ttu-id="5895e-123">Eine **DTBLCHECKBOX** -Struktur beschreibt ein Kontrollkästchen ein Steuerelement, das einen der beiden Zustände widerspiegelt: Enabled (ein aktiviertes Kontrollkästchen) oder deaktiviert (ein leeres Feld).</span><span class="sxs-lookup"><span data-stu-id="5895e-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="5895e-124">Das **ulPRPropertyName** -Element beschreibt eine boolesche Eigenschaft, deren Wert durch Ändern des Status des Kontrollkästchens geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5895e-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="5895e-125">Wenn das Kontrollkästchen zuerst angezeigt wird, ruft MAPI die \*\*\*\* GetProps-Methode der **IMAPIProp** -Implementierung auf, die der Anzeigetabelle zugeordnet ist, um einen Satz von Standardeigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5895e-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="5895e-126">Wenn eine der Eigenschaften dem Property-Tag in der **DTBLCHECKBOX** -Struktur zugeordnet ist, wird der Wert für diese Eigenschaft als Anfangswert des Kontrollkästchens angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5895e-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="5895e-127">Kontrollkästchen-Steuerelemente können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5895e-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="5895e-128">Dadurch kann ein Benutzer seine Status ändern.</span><span class="sxs-lookup"><span data-stu-id="5895e-128">This allows a user to change their states.</span></span> <span data-ttu-id="5895e-129">Veränderbare Kontrollkästchen legen Sie das DT_EDITABLE-Flag im **ulCtlFlags** -Element ihrer [DTCTL](dtctl.md) -Struktur und in Ihrer **PR_CONTROL_FLAGS** ([pidtagcontrolflags (](pidtagcontrolflags-canonical-property.md))-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="5895e-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="5895e-130">Wenn ein Kontrollkästchen seinen Status ändert, ruft MAPI [IMAPIProp::](imapiprop-setprops.md) SetProps auf, um die im Property-Tag-Element der **DTBLCHECKBOX** -Struktur angegebene Eigenschaft auf den neuen Status festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5895e-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="5895e-131">Ein Adressbuchanbieter kann beispielsweise ein änderbares Kontrollkästchen-Steuerelement in sein Konfigurationsdialogfeld aufnehmen, um die Einstellung der **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft eines Empfängers anzupassen.</span><span class="sxs-lookup"><span data-stu-id="5895e-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="5895e-132">Wenn der Benutzer das Kontrollkästchen aktiviert, wird diese Eigenschaft von MAPI auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5895e-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="5895e-133">Wenn das Kontrollkästchen deaktiviert ist, wird die Eigenschaft auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5895e-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="5895e-134">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5895e-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="5895e-135">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="5895e-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="5895e-136">Weitere Informationen zu Eigenschaftstypen finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5895e-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5895e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5895e-137">See also</span></span>



[<span data-ttu-id="5895e-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="5895e-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="5895e-139">Kanonische Pidtagcontroltype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5895e-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="5895e-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5895e-140">MAPI Structures</span></span>](mapi-structures.md)

