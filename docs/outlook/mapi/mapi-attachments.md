---
title: MAPI-Anlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417833"
---
# <a name="mapi-attachments"></a><span data-ttu-id="523cd-103">MAPI-Anlagen</span><span class="sxs-lookup"><span data-stu-id="523cd-103">MAPI Attachments</span></span>

  
  
<span data-ttu-id="523cd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="523cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="523cd-105">Einige Anbieter Nachricht erm�glichen Clients Nachrichten Informationen hinzugef�gt, in Form von Dateien, OLE-Objekte, Nachrichten oder Bin�rdaten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="523cd-105">Some message store providers enable clients to associate added information in the form of files, OLE objects, messages, or binary data with messages.</span></span> <span data-ttu-id="523cd-106">Diese zus�tzlichen Informationen wird eine e-Mail-Nachrichtenanhang aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="523cd-106">This added information is called a message's attachment.</span></span> <span data-ttu-id="523cd-107">Da Anlagen erstellt, verwaltet und auf die nur �ber ihre Nachrichten zugegriffen werden, werden sie Nachricht Unterobjekte betrachtet.</span><span class="sxs-lookup"><span data-stu-id="523cd-107">Because attachments are created, maintained, and accessed only through their messages, they are considered message subobjects.</span></span> <span data-ttu-id="523cd-108">Anlagen enthalten einen fortlaufende Zahlen bekannten statt eines Eintrags-ID f�r den Zugriff als Anlage Zahl.</span><span class="sxs-lookup"><span data-stu-id="523cd-108">Rather than having an entry identifier for access, attachments have a sequential number known as an attachment number.</span></span> <span data-ttu-id="523cd-109">Diese Nummer wird die Anlage in der Nachricht, aber nicht notwendigerweise innerhalb der Nachrichtenspeicher eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="523cd-109">This number uniquely identifies the attachment within its message, but not necessarily within the message store.</span></span> <span data-ttu-id="523cd-110">Zwei verschiedene Nachrichten k�nnen verschiedene Anlagen mit derselben Anlage Nummer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="523cd-110">Two different messages can have different attachments with the same attachment number.</span></span> <span data-ttu-id="523cd-111">Anlagennummern sind nur gültig, solange die Nachricht geöffnet ist und in der **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="523cd-111">Attachment numbers are only valid as long as the message is open and are stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="523cd-p102">Zugriff auf zusammenfassende Informationen zu allen eine e-Mail-Anlagen abrufen Clients die Anlagentabelle. Die Anlagentabelle enth�lt Informationen, mit denen Clients eine Anlage direkt, wie die Anzahl der Anlage und aufzeichnen Schl�ssel zuzugreifen. Clients k�nnen eine Anlagentabelle durch Abrufen:</span><span class="sxs-lookup"><span data-stu-id="523cd-p102">To access summary information about all of a message's attachments, clients retrieve its attachment table. The attachment table includes information that clients can use to access an attachment directly, such as its attachment number and record key. Clients can retrieve an attachment table by:</span></span>
  
- <span data-ttu-id="523cd-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="523cd-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
- <span data-ttu-id="523cd-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="523cd-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="523cd-119">Message store providers are expected to support both of these approaches.</span><span class="sxs-lookup"><span data-stu-id="523cd-119">Message store providers are expected to support both of these approaches.</span></span> <span data-ttu-id="523cd-120">Der **OpenProperty** -Ansatz erfordert, dass der Aufrufer IID_IMAPITable als Schnittstellenbezeichner und **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md)) als das Property-Tag angibt.</span><span class="sxs-lookup"><span data-stu-id="523cd-120">The **OpenProperty** approach requires that the caller specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) as the property tag.</span></span> <span data-ttu-id="523cd-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span><span class="sxs-lookup"><span data-stu-id="523cd-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span></span> <span data-ttu-id="523cd-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span><span class="sxs-lookup"><span data-stu-id="523cd-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span></span> <span data-ttu-id="523cd-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span><span class="sxs-lookup"><span data-stu-id="523cd-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span>
  
 <span data-ttu-id="523cd-124">**PR_MESSAGE_ATTACHMENTS** kann verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="523cd-124">**PR_MESSAGE_ATTACHMENTS** can be used:</span></span> 
  
- <span data-ttu-id="523cd-125">Mit **IMAPIProp::OpenProperty** Zugriff auf eine Anlage oder ein Empf�nger-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="523cd-125">With **IMAPIProp::OpenProperty** to access an attachment or recipient table.</span></span> 
    
- <span data-ttu-id="523cd-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span><span class="sxs-lookup"><span data-stu-id="523cd-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="523cd-128">In einer Einschr�nkung Unterobjekt um anzugeben, dass die untergeordneten Einschr�nkung auf Anlagen angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="523cd-128">In a subobject restriction to indicate that the child restriction should apply to attachments.</span></span>
    
<span data-ttu-id="523cd-129">For more information, see [Anlagentabellen](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="523cd-129">For more information, see [Attachment Tables](attachment-tables.md).</span></span>
  

