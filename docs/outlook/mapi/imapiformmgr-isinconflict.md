---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412884"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="46b17-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="46b17-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="46b17-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46b17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46b17-105">Bestimmt, ob ein Formular eigene Nachrichten Konflikte verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="46b17-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="46b17-106">Eine Nachricht ist in Konflikt, wenn Sie von mehreren Benutzern gleichzeitig bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="46b17-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="46b17-107">Dies kann mit Nachrichten in öffentlichen Ordnern geschehen.</span><span class="sxs-lookup"><span data-stu-id="46b17-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="46b17-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="46b17-108">Parameters</span></span>

 <span data-ttu-id="46b17-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="46b17-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="46b17-110">in Ein Zeiger auf eine Bitmaske von Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer Nachricht kopiert werden, die den aktuellen Status der Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="46b17-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="46b17-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="46b17-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="46b17-112">in Eine Bitmaske von Client definierten oder Anbieter definierten Flags, die aus der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft einer Nachricht kopiert werden, die zusätzliche Informationen zum Status der Nachricht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="46b17-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="46b17-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="46b17-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="46b17-114">in Eine Zeichenfolge, die die Nachrichtenklasse der Nachricht benennt.</span><span class="sxs-lookup"><span data-stu-id="46b17-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="46b17-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="46b17-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="46b17-116">in Ein Zeiger auf den Ordner, der die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="46b17-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="46b17-117">Der _pFolderFocus_ -Parameter kann NULL sein, wenn ein solcher Ordner nicht vorhanden ist (beispielsweise, wenn die Nachricht in eine andere Nachricht eingebettet ist).</span><span class="sxs-lookup"><span data-stu-id="46b17-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="46b17-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46b17-118">Return value</span></span>

<span data-ttu-id="46b17-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="46b17-119">S_OK</span></span> 
  
> <span data-ttu-id="46b17-120">Das Formular verarbeitet keine eigenen Nachrichten Konflikte.</span><span class="sxs-lookup"><span data-stu-id="46b17-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="46b17-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="46b17-121">S_FALSE</span></span> 
  
> <span data-ttu-id="46b17-122">Das Formular verarbeitet eigene Nachrichten Konflikte, oder die Nachricht, für die Informationen übergeben wurden, ist nicht in Konflikt.</span><span class="sxs-lookup"><span data-stu-id="46b17-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46b17-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46b17-123">Remarks</span></span>

<span data-ttu-id="46b17-124">Formular Betrachter rufen die **IMAPIFormMgr:: IsInConflict** -Methode auf, um zu ermitteln, ob ein bestimmtes Formular eigene Nachrichten Konflikte nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="46b17-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="46b17-125">**IsInConflict** überprüft die Bitmasken in den Parametern _ulMessageFlags_ und _ulMessageStatus_ auf das vorhanden sein eines Konflikt Kennzeichens.</span><span class="sxs-lookup"><span data-stu-id="46b17-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="46b17-126">Wenn ein Konflikt-Flag festgelegt ist, löst **IsInConflict** die Nachrichtenklasse, die im Parameter _szMessageClass_ übergeben wird, und gibt S_OK zurück, wenn das Formular Ihre eigenen Konflikte nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="46b17-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="46b17-127">**IsInConflict** gibt S_FALSE zurück, wenn das Formular eigene Konflikte behandelt.</span><span class="sxs-lookup"><span data-stu-id="46b17-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="46b17-128">Ein Formular, das seine eigenen Konflikte nicht behandelt, muss mithilfe der [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) -Methode geöffnet werden und kann kein vorhandenes Form-Objekt wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="46b17-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="46b17-129">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="46b17-129">Notes to callers</span></span>

<span data-ttu-id="46b17-130">Client Anwendungen müssen in der Regelkonflikte bewältigen, wenn die Anwendungen von einer Nachricht zur nächsten oder zur vorherigen Nachricht in einem Ordner wechseln.</span><span class="sxs-lookup"><span data-stu-id="46b17-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="46b17-131">Wenn eine Nachricht in Konflikt steht, aber der Formularserver für diese Nachricht Konflikte verarbeiten kann, sollte die Clientanwendung den üblichen Code zum Anzeigen der nächsten oder vorherigen Nachricht ausführen.</span><span class="sxs-lookup"><span data-stu-id="46b17-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="46b17-132">Wenn der Formularserver Konflikte nicht verarbeiten kann, sollte die Clientanwendung fortgesetzt werden, als ob Sie die Nachrichtenklasse der nächsten oder vorherigen Nachricht nicht kennen würde.</span><span class="sxs-lookup"><span data-stu-id="46b17-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46b17-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46b17-133">See also</span></span>



[<span data-ttu-id="46b17-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="46b17-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="46b17-135">Kanonische PidTagMessageFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="46b17-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="46b17-136">Kanonische Pidtagmessagestatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="46b17-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="46b17-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46b17-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

