---
title: Starten ein neues Formular zum Verfassen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8d1b94c70e4de6310d2e84cf002c4e3199fced2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792908"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="2d91b-103">Starten ein neues Formular zum Verfassen</span><span class="sxs-lookup"><span data-stu-id="2d91b-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="2d91b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d91b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d91b-105">Formular Server Implementierer erwarten, dass die folgende Sequenz von Methode von Anrufen an ihre Server Formular und Formularobjekte, wenn eine Clientanwendung öffnet eine neue Nachricht zum Verfassen:</span><span class="sxs-lookup"><span data-stu-id="2d91b-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="2d91b-106">Die Clientanwendung ruft die [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode, um die Klasseninformationen zu dem Formular Server Nachrichtenklasse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d91b-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="2d91b-107">Die Clientanwendung ruft [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) zum Abrufen eines neuen Formulars-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2d91b-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="2d91b-108">MAPI-Formular-Manager lädt der Formular-Server, wenn es nicht bereits im Arbeitsspeicher, und eine [IMAPIForm](imapiformiunknown.md) Schnittstelle aus dem Formular Server ruft.</span><span class="sxs-lookup"><span data-stu-id="2d91b-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="2d91b-109">Die Client-Anwendung die resultierende **IMAPIForm** -Schnittstelle und ruft die [QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode, um das Objekt [IPersistMessage](ipersistmessageiunknown.md) Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="2d91b-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="2d91b-110">Die Clientanwendung ruft die [IPersistMessage::InitNew](ipersistmessage-initnew.md) -Methode, um das Formularobjekt [IMessage](imessageimapiprop.md), Ansichtskontext, zuordnen und beraten der Empfängerobjekten.</span><span class="sxs-lookup"><span data-stu-id="2d91b-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="2d91b-111">Die Clientanwendung ruft die [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode, um das Öffnen Verb aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d91b-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2d91b-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d91b-112">See also</span></span>



[<span data-ttu-id="2d91b-113">Formular Server Interaktionen</span><span class="sxs-lookup"><span data-stu-id="2d91b-113">Form Server Interactions</span></span>](form-server-interactions.md)

