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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01bdf6cdde864d1ea4ed19dfeb01a96236dc9c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792137"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="78476-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="78476-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="78476-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="78476-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="78476-105">Gibt an, dass eine Änderung in den Status des Formular-Viewers aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="78476-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="78476-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78476-106">Parameters</span></span>

 <span data-ttu-id="78476-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="78476-107">_ulDir_</span></span>
  
> <span data-ttu-id="78476-108">[in] Eine Bitmaske aus Flags, die Informationen zur Änderung bereitstellt, die in die Ereignisanzeige und die erwartete Antwort im Format aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="78476-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="78476-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="78476-109">The following flags can be set:</span></span>
    
<span data-ttu-id="78476-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="78476-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="78476-111">Es ist eine Nachricht nächste oder vorherige in einer anderen Kategorie.</span><span class="sxs-lookup"><span data-stu-id="78476-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="78476-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="78476-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="78476-113">Das Formular sollte eine Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="78476-113">The form should display a user interface.</span></span> <span data-ttu-id="78476-114">Wenn dieses Flag nicht festgelegt ist, sollte das Formular unterdrückt eine Benutzeroberfläche anzeigen, auch als Antwort auf ein Verb, das in der Regel verursacht eine Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="78476-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="78476-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="78476-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="78476-116">Das Formular ist für den Betrachter Formular gebunden sein.</span><span class="sxs-lookup"><span data-stu-id="78476-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="78476-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="78476-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="78476-118">Es ist eine nächste Nachricht im Formular-Viewer.</span><span class="sxs-lookup"><span data-stu-id="78476-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="78476-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="78476-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="78476-120">Es ist eine vorherige Nachricht im Formular-Viewer.</span><span class="sxs-lookup"><span data-stu-id="78476-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="78476-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="78476-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="78476-122">Löschen Sie, senden Sie, und verschieben Sie Vorgänge deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="78476-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="78476-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="78476-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="78476-124">Es ist eine nächste oder Vorherige ungelesene Nachricht im Formular-Viewer.</span><span class="sxs-lookup"><span data-stu-id="78476-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78476-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="78476-125">Return value</span></span>

<span data-ttu-id="78476-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="78476-126">S_OK</span></span> 
  
> <span data-ttu-id="78476-127">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="78476-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78476-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78476-128">Remarks</span></span>

<span data-ttu-id="78476-129">Formular Viewer rufen Sie die **IMAPIFormAdviseSink::OnChange** -Methode, um das Formular über eine Änderung in einem Viewer Status zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="78476-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="78476-130">In der Regel ist die einzige Änderung festlegen oder Löschen der basierend auf dem Vorhandensein oder Abwesenheit einer nächsten oder vorherigen Nachricht im Viewer VCSTATUS_NEXT oder VCSTATUS_PREVIOUS-Flag.</span><span class="sxs-lookup"><span data-stu-id="78476-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="78476-131">Das Form-Objekt wird entsprechend, klicken Sie dann aktiviert, oder der nächsten oder vorherigen Aktionen unterstützten deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="78476-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="78476-132">Die Einstellungen VCSTATUS_MODAL und VCSTATUS_INTERACTIVE können nicht in einem Ansichtskontext ändern, nachdem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="78476-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="78476-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="78476-133">Notes to implementers</span></span>

<span data-ttu-id="78476-134">Die Implementierung dieser Methode ist die Merkmale des Formulars vollständig abhängig.</span><span class="sxs-lookup"><span data-stu-id="78476-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="78476-135">Die meisten Formularobjekte mit dieser Methode können Sie ihre-Benutzeroberfläche (beispielsweise zum Aktivieren oder deaktivieren Menübefehle oder Schaltflächen entsprechend der Viewer Status Flags-Parameter) ändern.</span><span class="sxs-lookup"><span data-stu-id="78476-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78476-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78476-136">See also</span></span>



[<span data-ttu-id="78476-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="78476-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="78476-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78476-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

