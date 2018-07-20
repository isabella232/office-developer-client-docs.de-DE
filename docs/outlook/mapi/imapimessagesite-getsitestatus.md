---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792215"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="ce24a-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="ce24a-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="ce24a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce24a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce24a-105">Gibt Informationen aus einem Objekt "Message" Website zur Nachricht der Website Funktionen für die aktuelle Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="ce24a-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="ce24a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce24a-106">Parameters</span></span>

 <span data-ttu-id="ce24a-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="ce24a-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="ce24a-108">[out] Ein Zeiger auf eine Bitmaske aus Flags, die Informationen zum Nachrichtenstatus bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ce24a-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="ce24a-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ce24a-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ce24a-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="ce24a-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="ce24a-111">Die Nachricht kann kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce24a-111">The message can be copied.</span></span> 
    
<span data-ttu-id="ce24a-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="ce24a-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="ce24a-113">Die Nachricht kann gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ce24a-113">The message can be deleted.</span></span>
    
<span data-ttu-id="ce24a-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="ce24a-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="ce24a-115">Wenn gelöscht, wird eine Meldung in einem Ordner **Gelöschte Elemente** in den Nachrichtenspeicher anstelle von den Nachrichtenspeicher sofort entfernt wird verschoben.</span><span class="sxs-lookup"><span data-stu-id="ce24a-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="ce24a-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="ce24a-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="ce24a-117">Die Nachricht kann verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="ce24a-117">The message can be moved.</span></span>
    
<span data-ttu-id="ce24a-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="ce24a-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="ce24a-119">Eine neue Nachricht kann erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ce24a-119">A new message can be created.</span></span>
    
<span data-ttu-id="ce24a-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="ce24a-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="ce24a-121">Die Nachricht kann gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ce24a-121">The message can be saved.</span></span>
    
<span data-ttu-id="ce24a-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="ce24a-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="ce24a-123">Die Nachricht kann gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce24a-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce24a-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce24a-124">Return value</span></span>

<span data-ttu-id="ce24a-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce24a-125">S_OK</span></span> 
  
> <span data-ttu-id="ce24a-126">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ce24a-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce24a-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce24a-127">Remarks</span></span>

<span data-ttu-id="ce24a-128">Formularobjekte Aufrufen die **IMAPIMessageSite::GetSiteStatus** -Methode, um die Nachricht Standortobjekt Funktionen für die aktuelle Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ce24a-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="ce24a-129">Die Kennzeichen, die in der _LpulStatus_ -Parameter zurückgegeben liefern Informationen zur Nachricht-Website.</span><span class="sxs-lookup"><span data-stu-id="ce24a-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="ce24a-130">In der Regel ein Formular aktiviert oder deaktiviert die Menübefehle, je nach Informationen, die die Kennzeichen bereitstellen zu den Funktionen der Nachricht Website-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="ce24a-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="ce24a-131">Wenn eine neue Nachricht durch die [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) -Methode oder die [IPersistMessage::Load](ipersistmessage-load.md) -Methode in einem Formular geladen wird, müssen die Status-Kennzeichen überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce24a-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="ce24a-132">Einige Nachricht Websiteobjekte, insbesondere schreibgeschützt, lassen Sie nicht Nachrichten gespeichert oder gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce24a-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ce24a-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ce24a-133">Notes to implementers</span></span>

<span data-ttu-id="ce24a-134">Die Methode **IMAPIMessageSite::GetSiteStatus** erfordern möglicherweise die Client-Anwendung, um zu bestimmen, welche Vorgänge können oder nicht auf die aktuelle Nachricht durchgeführt werden einige Berechnung ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce24a-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="ce24a-135">In der Regel, die umfasst die Statuszeile für die aktuelle Nachricht Nachricht Speicheranbieter betrachten oder den Anbieter anmelden, um zu bestimmen, welche Aktionen Abfragen kann die Client-Anwendung mithilfe des Nachrichtenspeichers ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce24a-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="ce24a-136">Überprüfen Sie beispielsweise um festzustellen, ob das Flag MAPI_DELETE_IS_MOVE zurückzugeben, das Nachricht Store-Objekt **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))-Eigenschaft, um festzustellen, ob es ein Ordner **Gelöschte Elemente** in ist der Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="ce24a-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="ce24a-137">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="ce24a-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce24a-138">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="ce24a-138">MFCMAPI reference</span></span>

<span data-ttu-id="ce24a-139">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ce24a-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce24a-140">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ce24a-140">**File**</span></span>|<span data-ttu-id="ce24a-141">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ce24a-141">**Function**</span></span>|<span data-ttu-id="ce24a-142">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ce24a-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce24a-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ce24a-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ce24a-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="ce24a-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="ce24a-145">MFCMAPI (engl.) verwendet die **IMAPIMessageSite::GetSiteStatus** -Methode, um den Status der angegebenen Website zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ce24a-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="ce24a-146">Es kann VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE oder VCSTATUS_SUBMIT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ce24a-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce24a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce24a-147">See also</span></span>



[<span data-ttu-id="ce24a-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="ce24a-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="ce24a-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="ce24a-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="ce24a-150">PidTagIpmWastebasketEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ce24a-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="ce24a-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce24a-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="ce24a-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ce24a-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ce24a-153">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="ce24a-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

