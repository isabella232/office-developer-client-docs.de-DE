---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6351be353100649e38a14543a44df5e115c9408b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792521"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="1a28f-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="1a28f-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="1a28f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a28f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a28f-105">Erstellt eine neue Anlage.</span><span class="sxs-lookup"><span data-stu-id="1a28f-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="1a28f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a28f-106">Parameters</span></span>

 <span data-ttu-id="1a28f-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1a28f-107">_lpInterface_</span></span>
  
> <span data-ttu-id="1a28f-108">[in] Zeiger auf die Schnittstelle-ID (IID), das die Schnittstelle für verwendet werden, um Zugriff auf die Nachricht darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a28f-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="1a28f-109">Bei Übergabe von NULL führt der Nachricht Standardschnittstelle oder **IMessage**, zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1a28f-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="1a28f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a28f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1a28f-111">[in] Bitmaske aus Flags, die steuert, wie das Attachment-Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1a28f-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="1a28f-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1a28f-112">The following flag can be set:</span></span>
    
<span data-ttu-id="1a28f-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1a28f-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1a28f-114">Ermöglicht **CreateAttach** erfolgreich, möglicherweise beendet, bevor die Anlage vollständig an den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1a28f-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="1a28f-115">Wenn die Anlage nicht möglich ist, kann nachfolgende aufrufen es ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="1a28f-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="1a28f-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="1a28f-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="1a28f-117">[out] Zeiger auf eine Indexnummer, die das neu erstellte Attachment-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1a28f-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="1a28f-118">Diese Nummer gilt nur, wenn die Nachricht geöffnet wird und die Grundlage für die Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft bildet.</span><span class="sxs-lookup"><span data-stu-id="1a28f-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="1a28f-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="1a28f-119">_lppAttach_</span></span>
  
> <span data-ttu-id="1a28f-120">[out] Zeiger auf einen Zeiger auf das Objekt Anlage öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a28f-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a28f-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1a28f-121">Return value</span></span>

<span data-ttu-id="1a28f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a28f-122">S_OK</span></span> 
  
> <span data-ttu-id="1a28f-123">Die Anlage wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="1a28f-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a28f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a28f-124">Remarks</span></span>

<span data-ttu-id="1a28f-125">Die **IMessage::CreateAttach** -Methode erstellt eine neue Anlage in einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1a28f-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="1a28f-126">Die neue Anlage und Eigenschaften, die für sie festgelegt sind sind nicht verfügbar, bis ein Client die Anlage [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode und die Nachricht **IMAPIProp::SaveChanges** -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="1a28f-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="1a28f-127">Die Anlage Anzahl auf den _LpulAttachmentNum_ ist eindeutig und nur im Kontext der Nachricht gültig.</span><span class="sxs-lookup"><span data-stu-id="1a28f-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="1a28f-128">D. h., können zwei Anlagen in zwei verschiedene Nachrichten die gleiche Anzahl haben, während zwei Anlagen in die gleiche Nachricht ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="1a28f-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a28f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a28f-129">See also</span></span>



[<span data-ttu-id="1a28f-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1a28f-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

