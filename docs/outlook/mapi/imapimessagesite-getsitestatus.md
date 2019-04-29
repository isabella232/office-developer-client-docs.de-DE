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
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430126"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="9df71-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="9df71-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="9df71-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9df71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9df71-105">Gibt Informationen aus einem Nachrichtenwebsite Objekt über die Funktionen der Nachrichtenwebsite für die aktuelle Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="9df71-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="9df71-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9df71-106">Parameters</span></span>

 <span data-ttu-id="9df71-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="9df71-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="9df71-108">Out Ein Zeiger auf eine Bitmaske von Flags, die Informationen zum Status der Nachricht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9df71-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="9df71-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9df71-109">The following flags can be set:</span></span>
    
<span data-ttu-id="9df71-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="9df71-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="9df71-111">Die Nachricht kann kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="9df71-111">The message can be copied.</span></span> 
    
<span data-ttu-id="9df71-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="9df71-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="9df71-113">Die Nachricht kann gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9df71-113">The message can be deleted.</span></span>
    
<span data-ttu-id="9df71-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="9df71-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="9df71-115">Nach dem Löschen wird eine Nachricht in einen Ordner " **Gelöschte Elemente** " im Nachrichtenspeicher verschoben, anstatt Sie sofort aus dem Nachrichtenspeicher zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9df71-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="9df71-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="9df71-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="9df71-117">Die Nachricht kann verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="9df71-117">The message can be moved.</span></span>
    
<span data-ttu-id="9df71-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="9df71-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="9df71-119">Eine neue Nachricht kann erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9df71-119">A new message can be created.</span></span>
    
<span data-ttu-id="9df71-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="9df71-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="9df71-121">Die Nachricht kann gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9df71-121">The message can be saved.</span></span>
    
<span data-ttu-id="9df71-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="9df71-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="9df71-123">Die Nachricht kann übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9df71-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9df71-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9df71-124">Return value</span></span>

<span data-ttu-id="9df71-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="9df71-125">S_OK</span></span> 
  
> <span data-ttu-id="9df71-126">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9df71-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9df71-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9df71-127">Remarks</span></span>

<span data-ttu-id="9df71-128">Formularobjekte rufen die **IMAPIMessageSite:: GetSiteStatus** -Methode auf, um die Funktionen des Nachrichtenwebsite Objekts für die aktuelle Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9df71-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="9df71-129">Die im Parameter _lpulStatus_ zurückgegebenen Flags enthalten Informationen zur Nachrichtenwebsite.</span><span class="sxs-lookup"><span data-stu-id="9df71-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="9df71-130">In der Regel aktiviert oder deaktiviert ein Formular Menübefehle, je nachdem, welche Informationen die Flags über die Funktionen der Nachrichtenwebsite Implementierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9df71-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="9df71-131">Wenn eine neue Nachricht von der [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) -Methode oder der [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode in ein Formular geladen wird, müssen die Status-Flags überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="9df71-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="9df71-132">Bei einigen Nachrichtenwebsite Objekten, insbesondere schreibgeschützten Objekten, können keine Nachrichten gespeichert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9df71-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9df71-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="9df71-133">Notes to implementers</span></span>

<span data-ttu-id="9df71-134">Die **IMAPIMessageSite:: GetSiteStatus** -Methode erfordert möglicherweise eine Berechnung der Clientanwendung, um zu bestimmen, welche Vorgänge für die aktuelle Nachricht ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9df71-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="9df71-135">In der Regel müssen Sie sich die Statuszeile des Nachrichtenspeicher Anbieters der aktuellen Nachricht ansehen oder den Speicheranbieter Abfragen, um zu bestimmen, welche Aktionen die Clientanwendung mithilfe des Nachrichtenspeichers ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="9df71-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="9df71-136">Um beispielsweise zu bestimmen, ob das MAPI_DELETE_IS_MOVE-Flag zurückgegeben werden soll, überprüfen Sie die **PR_IPM_WASTEBASKET_ENTRYID** ([pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeicher Objekts, um festzustellen, ob ein Ordner " **Gelöschte Elemente** " in der Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="9df71-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="9df71-137">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9df71-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9df71-138">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="9df71-138">MFCMAPI reference</span></span>

<span data-ttu-id="9df71-139">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9df71-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9df71-140">**Datei**</span><span class="sxs-lookup"><span data-stu-id="9df71-140">**File**</span></span>|<span data-ttu-id="9df71-141">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="9df71-141">**Function**</span></span>|<span data-ttu-id="9df71-142">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9df71-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9df71-143">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="9df71-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="9df71-144">CMyMAPIFormViewer:: GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="9df71-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="9df71-145">MFCMAPI verwendet die **IMAPIMessageSite:: GetSiteStatus** -Methode, um den Status der angegebenen Website abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9df71-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="9df71-146">Es kann VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE oder VCSTATUS_SUBMIT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9df71-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9df71-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9df71-147">See also</span></span>



[<span data-ttu-id="9df71-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="9df71-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="9df71-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="9df71-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="9df71-150">Kanonische Pidtagipmwastebasketentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9df71-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="9df71-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9df71-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="9df71-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="9df71-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9df71-153">MAPI-Formular Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9df71-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

