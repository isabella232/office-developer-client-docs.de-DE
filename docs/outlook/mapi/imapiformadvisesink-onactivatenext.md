---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411764"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="fe29e-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="fe29e-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="fe29e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe29e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe29e-105">Gibt an, ob das Formular die Nachrichtenklasse der nächsten anzuzeigenden Nachricht verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="fe29e-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="fe29e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe29e-106">Parameters</span></span>

 <span data-ttu-id="fe29e-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="fe29e-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="fe29e-108">[in] Ein Zeiger auf die Nachrichtenklasse der nächsten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fe29e-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="fe29e-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="fe29e-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="fe29e-110">[in] Eine Bitmaske mit client- oder anbieterdefinierten Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der nächsten anzuzeigenden Nachricht kopiert werden, die Statusinformationen zur Inhaltstabelle enthält, in der die Nachricht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fe29e-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="fe29e-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="fe29e-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="fe29e-112">[in] Ein Zeiger auf eine Bitmaske von **Flags,** die aus der PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der nächsten anzuzeigenden Nachricht kopiert wurden, die den aktuellen Status der Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="fe29e-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="fe29e-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="fe29e-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="fe29e-114">[out] Ein Zeiger auf einen Zeiger auf die [IPersistMessage-Implementierung](ipersistmessageiunknown.md) für das Formularobjekt, das für das neue Formular verwendet wird, wenn ein neues Formular erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fe29e-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="fe29e-115">Ein Zeiger auf NULL kann zurückgegeben werden, wenn das aktuelle Formularobjekt zum Anzeigen und Speichern der nächsten Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe29e-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fe29e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe29e-116">Return value</span></span>

<span data-ttu-id="fe29e-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe29e-117">S_OK</span></span> 
  
> <span data-ttu-id="fe29e-118">Die Benachrichtigung war erfolgreich, und das Formular kann die nächste Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fe29e-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="fe29e-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fe29e-119">S_FALSE</span></span> 
  
> <span data-ttu-id="fe29e-120">Das Formular verarbeiten nicht die Nachrichtenklasse der nächsten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fe29e-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe29e-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe29e-121">Remarks</span></span>

<span data-ttu-id="fe29e-122">Formularbetrachter rufen die **IMAPIFormAdviseSink::OnActivateNext-Methode** auf, um dem Formular zu helfen, zu bestimmen, ob die nächste Nachricht in einem Ordner angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe29e-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="fe29e-123">Die nächste Nachricht kann eine Nachricht einer beliebigen Klasse sein, aber in der Regel handelt es sich um dieselbe Klasse oder eine verwandte Klasse.</span><span class="sxs-lookup"><span data-stu-id="fe29e-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="fe29e-124">Dadurch wird das Lesen mehrerer Nachrichten derselben Klasse effizienter, indem Clientanwendungen die Wiederverwendung von Formularobjekten nach Möglichkeit ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fe29e-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="fe29e-125">Die meisten Formularobjekte verwenden die Nachrichtenklasse, auf die der  _lpszMessageClass-Parameter_ verweist, um zu bestimmen, ob sie die nächste Nachricht verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="fe29e-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="fe29e-126">In der Regel kann ein Formular Nachrichten verarbeiten, die zu Klassen gehören, deren Standardklasse des Formulars eine Unterklasse ist, zusätzlich zu Nachrichten, die zur Standardklasse gehören.</span><span class="sxs-lookup"><span data-stu-id="fe29e-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="fe29e-127">Ein Formular kann jedoch andere Faktoren verwenden, um ohne Frage zu bestimmen, ob eine Nachricht verarbeitet werden kann, z. B. den gesendeten oder nicht gesendeten Status der nächsten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fe29e-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fe29e-128">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="fe29e-128">Notes to implementers</span></span>

<span data-ttu-id="fe29e-129">Geben S_OK und NULL im  _ppPersistMessage-Parameter_ zurück, wenn das Formular die Nachrichtenklasse verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="fe29e-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="fe29e-130">Wenn das Formular ein neues Formular erstellen kann, das die Nachricht verarbeiten kann, die das Formular nicht verarbeiten kann, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="fe29e-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="fe29e-131">Rufen Sie die Klassen factory des Formulars auf, um eine Instanz eines neuen Formularobjekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fe29e-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="fe29e-132">Store instanz im Inhalt des _ppPersistMessage-Zeigerparameters._</span><span class="sxs-lookup"><span data-stu-id="fe29e-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="fe29e-133">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="fe29e-133">Return S_OK.</span></span>
    
<span data-ttu-id="fe29e-134">Die Formularanzeige wird die Nachricht mithilfe der [IPersistMessage::Load-Methode](ipersistmessage-load.md) laden, die zu dem Objekt gehört, auf das _von ppPersistMessage verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="fe29e-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="fe29e-135">Wenn weder das Formular noch ein Formular, das Sie erstellen können, die nächste Nachricht verarbeiten kann, geben Sie S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="fe29e-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="fe29e-136">Im Allgemeinen sollten Formulare diesen Wert jedoch nicht zurückgeben, da dadurch die Leistung in der Formularanzeige verringert wird.</span><span class="sxs-lookup"><span data-stu-id="fe29e-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fe29e-137">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="fe29e-137">MFCMAPI reference</span></span>

<span data-ttu-id="fe29e-138">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fe29e-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fe29e-139">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fe29e-139">**File**</span></span>|<span data-ttu-id="fe29e-140">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fe29e-140">**Function**</span></span>|<span data-ttu-id="fe29e-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fe29e-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe29e-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fe29e-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fe29e-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="fe29e-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="fe29e-144">MFCMAPI verwendet die **IMAPIFormAdviseSink::OnActivateNext-Methode,** um die [IMAPIViewContext::ActivateNext-Methode zu](imapiviewcontext-activatenext.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="fe29e-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe29e-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe29e-145">See also</span></span>



[<span data-ttu-id="fe29e-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="fe29e-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="fe29e-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe29e-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="fe29e-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="fe29e-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="fe29e-149">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fe29e-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="fe29e-150">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fe29e-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="fe29e-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe29e-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="fe29e-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="fe29e-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

