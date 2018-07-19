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
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792173"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="b7a1a-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="b7a1a-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="b7a1a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7a1a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7a1a-105">Bestimmt, ob ein Formular eine eigene Nachricht Konflikte verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="b7a1a-106">Eine Nachricht ist in Konflikt, wenn es von mehreren Benutzern gleichzeitig bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="b7a1a-107">Dies kann vorkommen, auf Nachrichten in öffentlichen Ordnern.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="b7a1a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7a1a-108">Parameters</span></span>

 <span data-ttu-id="b7a1a-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="b7a1a-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="b7a1a-110">[in] Ein Zeiger auf eine Bitmaske aus Flags, die von der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer Nachricht, der angibt, den aktuellen Status der Nachricht kopiert.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="b7a1a-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="b7a1a-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="b7a1a-112">[in] Eine Bitmaske vom Client definiert oder vom Anbieter definiertes Flags, kopiert aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft einer Nachricht bereitstellt, die zusätzliche Informationen zum Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="b7a1a-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="b7a1a-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="b7a1a-114">[in] Eine Zeichenfolge, die die Nachricht Nachrichtenklasse bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="b7a1a-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="b7a1a-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="b7a1a-116">[in] Ein Zeiger auf den Ordner, der die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="b7a1a-117">Der Parameter _pFolderFocus_ kann NULL sein, wenn eine solche ein Ordner nicht vorhanden ist (z. B., wenn die Nachricht in eine andere Nachricht eingebettet ist).</span><span class="sxs-lookup"><span data-stu-id="b7a1a-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b7a1a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7a1a-118">Return value</span></span>

<span data-ttu-id="b7a1a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7a1a-119">S_OK</span></span> 
  
> <span data-ttu-id="b7a1a-120">Das Formular behandelt eine eigene Nachricht Konflikte nicht.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="b7a1a-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b7a1a-121">S_FALSE</span></span> 
  
> <span data-ttu-id="b7a1a-122">Das Formular eine eigene Nachricht Konflikte behandelt werden, oder die Nachricht, deren Informationen übergeben wurde, ist nicht in Konflikt.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7a1a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7a1a-123">Remarks</span></span>

<span data-ttu-id="b7a1a-124">Formular Viewer rufen Sie die **IMAPIFormMgr::IsInConflict** -Methode, um zu ermitteln, ob ein bestimmtes Formular eine eigene Nachricht Konflikte nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="b7a1a-125">**IsInConflict** überprüft die Bitmasken in den _UlMessageFlags_ und _UlMessageStatus_ das Vorhandensein von ein Conflict-Flag.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="b7a1a-126">Wenn ein Konflikt Flag festgelegt ist, **IsInConflict** die Nachrichtenklasse in der _SzMessageClass_ -Parameter übergeben wird, aufgelöst wird und gibt S_OK zurück, wenn das Formular eine eigene Konflikte nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="b7a1a-127">**IsInConflict** gibt S_FALSE zurück, wenn das Formular eine eigene Konflikte behandelt.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="b7a1a-128">Ein Formular, das nicht über einen eigenen Konflikte handhabt muss mithilfe der [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) -Methode geöffnet und kann nicht wiederverwenden ein vorhandenen Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b7a1a-129">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b7a1a-129">Notes to callers</span></span>

<span data-ttu-id="b7a1a-130">Clientanwendungen weisen in der Regel für den Umgang mit Konflikte, wenn die Anwendung von einer Nachricht in der nächsten oder der vorherigen Nachricht in einem Ordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="b7a1a-131">Wenn eine Nachricht liegt ein Konflikt, aber der Server Formular für diese Nachricht Konflikte behandeln kann, sollte die Clientanwendung seine üblichen Code für die Anzeige der nächsten oder der vorherigen Nachricht ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="b7a1a-132">Wenn der Formular Server Konflikte nicht verarbeiten kann, sollte die Clientanwendung fortgesetzt, als wäre es der Nachrichtenklasse der nächsten oder der vorherigen Nachricht nicht bekannt war.</span><span class="sxs-lookup"><span data-stu-id="b7a1a-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7a1a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7a1a-133">See also</span></span>



[<span data-ttu-id="b7a1a-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="b7a1a-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="b7a1a-135">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b7a1a-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="b7a1a-136">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b7a1a-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="b7a1a-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7a1a-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

