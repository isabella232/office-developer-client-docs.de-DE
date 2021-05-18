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
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405156"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="9f6ca-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="9f6ca-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="9f6ca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f6ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f6ca-105">Kopiert oder verschiebt Nachrichten aus einem Ordner in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-105">Copies or moves messages from one folder to another folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="9f6ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f6ca-106">Parameters</span></span>

 <span data-ttu-id="9f6ca-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="9f6ca-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="9f6ca-108">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Ordner verwendet werden soll, der die zu kopierende oder zu verschiebende Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="9f6ca-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="9f6ca-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="9f6ca-110">[in] Ein Zeiger auf den Ordner, der die zu kopierende oder zu verschiebende Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="9f6ca-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="9f6ca-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="9f6ca-112">[in] Ein Zeiger auf ein Array von Eintragsbezeichnern, die die zu kopierenden oder verschobenen Nachrichten identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="9f6ca-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="9f6ca-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="9f6ca-114">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Zielordner für die kopierten oder verschobenen Nachrichten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="9f6ca-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="9f6ca-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="9f6ca-116">[in] Ein Zeiger auf den Zielordner für die kopierten oder verschobenen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="9f6ca-117">Dieser Ordner muss geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-117">This folder must be open.</span></span>
    
 <span data-ttu-id="9f6ca-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9f6ca-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="9f6ca-119">[in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9f6ca-120">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="9f6ca-121">Der _lpProgress-Parameter_ wird ignoriert, es sei denn, MESSAGE_DIALOG in _ulFlags festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="9f6ca-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9f6ca-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9f6ca-122">_lpProgress_</span></span>
  
> <span data-ttu-id="9f6ca-123">[in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9f6ca-124">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="9f6ca-125">Der _lpProgress-Parameter_ wird ignoriert, es sei denn, MESSAGE_DIALOG in _ulFlags festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="9f6ca-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9f6ca-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f6ca-126">_ulFlags_</span></span>
  
> <span data-ttu-id="9f6ca-127">[in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebevorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="9f6ca-128">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9f6ca-128">The following flags can be set:</span></span>
    
<span data-ttu-id="9f6ca-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9f6ca-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="9f6ca-130">Fordert die Anzeige eines Statusindikators an.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="9f6ca-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="9f6ca-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="9f6ca-132">Die Nachrichten sollten verschoben und nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="9f6ca-133">Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f6ca-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f6ca-134">Return value</span></span>

<span data-ttu-id="9f6ca-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f6ca-135">S_OK</span></span> 
  
> <span data-ttu-id="9f6ca-136">Der Kopier- oder Verschiebevorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="9f6ca-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9f6ca-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="9f6ca-138">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9f6ca-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f6ca-139">Remarks</span></span>

<span data-ttu-id="9f6ca-140">Die **IMAPISupport::CopyMessages-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9f6ca-141">Nachrichtenspeicheranbieter können **IMAPISupport::CopyMessages** in ihrer Implementierung von [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) aufrufen, um eine oder mehrere Nachrichten aus einem Ordner in einen anderen zu kopieren oder zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="9f6ca-142">Im Rahmen des **IMAPISupport::CopyMessages-Aufrufs** kann der Nachrichtenspeicheranbieter angeben, dass MAPI einen Statusindikator anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="9f6ca-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f6ca-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f6ca-143">See also</span></span>



[<span data-ttu-id="9f6ca-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="9f6ca-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="9f6ca-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f6ca-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

