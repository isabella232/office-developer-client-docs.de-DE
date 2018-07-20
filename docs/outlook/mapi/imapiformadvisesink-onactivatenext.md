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
ms.openlocfilehash: 3ce4d57ab4837f40ffbc898fde68e44cc802676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792127"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="ba607-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="ba607-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="ba607-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba607-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba607-105">Gibt an, ob das Formular die Nachrichtenklasse für die nächste anzuzeigende Meldung verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="ba607-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="ba607-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba607-106">Parameters</span></span>

 <span data-ttu-id="ba607-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="ba607-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="ba607-108">[in] Ein Zeiger auf die Nachrichtenklasse des nächsten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ba607-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="ba607-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="ba607-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="ba607-110">[in] Eine Bitmaske vom Client definiert oder vom Anbieter definiertes Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft die nächste Nachricht angezeigt kopiert, bereitstellt, die Statusinformationen bezüglich der Inhaltstabelle, dass die Nachricht enthalten ist. in.</span><span class="sxs-lookup"><span data-stu-id="ba607-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="ba607-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="ba607-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="ba607-112">[in] Ein Zeiger auf eine Bitmaske aus Flags aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft, die an die nächste Nachricht kopiert gibt den aktuellen Status der Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="ba607-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="ba607-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="ba607-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="ba607-114">[out] Ein Zeiger auf einen Zeiger auf die [IPersistMessage](ipersistmessageiunknown.md) -Implementierung für das Form-Objekt für das neue Formular verwendet wird, wenn ein neues Formular erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ba607-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="ba607-115">Ein Zeiger auf NULL kann zurückgegeben werden, wenn das aktuelle Formularobjekt zum Anzeigen und speichern die nächste Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba607-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ba607-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba607-116">Return value</span></span>

<span data-ttu-id="ba607-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba607-117">S_OK</span></span> 
  
> <span data-ttu-id="ba607-118">Die Benachrichtigung war erfolgreich, und das Formular kann die nächste Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ba607-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="ba607-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ba607-119">S_FALSE</span></span> 
  
> <span data-ttu-id="ba607-120">Das Formular behandelt die Nachrichtenklasse für die nächste Nachricht nicht.</span><span class="sxs-lookup"><span data-stu-id="ba607-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba607-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba607-121">Remarks</span></span>

<span data-ttu-id="ba607-122">Formular Viewer rufen Sie die **IMAPIFormAdviseSink::OnActivateNext** -Methode, mit denen das Formular zu bestimmen, ob die nächste Nachricht in einem Ordner angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="ba607-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="ba607-123">Die nächste Nachricht konnte eine Nachricht einer beliebigen Klasse werden, jedoch ist normalerweise der gleichen Klasse oder einer verknüpften-Klasse.</span><span class="sxs-lookup"><span data-stu-id="ba607-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="ba607-124">Dadurch wird das Lesen von mehrere Nachrichten von der gleichen Klasse effizienter durch Clientanwendungen Formularobjekte nach Möglichkeit wiederverwenden aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ba607-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="ba607-125">Die meisten Formularobjekte werden die Nachrichtenklasse auf das durch den Parameter _LpszMessageClass_ verwenden, um festzustellen, ob sie die nächste Nachricht verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="ba607-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="ba607-126">In der Regel kann ein Formular Verarbeitung von Nachrichten, die zu Klassen, von denen Standard-Klasse des Formulars eine Unterklasse, zusätzlich zu Nachrichten gehören, die der Default-Klasse angehören.</span><span class="sxs-lookup"><span data-stu-id="ba607-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="ba607-127">Ein Formular kann jedoch andere Faktoren verwenden, um ohne Frage zu bestimmen, ob eine Nachricht kann, wie beispielsweise der Status gesendet, der die nächste Nachricht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ba607-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ba607-128">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ba607-128">Notes to implementers</span></span>

<span data-ttu-id="ba607-129">Zurückgeben Sie S_OK und NULL in der _PpPersistMessage_ -Parameter, wenn das Formular die Nachrichtenklasse verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba607-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="ba607-130">Wenn das Formular ein neues Formular, das die Nachricht verarbeitet werden können, die das Formular nicht behandelt wird erstellen kann, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="ba607-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="ba607-131">Rufen Sie das Formular Klassenfactory zum Erstellen einer Instanz eines neuen Formulars-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ba607-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="ba607-132">Speichern Sie diese Instanz, in den Inhalt des Parameters Zeiger _PpPersistMessage_ .</span><span class="sxs-lookup"><span data-stu-id="ba607-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="ba607-133">Geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ba607-133">Return S_OK.</span></span>
    
<span data-ttu-id="ba607-134">Der Formular-Viewer lädt die Nachricht mit der [IPersistMessage::Load](ipersistmessage-load.md) -Methode, die auf das Objekt, auf das _PpPersistMessage_gehört.</span><span class="sxs-lookup"><span data-stu-id="ba607-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="ba607-135">Wenn weder das Formular noch ein Formular, das Sie erstellen können die nächste Nachricht behandeln, zurückgeben Sie S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="ba607-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="ba607-136">Allerdings sollte im Allgemeinen Formulare nicht zurückgegeben werden, dass dieser Wert, da dadurch die Leistung im Formular-Viewer verringert.</span><span class="sxs-lookup"><span data-stu-id="ba607-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba607-137">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="ba607-137">MFCMAPI reference</span></span>

<span data-ttu-id="ba607-138">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ba607-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba607-139">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ba607-139">**File**</span></span>|<span data-ttu-id="ba607-140">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ba607-140">**Function**</span></span>|<span data-ttu-id="ba607-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ba607-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba607-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ba607-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ba607-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ba607-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="ba607-144">MFCMAPI (engl.) verwendet die **IMAPIFormAdviseSink::OnActivateNext** -Methode, um die [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) -Methode zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ba607-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba607-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba607-145">See also</span></span>



[<span data-ttu-id="ba607-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ba607-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="ba607-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba607-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="ba607-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="ba607-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="ba607-149">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ba607-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="ba607-150">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ba607-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="ba607-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba607-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="ba607-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ba607-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

