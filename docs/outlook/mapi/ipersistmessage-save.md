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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309618"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="48aa3-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="48aa3-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="48aa3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48aa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48aa3-105">Speichert ein überarbeitete Formular zurück in der Nachricht, von der es geladen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="48aa3-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="48aa3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48aa3-106">Parameters</span></span>

 <span data-ttu-id="48aa3-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="48aa3-107">_pMessage_</span></span>
  
> <span data-ttu-id="48aa3-108">in Ein Zeiger auf die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="48aa3-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="48aa3-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="48aa3-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="48aa3-110">in TRUE, um anzugeben, dass die Nachricht, auf die von _pMessage_ verwiesen wird, die Nachricht ist, von der das Formular geladen oder erstellt wurde; andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="48aa3-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48aa3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48aa3-111">Return value</span></span>

<span data-ttu-id="48aa3-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="48aa3-112">S_OK</span></span> 
  
> <span data-ttu-id="48aa3-113">Das Formular wurde erfolgreich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="48aa3-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48aa3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48aa3-114">Remarks</span></span>

<span data-ttu-id="48aa3-115">Formular Betrachter rufen die **IPersistMessage:: Save** -Methode auf, um ein überarbeitete Formular zurück in die Nachricht zu speichern, aus der es geladen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="48aa3-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="48aa3-116">**Save** sollte nur aufgerufen werden, wenn sich das Formular im [Normal](normal-state.md) Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="48aa3-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="48aa3-117">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="48aa3-117">Notes to implementers</span></span>

<span data-ttu-id="48aa3-118">Speichern Sie die gespeicherten Änderungen nicht. der Aufrufer muss die Änderungen übernehmen.</span><span class="sxs-lookup"><span data-stu-id="48aa3-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="48aa3-119">Nehmen Sie keine Änderungen an den Eigenschaften vor, die zur Nachricht des Formulars gehören, außer während des **Save** -Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="48aa3-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="48aa3-120">Wenn _fSameAsLoad_ auf true festgelegt ist, können Sie die Änderungen an der vorhandenen Nachricht des Formulars speichern.</span><span class="sxs-lookup"><span data-stu-id="48aa3-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="48aa3-121">Wenn _fSameAsLoad_ auf false festgelegt ist, müssen Sie alle Eigenschaften aus der ursprünglichen Nachricht in die Nachricht kopieren, die von _pMessage_ vor dem Speichern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48aa3-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="48aa3-122">Verwenden Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode der ursprünglichen Nachricht, um die Eigenschaften zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="48aa3-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="48aa3-123">Wenn alle Eigenschaften kopiert wurden, geben Sie den Status [noscribble](noscribble-state.md) ein.</span><span class="sxs-lookup"><span data-stu-id="48aa3-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="48aa3-124">Wenn keine Fehler auftreten, geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="48aa3-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="48aa3-125">Geben Sie andernfalls den Fehler aus der fehlgeschlagenen Aktion zurück.</span><span class="sxs-lookup"><span data-stu-id="48aa3-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="48aa3-126">Wenn **Save** aufgerufen wird, wenn sich das Formular in einem anderen Status als normal befindet, geben Sie E_UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="48aa3-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="48aa3-127">Weitere Informationen zum Speichern von Speicherobjekten finden Sie in der Dokumentation zu den [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="48aa3-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48aa3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48aa3-128">See also</span></span>



[<span data-ttu-id="48aa3-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48aa3-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="48aa3-130">Formular Status</span><span class="sxs-lookup"><span data-stu-id="48aa3-130">Form States</span></span>](form-states.md)

