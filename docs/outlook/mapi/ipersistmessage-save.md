---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 222d8257a802739ee8e513a0ea95a13f4b99322e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792736"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="56b10-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="56b10-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="56b10-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56b10-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56b10-105">Speichert eine überarbeitete Formular an die Nachricht aus der es geladen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="56b10-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="56b10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56b10-106">Parameters</span></span>

 <span data-ttu-id="56b10-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="56b10-107">_pMessage_</span></span>
  
> <span data-ttu-id="56b10-108">[in] Ein Zeiger auf die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="56b10-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="56b10-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="56b10-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="56b10-110">[in] True, um anzugeben, dass die Nachricht, auf das verwiesen ist durch _pMessage_ die Nachricht aus der das Formular geladen oder erstellt wurde. andernfalls, FALSE.</span><span class="sxs-lookup"><span data-stu-id="56b10-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="56b10-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="56b10-111">Return value</span></span>

<span data-ttu-id="56b10-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="56b10-112">S_OK</span></span> 
  
> <span data-ttu-id="56b10-113">Das Formular wurde erfolgreich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="56b10-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56b10-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56b10-114">Remarks</span></span>

<span data-ttu-id="56b10-115">Formular Viewer rufen Sie die **IPersistMessage::Save** -Methode, um ein überarbeiteten Formular wieder auf die Nachricht zu speichern, von dem er geladen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="56b10-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="56b10-116">**Speichern Sie** sollte nur aufgerufen werden, wenn das Formular in seinem [normalen](normal-state.md) Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="56b10-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="56b10-117">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="56b10-117">Notes to implementers</span></span>

<span data-ttu-id="56b10-118">Übernehmen Sie die gespeicherten Änderungen nicht; Es liegt an den Anrufer an die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="56b10-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="56b10-119">Nehmen Sie Änderungen an den Eigenschaften, die während des Anrufs **Speichern** auf das Formular Nachricht außer gehören nie vor.</span><span class="sxs-lookup"><span data-stu-id="56b10-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="56b10-120">Wenn _fSameAsLoad_ auf TRUE festgelegt ist, können Sie die Änderungen auf dem Formular vorhandene Nachricht speichern.</span><span class="sxs-lookup"><span data-stu-id="56b10-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="56b10-121">Wenn _fSameAsLoad_ auf FALSE festgelegt ist, müssen Sie alle Eigenschaften aus der ursprünglichen Nachricht in der Meldung von _pMessage_ vor dem Speichern kopieren.</span><span class="sxs-lookup"><span data-stu-id="56b10-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="56b10-122">Verwenden Sie die ursprüngliche Nachricht [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode, um die Eigenschaften zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="56b10-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="56b10-123">Wenn alle Eigenschaften kopiert wurden, geben Sie den Status [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="56b10-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="56b10-124">Wenn keine Fehler auftreten, geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="56b10-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="56b10-125">Anderenfalls zurückgegeben Sie Fehler, der von der fehlgeschlagenen Aktion.</span><span class="sxs-lookup"><span data-stu-id="56b10-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="56b10-126">Wenn **Speichern** aufgerufen wird, wenn das Formular in einem anderen Status als Normal befindet, zurückgeben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="56b10-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="56b10-127">Weitere Informationen zum Speichern von Speicherobjekte finden Sie in der Dokumentation zu den Methoden [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="56b10-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56b10-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56b10-128">See also</span></span>



[<span data-ttu-id="56b10-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="56b10-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="56b10-130">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="56b10-130">Form States</span></span>](form-states.md)

