---
title: Starten eines neuen Formulars zum verFassen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270056"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="2a1a2-103">Starten eines neuen Formulars zum verFassen</span><span class="sxs-lookup"><span data-stu-id="2a1a2-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="2a1a2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a1a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a1a2-105">Formularserver Implementierer sollten die folgende Abfolge von Methoden aufrufen zu ihren Formularserver-und Form-Objekten erwarten, wenn eine Clientanwendung eine neue Nachricht zum Verfassen öffnet:</span><span class="sxs-lookup"><span data-stu-id="2a1a2-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="2a1a2-106">Die Clientanwendung Ruft die [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode auf, um Klasseninformationen zur Nachrichtenklasse des Formular Servers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="2a1a2-107">Die Clientanwendung Ruft [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) auf, um ein neues Form-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="2a1a2-108">Der MAPI-Formular-Manager lädt den Formularserver, falls er sich nicht bereits im Arbeitsspeicher befindet, und ruft eine [IMAPIForm](imapiformiunknown.md) -Schnittstelle vom Formularserver ab.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="2a1a2-109">Die Clientanwendung verwendet die resultierende **IMAPIForm** -Schnittstelle und ruft die [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode auf, um die [IPersistMessage](ipersistmessageiunknown.md) -Schnittstelle des Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="2a1a2-110">Die Clientanwendung Ruft die [IPersistMessage:: InitNew](ipersistmessage-initnew.md) -Methode auf, um das Form-Objekt mit [IMessage](imessageimapiprop.md)-, View Context-und Advise-Objekten zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="2a1a2-111">Die Clientanwendung Ruft die [IMAPIForm::D overb](imapiform-doverb.md) -Methode auf, um das geöffnete Verb aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2a1a2-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a1a2-112">See also</span></span>



[<span data-ttu-id="2a1a2-113">Formular Server interAktionen</span><span class="sxs-lookup"><span data-stu-id="2a1a2-113">Form Server Interactions</span></span>](form-server-interactions.md)

