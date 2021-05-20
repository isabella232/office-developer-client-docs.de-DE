---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430000"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="d5bdd-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="d5bdd-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="d5bdd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5bdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5bdd-105">Kopiert die aktuelle Nachricht in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="d5bdd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5bdd-106">Parameters</span></span>

 <span data-ttu-id="d5bdd-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="d5bdd-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="d5bdd-108">[in] Ein Zeiger auf den Ordner, in den die Nachricht kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5bdd-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5bdd-109">Return value</span></span>

<span data-ttu-id="d5bdd-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5bdd-110">S_OK</span></span> 
  
> <span data-ttu-id="d5bdd-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d5bdd-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d5bdd-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d5bdd-113">Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5bdd-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5bdd-114">Remarks</span></span>

<span data-ttu-id="d5bdd-115">Form-Objekte rufen die **IMAPIMessageSite::CopyMessage-Methode** auf, um die aktuelle Nachricht in einen neuen Ordner zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="d5bdd-116">**CopyMessage** ändert die Nachricht, die dem Benutzer derzeit angezeigt wird, nicht, und es wird keine Schnittstelle für die neu erstellte Nachricht an das Formular zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d5bdd-117">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d5bdd-117">Notes to implementers</span></span>

<span data-ttu-id="d5bdd-118">Eine typische Implementierung der **CopyMessage-Methode** führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="d5bdd-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="d5bdd-119">Erstellt eine neue Nachricht, in die die aktuelle Nachricht kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="d5bdd-120">Ruft die [IPersistMessage::Save-Methode](ipersistmessage-save.md) mit einem Zeiger auf die neue Nachricht im  _pMessage-Parameter_ und FALSE im  _fSameAsLoad-Parameter_ auf.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="d5bdd-121">Ruft die [IPersistMessage::SaveCompleted-Methode](ipersistmessage-savecompleted.md) auf, und übergeben Sie NULL im _pMessage-Parameter._</span><span class="sxs-lookup"><span data-stu-id="d5bdd-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="d5bdd-122">Ruft die [IMAPIProp::SaveChanges-Methode für](imapiprop-savechanges.md) die neue Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="d5bdd-123">Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d5bdd-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d5bdd-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d5bdd-124">MFCMAPI reference</span></span>

<span data-ttu-id="d5bdd-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d5bdd-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d5bdd-126">**File**</span></span>|<span data-ttu-id="d5bdd-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d5bdd-127">**Function**</span></span>|<span data-ttu-id="d5bdd-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d5bdd-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5bdd-129">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d5bdd-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d5bdd-130">CMyMAPIFormViewer::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="d5bdd-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="d5bdd-131">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d5bdd-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5bdd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5bdd-132">See also</span></span>



[<span data-ttu-id="d5bdd-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d5bdd-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="d5bdd-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="d5bdd-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="d5bdd-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="d5bdd-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="d5bdd-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5bdd-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d5bdd-137">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d5bdd-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d5bdd-138">MAPI-Formularschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d5bdd-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

