---
title: Verf�gbarmachen von Ordnern in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 457620dd0f805e78d12fc8feba09f8fc8aedc554
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341349"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="cd29a-103">Verfügbarmachen von Ordnern in Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="cd29a-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="cd29a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd29a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd29a-p101">Jeder Nachrichtenspeicheranbieter muss für Clientanwendungen eine [IMAPIFolder](imapifolderimapicontainer.md)-Schnittstelle auf oberster Ebene präsentieren. Der Ordner auf oberster Ebene entspricht dem gesamten Nachrichtenspeicher; er bietet Zugriff auf die Ordner, die Benutzer als die Inhalte des Nachrichtenspeichers sehen. Außerdem wird der Ordner auf oberster Ebene häufig als Standardempfangsordner für IPC-Nachrichten und als der Ordner verwendet, von dem aus Leseberichte gesendet werden. Nachrichtenspeicheranbieter müssen für Clientanwendungen auch eine IPM-Unterstruktur präsentieren, eine Reihe von Ordnern, in denen IPM-Nachrichten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cd29a-p101">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications. The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store. In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent. Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="cd29a-p102">Client-Anwendungen k�nnen durch Aufrufen der [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode mit 0 und NULL f�r die Parameter  _cbEntryId_ und  _lpEntryId_ jeweils Ordner den obersten Ebene �ffnen. In den meisten F�llen �ffnen Clientanwendungen jedoch den Satz von Ordnern, die IPM Nachrichten enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd29a-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="cd29a-111">Wenn Sie eine Liste der Ordner in den Nachrichtenspeicher IPM Ordnerstruktur erhalten m�chten, verwenden Sie die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="cd29a-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="cd29a-112">Rufen Sie die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)-Methode mithilfe der MAPI-Sitzung auf.</span><span class="sxs-lookup"><span data-stu-id="cd29a-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="cd29a-113">Verwenden Sie den resultierenden Nachrichtendatenbankzeiger zum Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md)-Methode für die **PR_IPM_SUBTREE_ENTRYID** ( [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cd29a-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="cd29a-114">Rufen Sie die [IMsgStore::OpenEntry](imsgstore-openentry.md)-Methode mit der Eintrags-ID auf, um einen **IMAPIFolder**-Verweis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd29a-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="cd29a-115">Rufen Sie die [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Abrufen einer Tabelle der Inhalt des Ordners.</span><span class="sxs-lookup"><span data-stu-id="cd29a-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="cd29a-116">Rufen Sie [die QueryRows, um eine Liste der Ordner im Ordner obersten Ebene](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="cd29a-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="cd29a-p103">MAPI-Clients verwenden diese Ordner, um auf andere Ordnerobjekte und Nachrichtenobjekte im Nachrichtenspeicher zuzugreifen. **IMAPIFolder** und die übergeordnete Schnitstelle [IMAPIContainer](imapicontainerimapiprop.md) enthalten die Methoden, die Ihr Nachrichtenspeicheranbieter implementieren muss, um Ordner mit Nachrichtenobjekten aufzufüllen und auf Clientanfragen im Zusammenhang mit Nachrichten zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="cd29a-p103">MAPI clients use these folders to access other folder objects and message objects in the message store. **IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd29a-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd29a-119">See also</span></span>



[<span data-ttu-id="cd29a-120">Implementieren von Ordnern in Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="cd29a-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

