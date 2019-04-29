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
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="a0e7f-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="a0e7f-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="a0e7f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0e7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0e7f-105">Gibt an, ob das Formular die Nachrichtenklasse der nächsten anzuzeigende Nachricht behandeln kann.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="a0e7f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0e7f-106">Parameters</span></span>

 <span data-ttu-id="a0e7f-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a0e7f-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="a0e7f-108">in Ein Zeiger auf die Nachrichtenklasse der nächsten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="a0e7f-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="a0e7f-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="a0e7f-110">in Eine Bitmaske von Client definierten oder Anbieter definierten Flags, die von der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der nächsten anzuzeigende Nachricht kopiert werden und Status Informationen zur Inhaltstabelle bereitstellen, die die Nachricht enthält. in.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="a0e7f-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="a0e7f-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="a0e7f-112">in Ein Zeiger auf eine Bitmaske von Flags, die von der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der nächsten anzuzeigende Nachricht kopiert und den aktuellen Status der Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="a0e7f-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="a0e7f-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="a0e7f-114">Out Ein Zeiger auf einen Zeiger auf die [IPersistMessage](ipersistmessageiunknown.md) -Implementierung für das Form-Objekt, das für das neue Formular verwendet wird, wenn ein neues Formular erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="a0e7f-115">Ein Zeiger auf NULL kann zurückgegeben werden, wenn das aktuelle Formularobjekt verwendet werden kann, um die nächste Nachricht anzuzeigen und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a0e7f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0e7f-116">Return value</span></span>

<span data-ttu-id="a0e7f-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0e7f-117">S_OK</span></span> 
  
> <span data-ttu-id="a0e7f-118">Die Benachrichtigung war erfolgreich, und das Formular kann die nächste Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="a0e7f-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a0e7f-119">S_FALSE</span></span> 
  
> <span data-ttu-id="a0e7f-120">Das Formular verarbeitet die Nachrichtenklasse der nächsten Nachricht nicht.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0e7f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0e7f-121">Remarks</span></span>

<span data-ttu-id="a0e7f-122">Formular Betrachter rufen die **IMAPIFormAdviseSink:: OnActivateNext** -Methode auf, um zu bestimmen, ob die nächste Nachricht in einem Ordner angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="a0e7f-123">Bei der nächsten Nachricht kann es sich um eine beliebige Klasse handeln, aber in der Regel handelt es sich um eine Klasse oder eine zugehörige Klasse.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="a0e7f-124">Dadurch wird der Prozess des Lesens mehrerer Nachrichten derselben Klasse effizienter, indem Clientanwendungen nach Möglichkeit die Wiederverwendung von Formularobjekten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="a0e7f-125">Die meisten Form-Objekte verwenden die Nachrichtenklasse, auf die durch den _lpszMessageClass_ -Parameter verwiesen wird, um zu bestimmen, ob Sie die nächste Nachricht verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="a0e7f-126">In der Regel kann ein Formular Nachrichten verarbeiten, die zu Klassen gehören, deren Standardklasse eine Unterklasse ist, zusätzlich zu Nachrichten, die zur Standardklasse gehören.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="a0e7f-127">Ein Formular kann jedoch andere Faktoren verwenden, um zu bestimmen, ob eine Nachricht verarbeitet werden kann, beispielsweise den Status "gesendet" oder "nicht gesendet" der nächsten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a0e7f-128">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="a0e7f-128">Notes to implementers</span></span>

<span data-ttu-id="a0e7f-129">Geben Sie S_OK und NULL im _ppPersistMessage_ -Parameter zurück, wenn das Formular die Nachrichtenklasse verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="a0e7f-130">Führen Sie die folgenden Schritte aus, wenn das Formular ein neues Formular erstellen kann, das die Nachricht verarbeiten kann, die vom Formular nicht verarbeitet werden konnte:</span><span class="sxs-lookup"><span data-stu-id="a0e7f-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="a0e7f-131">Rufen Sie die Klassen Factory des Formulars auf, um eine Instanz eines neuen Form-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="a0e7f-132">Speichern Sie diese Instanz im Inhalt des _ppPersistMessage_ -Zeiger-Parameters.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="a0e7f-133">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-133">Return S_OK.</span></span>
    
<span data-ttu-id="a0e7f-134">Der Formular-Viewer lädt die Nachricht mithilfe der [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode, die zu dem Objekt gehört, auf das durch _ppPersistMessage_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="a0e7f-135">Wenn weder das Formular noch ein Formular, das Sie erstellen können, die nächste Nachricht verarbeiten kann, geben Sie S_FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="a0e7f-136">Im Allgemeinen sollten Formulare diesen Wert jedoch nicht zurückgeben, da dadurch die Leistung im Formular Betrachter vermindert wird.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a0e7f-137">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a0e7f-137">MFCMAPI reference</span></span>

<span data-ttu-id="a0e7f-138">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a0e7f-139">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a0e7f-139">**File**</span></span>|<span data-ttu-id="a0e7f-140">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a0e7f-140">**Function**</span></span>|<span data-ttu-id="a0e7f-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a0e7f-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0e7f-142">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="a0e7f-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a0e7f-143">CMyMAPIFormViewer:: ActivateNext</span><span class="sxs-lookup"><span data-stu-id="a0e7f-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="a0e7f-144">MFCMAPI verwendet die **IMAPIFormAdviseSink:: OnActivateNext** -Methode, um die [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) -Methode zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="a0e7f-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0e7f-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0e7f-145">See also</span></span>



[<span data-ttu-id="a0e7f-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="a0e7f-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="a0e7f-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0e7f-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="a0e7f-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="a0e7f-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="a0e7f-149">Kanonische PidTagMessageFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a0e7f-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="a0e7f-150">Kanonische Pidtagmessagestatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a0e7f-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="a0e7f-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0e7f-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="a0e7f-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a0e7f-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

