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
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412786"
---
# <a name="dtblbutton"></a><span data-ttu-id="a0dfa-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="a0dfa-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="a0dfa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0dfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0dfa-105">Enthält Informationen zu einem Schaltflächen-Steuerelement für ein Dialogfeld, das aus einer Anzeigetabelle erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0dfa-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a0dfa-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0dfa-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a0dfa-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a0dfa-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="a0dfa-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="a0dfa-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="a0dfa-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="a0dfa-110">Members</span><span class="sxs-lookup"><span data-stu-id="a0dfa-110">Members</span></span>

 <span data-ttu-id="a0dfa-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="a0dfa-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="a0dfa-112">Position im Speicher der Zeichenfolge, die auf der Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="a0dfa-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a0dfa-113">**ulFlags**</span></span>
  
> <span data-ttu-id="a0dfa-114">Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabel** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="a0dfa-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a0dfa-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="a0dfa-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a0dfa-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a0dfa-117">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-117">The label is in Unicode format.</span></span> <span data-ttu-id="a0dfa-118">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="a0dfa-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="a0dfa-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="a0dfa-120">Property-Tag für eine Eigenschaft vom Typ PT_OBJECT, die die [IMAPIControl](imapicontroliunknown.md) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="a0dfa-121">Wenn auf die Schaltfläche geklickt wird, ruft MAPI die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode für die [IMAPIProp](imapipropiunknown.md) -Implementierung der Display-Tabelle auf, um diese Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a0dfa-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0dfa-122">Remarks</span></span>

<span data-ttu-id="a0dfa-123">Eine **DTBLBUTTON** -Struktur beschreibt ein Schaltflächen-Steuerelement, mit dem ein Benutzer beim Klicken einen Vorgang beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="a0dfa-124">Wenn Sie auf eine Schaltfläche klicken, wird in der Regel ein modales Dialogfeld angezeigt oder eine programmgesteuerte Aufgabe aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="a0dfa-125">Dienstanbieter können beliebige Elemente über ein Schaltflächen-Steuerelement implementieren.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="a0dfa-126">Wenn die Schaltfläche eine Aufgabe basierend auf den Werten anderer Steuerelemente ausführen soll, müssen diese Steuerelemente das DT_SET_IMMEDIATE-Flag festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="a0dfa-127">Das **ulbLpszLabel** -Element ist die Position im Arbeitsspeicher der Zeichenfolge, die auf der Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="a0dfa-128">Dienstanbieter können ein kaufmännisches und-&amp;Zeichen () hinzufügen, um einen Windows-Beschleuniger in der Schaltflächenbeschriftung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="a0dfa-129">Das Drücken einer Tastenkombination hat dieselbe Wirkung wie das Klicken auf die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="a0dfa-130">Das **ulPRControl** -Element beschreibt eine Objekteigenschaft, die beim Öffnen mit der **IMAPIProp:: OpenProperty** -Methode einen Zeiger auf ein Control-Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="a0dfa-131">Das Implementieren eines Control-Objekts, das die **IMAPIControl** -Schnittstelle unterstützt, stellt eine Möglichkeit dar, die MAPI-Featuregruppe zu erweitern und die Operation oder Aufgabe zu definieren, die beim Klicken auf die Schaltfläche auftritt.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="a0dfa-132">**IMAPIControl** stellt zwei Methoden zum Bearbeiten von Schaltflächen [](imapicontrol-getstate.md) bereit: GetState zum Deaktivieren oder Aktivieren von Schaltflächen und [aktivieren](imapicontrol-activate.md) zum Behandeln von Tastenklicks.</span><span class="sxs-lookup"><span data-stu-id="a0dfa-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="a0dfa-133">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a0dfa-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="a0dfa-134">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="a0dfa-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0dfa-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0dfa-135">See also</span></span>



[<span data-ttu-id="a0dfa-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="a0dfa-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="a0dfa-137">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a0dfa-137">MAPI Structures</span></span>](mapi-structures.md)

