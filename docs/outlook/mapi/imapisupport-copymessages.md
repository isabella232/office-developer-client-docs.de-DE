---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591037"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="031d3-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="031d3-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="031d3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="031d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="031d3-105">Kopiert oder verschiebt Nachrichten aus einem Ordner in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="031d3-105">Copies or moves messages from one folder to another folder.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="031d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="031d3-106">Parameters</span></span>

 <span data-ttu-id="031d3-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="031d3-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="031d3-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle dar, verwendet werden soll, auf den Ordner zugreifen, der enthält die Nachrichten, kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="031d3-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="031d3-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="031d3-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="031d3-110">[in] Ein Zeiger auf den Ordner mit der Nachrichten an kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="031d3-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="031d3-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="031d3-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="031d3-112">[in] Ein Zeiger auf ein Array von Eintragsbezeichner, mit denen die Nachrichten, kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="031d3-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="031d3-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="031d3-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="031d3-114">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugriff auf den Zielordner für die kopierte oder verschobenen Nachrichten zu verwendende darstellt.</span><span class="sxs-lookup"><span data-stu-id="031d3-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="031d3-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="031d3-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="031d3-116">[in] Ein Zeiger auf den Zielordner für die Nachrichten kopierten oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="031d3-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="031d3-117">In diesem Ordner muss geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="031d3-117">This folder must be open.</span></span>
    
 <span data-ttu-id="031d3-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="031d3-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="031d3-119">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="031d3-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="031d3-120">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="031d3-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="031d3-121">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="031d3-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="031d3-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="031d3-122">_lpProgress_</span></span>
  
> <span data-ttu-id="031d3-123">[in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="031d3-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="031d3-124">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="031d3-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="031d3-125">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="031d3-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="031d3-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="031d3-126">_ulFlags_</span></span>
  
> <span data-ttu-id="031d3-127">[in] Eine Bitmaske aus Flags, die steuert, wie der kopieren oder verschieben-Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="031d3-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="031d3-128">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="031d3-128">The following flags can be set:</span></span>
    
<span data-ttu-id="031d3-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="031d3-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="031d3-130">Fordert die Anzeige einer Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="031d3-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="031d3-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="031d3-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="031d3-132">Die Nachrichten verschoben werden soll, sondern kopiert.</span><span class="sxs-lookup"><span data-stu-id="031d3-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="031d3-133">Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.</span><span class="sxs-lookup"><span data-stu-id="031d3-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="031d3-134">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="031d3-134">Return value</span></span>

<span data-ttu-id="031d3-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="031d3-135">S_OK</span></span> 
  
> <span data-ttu-id="031d3-136">Kopieren oder verschieben-Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="031d3-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="031d3-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="031d3-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="031d3-138">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="031d3-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="031d3-139">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="031d3-139">Remarks</span></span>

<span data-ttu-id="031d3-140">Die **IMAPISupport::CopyMessages** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="031d3-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="031d3-141">Nachricht-Anbieter können in ihrer Durchführung des [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) zu kopieren oder verschieben eine oder mehrere Nachrichten aus einem Ordner in einen anderen **IMAPISupport::CopyMessages** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="031d3-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="031d3-142">Teil des Aufrufs **IMAPISupport::CopyMessages** kann der Nachricht Speicheranbieter angeben, dass MAPI eine Statusanzeige angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="031d3-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="031d3-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="031d3-143">See also</span></span>



[<span data-ttu-id="031d3-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="031d3-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="031d3-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="031d3-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

