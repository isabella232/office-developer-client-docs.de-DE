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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417671"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="77fb7-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="77fb7-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="77fb7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77fb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77fb7-105">Erstellt eine neue Anlage.</span><span class="sxs-lookup"><span data-stu-id="77fb7-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="77fb7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77fb7-106">Parameters</span></span>

 <span data-ttu-id="77fb7-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="77fb7-107">_lpInterface_</span></span>
  
> <span data-ttu-id="77fb7-108">in Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf die Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77fb7-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="77fb7-109">Übergeben von NULL-Ergebnissen in der Standardschnittstelle der Nachricht oder **IMessage**, wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77fb7-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="77fb7-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="77fb7-110">_ulFlags_</span></span>
  
> <span data-ttu-id="77fb7-111">in Bitmaske von Flags, die die Erstellung der Anlage steuert.</span><span class="sxs-lookup"><span data-stu-id="77fb7-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="77fb7-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="77fb7-112">The following flag can be set:</span></span>
    
<span data-ttu-id="77fb7-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="77fb7-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="77fb7-114">Ermöglicht \*\*\*\* , dass createattach erfolgreich zurückgegeben wird, möglicherweise, bevor der aufrufende Client vollständig auf die Anlage zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="77fb7-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="77fb7-115">Wenn auf die Anlage nicht zugegriffen werden kann, führt der nachfolgende Aufruf zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="77fb7-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="77fb7-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="77fb7-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="77fb7-117">Out Zeiger auf eine Indexnummer, die die neu erstellte Anlage identifiziert.</span><span class="sxs-lookup"><span data-stu-id="77fb7-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="77fb7-118">Diese Nummer ist nur gültig, wenn die Nachricht geöffnet ist und die Grundlage für die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage ist.</span><span class="sxs-lookup"><span data-stu-id="77fb7-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="77fb7-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="77fb7-119">_lppAttach_</span></span>
  
> <span data-ttu-id="77fb7-120">Out Zeiger auf einen Zeiger auf das offene Attachment-Objekt.</span><span class="sxs-lookup"><span data-stu-id="77fb7-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77fb7-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77fb7-121">Return value</span></span>

<span data-ttu-id="77fb7-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="77fb7-122">S_OK</span></span> 
  
> <span data-ttu-id="77fb7-123">Die Anlage wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="77fb7-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77fb7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77fb7-124">Remarks</span></span>

<span data-ttu-id="77fb7-125">Die **IMessage:: createattach** -Methode erstellt eine neue Anlage für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="77fb7-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="77fb7-126">Die neue Anlage und alle für Sie festgelegten Eigenschaften sind erst verfügbar, wenn ein Client sowohl die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode als auch die **IMAPIProp:: SaveChanges** -Methode der Nachricht aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="77fb7-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="77fb7-127">Die Anlagennummer, auf die durch _lpulAttachmentNum_ verwiesen wird, ist eindeutig und gilt nur innerhalb des Kontexts der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="77fb7-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="77fb7-128">Das heißt, zwei Anlagen in zwei verschiedenen Nachrichten können dieselbe Anzahl haben, während zwei Anlagen in der gleichen Nachricht nicht.</span><span class="sxs-lookup"><span data-stu-id="77fb7-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77fb7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77fb7-129">See also</span></span>



[<span data-ttu-id="77fb7-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="77fb7-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

