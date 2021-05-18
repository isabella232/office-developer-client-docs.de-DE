---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409090"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="32b42-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="32b42-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="32b42-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32b42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32b42-105">Verwaltet und bietet Zugriff auf die Eigenschaften von Anlagen in Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="32b42-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="32b42-106">Die **IAttach-Schnittstelle** verfügt über keine eigenen eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="32b42-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="32b42-107">Weitere Informationen zur Verwendung von Anlagen finden Sie unter [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="32b42-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32b42-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="32b42-108">Header file:</span></span>  <br/> |<span data-ttu-id="32b42-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32b42-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="32b42-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="32b42-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="32b42-111">Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="32b42-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="32b42-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="32b42-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="32b42-113">Anbieter von Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="32b42-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="32b42-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="32b42-114">Called by:</span></span>  <br/> |<span data-ttu-id="32b42-115">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="32b42-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="32b42-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="32b42-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="32b42-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="32b42-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="32b42-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="32b42-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="32b42-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="32b42-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="32b42-120">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="32b42-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="32b42-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="32b42-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="32b42-122">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="32b42-122">Vtable order</span></span>

<span data-ttu-id="32b42-123">Diese Schnittstelle verfügt nicht über eindeutige Methoden.</span><span class="sxs-lookup"><span data-stu-id="32b42-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="32b42-124">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="32b42-124">**Required properties**</span></span>|<span data-ttu-id="32b42-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="32b42-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32b42-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="32b42-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="32b42-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32b42-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="32b42-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="32b42-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="32b42-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="32b42-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="32b42-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="32b42-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="32b42-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="32b42-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32b42-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32b42-132">See also</span></span>



[<span data-ttu-id="32b42-133">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="32b42-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

