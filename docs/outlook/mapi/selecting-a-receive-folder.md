---
title: Auswählen eines Empfangs Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428417"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="e4a0d-103">Auswählen eines Empfangs Ordners</span><span class="sxs-lookup"><span data-stu-id="e4a0d-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="e4a0d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4a0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4a0d-105">Ein Empfangsordner ist der Speicherort eingehender Nachrichten einer bestimmten Klasse.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="e4a0d-106">Bei IPM-und verwandten Berichtnachrichten weist MAPI den Posteingang als standardmäßigen Empfangsordner zu.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="e4a0d-107">Für IPC und zugehörige Berichtnachrichten weist MAPI den Stammordner des Nachrichtenspeichers als standardmäßigen Empfangsordner zu.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="e4a0d-108">Sie können diese Zuordnungen ändern oder zusätzliche Zuordnungen für andere Nachrichtenklassen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="e4a0d-109">Die explizite Zuweisung von Empfangs Ordnern für die unterstützten Nachrichtenklassen des Clients ist optional.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="e4a0d-110">Wenn für eine Klasse für eingehende Nachrichten kein Empfangsordner zugewiesen ist, verwendet der Nachrichtenspeicher Anbieter automatisch den Ordner Receive für die Klasse, die mit dem längsten möglichen Präfix der eingehenden Klasse übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="e4a0d-111">Wenn Ihr Client beispielsweise eine Nachricht der Klasse IPM erhält. Hinweis. myDocument und der einzige empfangene Ordner, der eingerichtet wurde, ist der Posteingang für IPM-Nachrichten, diese Nachricht wird im Posteingang abgelegt, da IPM. Hinweis. myDocument wird von der Basisklasse IPM abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="e4a0d-112">Wenn Sie einen Empfangsordner für IPC-Nachrichten zuweisen, verwenden Sie niemals einen Ordner aus der IPM-Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="e4a0d-113">Diese Ordner sollten nur für IPM-Nachrichten reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="e4a0d-114">Verwenden Sie stattdessen einen Ordner, der im Stammordner des Nachrichtenspeichers enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="e4a0d-115">**So erstellen Sie einen Empfangsordner für eine IPM-Nachrichtenklasse**</span><span class="sxs-lookup"><span data-stu-id="e4a0d-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="e4a0d-116">Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers auf, um die **PR_IPM_SUBTREE_ENTRYID** ([pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="e4a0d-117">Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) mit **PR_IPM_SUBTREE_ENTRYID** als Eintragsbezeichner auf, um den Stammordner der IPM-Unterstruktur im Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="e4a0d-118">Rufen Sie [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) auf, um den Empfangsordner zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="e4a0d-119">Rufen Sie [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) auf, um den neuen Ordner der IPM-Nachrichtenklasse zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="e4a0d-120">**So erstellen Sie einen Empfangsordner für eine IPC-Nachrichtenklasse**</span><span class="sxs-lookup"><span data-stu-id="e4a0d-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="e4a0d-121">Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) mit einer NULL-Eintrags-ID auf, um den Stammordner des Nachrichtenspeichers zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="e4a0d-122">Rufen Sie [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) auf, um den Empfangsordner zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="e4a0d-123">Rufen Sie [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) auf, um den neuen Ordner der IPC-Nachrichtenklasse zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="e4a0d-124">Weisen Sie den empfangenen Ordner, den Sie für Nachrichten verwenden, für Verwandte Berichtnachrichten zu.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="e4a0d-125">Wenn Ihr Client beispielsweise IPM. Hinweis Nachrichten, Einrichten eines Empfangs Ordners für zukünftige IPM. Hinweis Nachrichten und derselbe Empfänger Ordner für zukünftige Berichte. IPM. Note-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e4a0d-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

