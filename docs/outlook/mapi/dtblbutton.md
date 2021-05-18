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
# <a name="dtblbutton"></a><span data-ttu-id="ad6b1-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="ad6b1-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="ad6b1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad6b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad6b1-105">Enthält Informationen zu einem Schaltflächensteuerelement für ein Dialogfeld, das aus einer Anzeigetabelle erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad6b1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ad6b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="ad6b1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad6b1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ad6b1-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="ad6b1-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="ad6b1-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="ad6b1-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="ad6b1-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="ad6b1-110">Members</span></span>

 <span data-ttu-id="ad6b1-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="ad6b1-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="ad6b1-112">Position im Arbeitsspeicher der Zeichenzeichenfolge, die auf der Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="ad6b1-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ad6b1-113">**ulFlags**</span></span>
  
> <span data-ttu-id="ad6b1-114">Bitmaske von Flags, die verwendet werden, um das Format der Bezeichnung zu bestimmen, auf das das **ulbLpszLabel-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="ad6b1-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ad6b1-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="ad6b1-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ad6b1-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ad6b1-117">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-117">The label is in Unicode format.</span></span> <span data-ttu-id="ad6b1-118">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="ad6b1-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="ad6b1-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="ad6b1-120">Eigenschaftstag für eine Eigenschaft vom Typ PT_OBJECT, die die [IMAPIControl-Schnittstelle](imapicontroliunknown.md) implementiert.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="ad6b1-121">Wenn auf die Schaltfläche geklickt wird, ruft MAPI die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, damit die [IMAPIProp-Implementierung](imapipropiunknown.md) der Anzeigetabelle diese Eigenschaft abruft.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ad6b1-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad6b1-122">Remarks</span></span>

<span data-ttu-id="ad6b1-123">Eine **DTBLBUTTON-Struktur** beschreibt eine Schaltfläche, die einem Benutzer beim Klicken auf ein Steuerelement das Starten eines Vorgangs ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="ad6b1-124">In der Regel wird durch Klicken auf eine Schaltfläche ein modales Dialogfeld angezeigt oder eine programmgesteuerte Aufgabe aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="ad6b1-125">Dienstanbieter können alles über ein Schaltflächensteuerelement implementieren.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="ad6b1-126">Wenn die Schaltfläche eine Aufgabe basierend auf den Werten anderer Steuerelemente ausführen soll, müssen diese Steuerelemente das Flag DT_SET_IMMEDIATE haben.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="ad6b1-127">Das **ulbLpszLabel-Element** ist die Position im Speicher der Zeichenzeichenfolge, die auf der Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="ad6b1-128">Dienstanbieter können ein kaufmännisches Und -Zeichen ( ) hinzufügen, um eine Windows &amp; in der Schaltflächenbeschriftung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="ad6b1-129">Das Drücken einer Zugriffstaste hat dieselbe Auswirkung wie das Klicken auf die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="ad6b1-130">Das **ulPRControl-Element** beschreibt eine Objekteigenschaft, die beim Öffnen mit der **IMAPIProp::OpenProperty-Methode** einen Zeiger auf ein Steuerelementobjekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="ad6b1-131">Die Implementierung eines Steuerelementobjekts, das die **IMAPIControl-Schnittstelle** unterstützt, ist eine Möglichkeit, den MAPI-Featuresatz zu erweitern und den Vorgang oder die Aufgabe zu definieren, die beim Klicken auf die Schaltfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="ad6b1-132">**IMAPIControl bietet** zwei Methoden zum Bearbeiten von Schaltflächen: [GetState](imapicontrol-getstate.md) zum Deaktivieren oder Aktivieren von Schaltflächen und [Aktivieren,](imapicontrol-activate.md) um Schaltflächenklicks zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ad6b1-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="ad6b1-133">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ad6b1-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="ad6b1-134">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="ad6b1-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad6b1-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad6b1-135">See also</span></span>



[<span data-ttu-id="ad6b1-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="ad6b1-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="ad6b1-137">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ad6b1-137">MAPI Structures</span></span>](mapi-structures.md)

