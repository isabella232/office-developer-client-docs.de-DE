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
ms.openlocfilehash: 074a806a710ce8c11adba815951c93c25d8cae7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579256"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="42c5b-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="42c5b-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="42c5b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42c5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42c5b-105">Kopiert die aktuelle Nachricht in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="42c5b-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="42c5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42c5b-106">Parameters</span></span>

 <span data-ttu-id="42c5b-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="42c5b-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="42c5b-108">[in] Ein Zeiger auf den Ordner, in dem die Nachricht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="42c5b-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42c5b-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="42c5b-109">Return value</span></span>

<span data-ttu-id="42c5b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="42c5b-110">S_OK</span></span> 
  
> <span data-ttu-id="42c5b-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="42c5b-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="42c5b-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="42c5b-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="42c5b-113">Der Vorgang wird von dieser Site Nachricht nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42c5b-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42c5b-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="42c5b-114">Remarks</span></span>

<span data-ttu-id="42c5b-115">Formularobjekte Aufrufen die **IMAPIMessageSite::CopyMessage** -Methode, um die aktuelle Nachricht in einen neuen Ordner zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="42c5b-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="42c5b-116">**CopyMessage** ändert nicht die Nachricht an den Benutzer derzeit angezeigt wird, und keine Schnittstelle für die neu erstellte Nachricht an das Formular zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42c5b-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="42c5b-117">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="42c5b-117">Notes to implementers</span></span>

<span data-ttu-id="42c5b-118">Eine typische Implementierung der **CopyMessage** -Methode führt die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="42c5b-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="42c5b-119">Erstellt eine neue Nachricht für die aktuelle Nachricht in kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="42c5b-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="42c5b-120">Ruft die [IPersistMessage::Save](ipersistmessage-save.md) -Methode mit einem Zeiger auf die neue Nachricht in den _pMessage_ -Parameter und FALSE im _fSameAsLoad_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="42c5b-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="42c5b-121">Ruft die [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) -Methode NULL im _pMessage_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="42c5b-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="42c5b-122">Ruft die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode auf die neue Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="42c5b-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="42c5b-123">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern, finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="42c5b-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="42c5b-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="42c5b-124">MFCMAPI reference</span></span>

<span data-ttu-id="42c5b-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="42c5b-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="42c5b-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="42c5b-126">**File**</span></span>|<span data-ttu-id="42c5b-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="42c5b-127">**Function**</span></span>|<span data-ttu-id="42c5b-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="42c5b-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="42c5b-129">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="42c5b-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="42c5b-130">CMyMAPIFormViewer::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="42c5b-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="42c5b-131">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="42c5b-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42c5b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42c5b-132">See also</span></span>



[<span data-ttu-id="42c5b-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="42c5b-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="42c5b-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="42c5b-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="42c5b-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="42c5b-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="42c5b-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42c5b-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="42c5b-137">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="42c5b-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="42c5b-138">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="42c5b-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

