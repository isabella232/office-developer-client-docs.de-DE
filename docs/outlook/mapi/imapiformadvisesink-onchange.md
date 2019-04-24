---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286628"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="4e813-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="4e813-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="4e813-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e813-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e813-105">Gibt an, dass eine Änderung im Status des Formular-Viewers aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4e813-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="4e813-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e813-106">Parameters</span></span>

 <span data-ttu-id="4e813-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="4e813-107">_ulDir_</span></span>
  
> <span data-ttu-id="4e813-108">in Eine Bitmaske von Flags, die Informationen zur Änderung im Viewer und zur erwarteten Antwort im Formular bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4e813-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="4e813-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4e813-109">The following flags can be set:</span></span>
    
<span data-ttu-id="4e813-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="4e813-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="4e813-111">Es gibt eine nächste oder eine vorherige Nachricht in einer anderen Kategorie.</span><span class="sxs-lookup"><span data-stu-id="4e813-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="4e813-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="4e813-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="4e813-113">Im Formular sollte eine Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4e813-113">The form should display a user interface.</span></span> <span data-ttu-id="4e813-114">Wenn dieses Flag nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche unterdrücken, auch als Reaktion auf ein Verb, das in der Regel bewirkt, dass eine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4e813-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="4e813-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="4e813-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="4e813-116">Das Formular soll an den Formular Betrachter gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="4e813-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="4e813-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="4e813-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="4e813-118">Es gibt eine nächste Nachricht im Formular-Viewer.</span><span class="sxs-lookup"><span data-stu-id="4e813-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="4e813-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="4e813-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="4e813-120">Es gibt eine vorherige Nachricht im Formular-Viewer.</span><span class="sxs-lookup"><span data-stu-id="4e813-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="4e813-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="4e813-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="4e813-122">Lösch-, Sende-und Verschiebungsvorgänge sollten deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="4e813-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="4e813-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="4e813-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="4e813-124">Es gibt eine nächste oder vorherige ungelesene Nachricht im Formular-Viewer.</span><span class="sxs-lookup"><span data-stu-id="4e813-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e813-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e813-125">Return value</span></span>

<span data-ttu-id="4e813-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e813-126">S_OK</span></span> 
  
> <span data-ttu-id="4e813-127">Die Benachrichtigung wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e813-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e813-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e813-128">Remarks</span></span>

<span data-ttu-id="4e813-129">Formular Betrachter rufen die **IMAPIFormAdviseSink:: OnChange** -Methode auf, um das Formular über eine Änderung des Status eines Viewers zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="4e813-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="4e813-130">In der Regel ist die einzige Änderung das Festlegen oder Deaktivieren des VCSTATUS_NEXT-oder VCSTATUS_PREVIOUS-Kennzeichens basierend auf dem vorhanden sein oder Fehlen einer nächsten oder einer vorherigen Nachricht im Viewer.</span><span class="sxs-lookup"><span data-stu-id="4e813-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="4e813-131">Dementsprechend aktiviert oder deaktiviert das Form-Objekt alle nächsten oder vorherigen Aktionen, die unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4e813-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="4e813-132">Die Einstellungen von VCSTATUS_MODAL und VCSTATUS_INTERACTIVE können nicht in einem Ansichtskontext geändert werden, nachdem Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4e813-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4e813-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="4e813-133">Notes to implementers</span></span>

<span data-ttu-id="4e813-134">Die spezifische Implementierung dieser Methode ist vollständig von den Details des Formulars abhängig.</span><span class="sxs-lookup"><span data-stu-id="4e813-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="4e813-135">Die meisten Formularobjekte verwenden diese Methode, um Ihre Benutzeroberfläche zu ändern (beispielsweise, um Menübefehle oder Schaltflächen so zu aktivieren oder zu deaktivieren, dass Sie mit dem Parameter Viewer Status Flags übereinstimmen).</span><span class="sxs-lookup"><span data-stu-id="4e813-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e813-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e813-136">See also</span></span>



[<span data-ttu-id="4e813-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="4e813-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="4e813-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e813-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

