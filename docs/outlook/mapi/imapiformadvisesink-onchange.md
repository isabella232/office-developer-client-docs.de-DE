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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431897"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="0b4ad-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="0b4ad-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="0b4ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b4ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b4ad-105">Gibt an, dass eine Änderung im Status der Formularanzeige aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="0b4ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b4ad-106">Parameters</span></span>

 <span data-ttu-id="0b4ad-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="0b4ad-107">_ulDir_</span></span>
  
> <span data-ttu-id="0b4ad-108">[in] Eine Bitmaske mit Flags, die Informationen über die im Viewer aufgetretene Änderung und die erwartete Antwort im Formular enthält.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="0b4ad-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0b4ad-109">The following flags can be set:</span></span>
    
<span data-ttu-id="0b4ad-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="0b4ad-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="0b4ad-111">Es gibt eine nächste oder vorherige Nachricht in einer anderen Kategorie.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="0b4ad-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="0b4ad-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="0b4ad-113">Das Formular sollte eine Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-113">The form should display a user interface.</span></span> <span data-ttu-id="0b4ad-114">Wenn dieses Kennzeichen nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche unterdrücken, auch als Reaktion auf ein Verb, das normalerweise dazu führt, dass eine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="0b4ad-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="0b4ad-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="0b4ad-116">Das Formular soll modal für die Formularanzeige sein.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="0b4ad-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="0b4ad-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="0b4ad-118">Es gibt eine nächste Nachricht in der Formularanzeige.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="0b4ad-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="0b4ad-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="0b4ad-120">Es ist eine vorherige Nachricht in der Formularanzeige.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="0b4ad-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="0b4ad-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="0b4ad-122">Lösch-, Absenden- und Verschiebevorgänge sollten deaktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="0b4ad-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="0b4ad-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="0b4ad-124">Es gibt eine nächste oder vorherige ungelesene Nachricht in der Formularanzeige.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0b4ad-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b4ad-125">Return value</span></span>

<span data-ttu-id="0b4ad-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b4ad-126">S_OK</span></span> 
  
> <span data-ttu-id="0b4ad-127">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b4ad-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b4ad-128">Remarks</span></span>

<span data-ttu-id="0b4ad-129">Formularbetrachter rufen die **IMAPIFormAdviseSink::OnChange-Methode** auf, um das Formular über eine Änderung des Status eines Betrachters zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="0b4ad-130">In der Regel ist die einzige Änderung das Festlegen oder Löschen der VCSTATUS_NEXT oder VCSTATUS_PREVIOUS basierend auf dem Vorhandensein oder Fehlen einer nächsten oder vorherigen Nachricht im Viewer.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="0b4ad-131">Entsprechend aktiviert oder deaktiviert das Formularobjekt dann alle nächsten oder vorherigen Aktionen, die es unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="0b4ad-132">Die Einstellungen von VCSTATUS_MODAL und VCSTATUS_INTERACTIVE können sich in einem Ansichtskontext nicht ändern, nachdem er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0b4ad-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="0b4ad-133">Notes to implementers</span></span>

<span data-ttu-id="0b4ad-134">Die spezifische Implementierung dieser Methode hängt vollständig von den Besonderheiten des Formulars ab.</span><span class="sxs-lookup"><span data-stu-id="0b4ad-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="0b4ad-135">Die meisten Formularobjekte verwenden diese Methode, um ihre Benutzeroberfläche zu ändern (z. B. zum Aktivieren oder Deaktivieren von Menübefehlen oder Schaltflächen, die mit dem Parameter "Viewer status flags" übereinstimmen).</span><span class="sxs-lookup"><span data-stu-id="0b4ad-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b4ad-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b4ad-136">See also</span></span>



[<span data-ttu-id="0b4ad-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="0b4ad-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="0b4ad-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b4ad-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

