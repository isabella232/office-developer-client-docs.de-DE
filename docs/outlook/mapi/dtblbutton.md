---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2505f555fd8867fdc24a14f523a74b6f478a3e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791598"
---
# <a name="dtblbutton"></a><span data-ttu-id="e2f78-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="e2f78-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="e2f78-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2f78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2f78-105">Enthält Informationen über ein Button-Steuerelement für ein Dialogfeld erstellt aus einer Tabelle anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e2f78-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2f78-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e2f78-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2f78-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2f78-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e2f78-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="e2f78-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e2f78-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="e2f78-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="e2f78-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="e2f78-110">Members</span></span>

 <span data-ttu-id="e2f78-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="e2f78-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="e2f78-112">Die Position im Speicher der Zeichenfolge, die auf der Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2f78-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="e2f78-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e2f78-113">**ulFlags**</span></span>
  
> <span data-ttu-id="e2f78-114">Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabel** Member.</span><span class="sxs-lookup"><span data-stu-id="e2f78-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="e2f78-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e2f78-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="e2f78-116">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2f78-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e2f78-117">Die Beschriftung wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="e2f78-117">The label is in Unicode format.</span></span> <span data-ttu-id="e2f78-118">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="e2f78-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="e2f78-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="e2f78-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="e2f78-120">Eigenschaftentag für eine Eigenschaft vom Typ PT_OBJECT, die die [IMAPIControl](imapicontroliunknown.md) -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="e2f78-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="e2f78-121">Wenn die Schaltfläche geklickt wird, ruft MAPI die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für die Anzeige Tabelle [IMAPIProp](imapipropiunknown.md) Implementierung dieser Eigenschaft abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e2f78-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e2f78-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2f78-122">Remarks</span></span>

<span data-ttu-id="e2f78-123">Eine Struktur **DTBLBUTTON** beschreibt eine Schaltfläche ein Steuerelement, das bei geklickt haben, kann sich einen Benutzer einen Vorgang beginnen.</span><span class="sxs-lookup"><span data-stu-id="e2f78-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="e2f78-124">In der Regel wird eine Schaltfläche auf die ein modales Dialogfeld angezeigt werden oder eine programmtechnische Aufgabe aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e2f78-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="e2f78-125">Dienstanbieter können alles über ein Button-Steuerelement implementieren.</span><span class="sxs-lookup"><span data-stu-id="e2f78-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="e2f78-126">Wenn die Schaltfläche zum Ausführen einer Aufgabe basierend auf den Werten der andere Steuerelemente, müssen diese Steuerelemente das Flag DT_SET_IMMEDIATE festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="e2f78-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="e2f78-127">Der **UlbLpszLabel** -Member ist die Position im Speicher der Zeichenfolge, die auf der Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2f78-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="e2f78-128">Dienstanbieter können kaufmännischen und-Zeichen hinzufügen (&amp;) an, dass ein Windows-Accelerator die Bezeichnung der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="e2f78-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="e2f78-129">Drücken der Zugriffstaste hat die gleiche Auswirkung wie das Klicken auf die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="e2f78-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="e2f78-130">Der **UlPRControl** -Member beschreibt-Eigenschaft eines Objekts, das beim Öffnen mit der **IMAPIProp::OpenProperty** -Methode gibt einen Zeiger auf ein Control-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e2f78-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="e2f78-131">Ein Control-Objekt, das die **IMAPIControl** -Schnittstelle unterstützt die Implementierung ist eine Möglichkeit zum Erweitern der MAPI-Featuregruppe und legen Sie den Vorgang oder eine Aufgabe, das auftritt, wenn auf die Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="e2f78-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="e2f78-132">**IMAPIControl** unterstützt zwei Methoden zum Bearbeiten von Schaltflächen: [GetState](imapicontrol-getstate.md) zu deaktivieren oder Aktivieren der Schaltflächen und [Aktivieren](imapicontrol-activate.md) , auf eine Schaltfläche zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="e2f78-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="e2f78-133">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e2f78-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e2f78-134">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e2f78-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2f78-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2f78-135">See also</span></span>



[<span data-ttu-id="e2f78-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e2f78-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e2f78-137">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e2f78-137">MAPI Structures</span></span>](mapi-structures.md)

