---
title: Auswählen einer Empfangsordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 87f8b4f4011e405d9848f12b5cae56f27fff1ab8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795468"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="af672-103">Auswählen einer Empfangsordner</span><span class="sxs-lookup"><span data-stu-id="af672-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="af672-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af672-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af672-105">Eine Empfangsordner ist in der eingehende Nachrichten von einer bestimmten Klasse platziert werden.</span><span class="sxs-lookup"><span data-stu-id="af672-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="af672-106">IPM und verwandte Berichtnachrichten weist MAPI Standard Empfangsordner im Posteingang.</span><span class="sxs-lookup"><span data-stu-id="af672-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="af672-107">IPK und verwandte Berichtnachrichten weist MAPI Standard Empfangsordner im Stammordner des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="af672-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="af672-108">Sie können diese Zuordnungen ändern oder zusätzliche Aufgaben für andere Nachrichtenklassen machen.</span><span class="sxs-lookup"><span data-stu-id="af672-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="af672-109">Explizites Ordner Aufgaben empfangen, für der Client des unterstützten Nachricht Klassen ist optional.</span><span class="sxs-lookup"><span data-stu-id="af672-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="af672-110">Wenn eine eingehende Nachrichtenklasse nicht mit einer zugewiesenen Empfangsordner verfügt, verwendet der Speicheranbieter Nachricht automatisch den Empfangsordner für die Klasse, die das längsten mögliche Präfix der eingehenden-Klasse entspricht.</span><span class="sxs-lookup"><span data-stu-id="af672-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="af672-111">Wenn beispielsweise der Client eine Nachricht der Klasse IPM empfängt. Note.MyDocument und die einzige erhalten Ordner, die hergestellt wurde ist der Posteingang für IPM-Nachrichten, diese Meldung wird im Posteingang platziert werden, da IPM. Note.MyDocument wird von der Basisklasse IPM abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="af672-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="af672-112">Wenn Sie eine Empfangsordner für IPK Nachrichten zuordnen möchten, verwenden Sie einen Ordner aus der IPM-Unterstruktur niemals.</span><span class="sxs-lookup"><span data-stu-id="af672-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="af672-113">Diese Ordner sollten für Nachrichten nur IPM reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="af672-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="af672-114">Verwenden Sie stattdessen einen Ordner wie, der ursprüngliche wird im Stammordner der Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="af672-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="af672-115">**Erstellen eines Ordners empfangen für eine Nachrichtenklasse IPM**</span><span class="sxs-lookup"><span data-stu-id="af672-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="af672-116">Rufen Sie den Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="af672-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="af672-117">Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) mit **PR_IPM_SUBTREE_ENTRYID** als die Eintrags-ID, um den Stammordner der IPM-Unterstruktur im Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="af672-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="af672-118">Rufen Sie [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) zum Erstellen des Ordners empfangen.</span><span class="sxs-lookup"><span data-stu-id="af672-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="af672-119">Rufen Sie [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) , um den neuen Ordner der Nachrichtenklasse IPM zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="af672-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="af672-120">**Erstellen eines Ordners empfangen für eine Nachrichtenklasse IPK**</span><span class="sxs-lookup"><span data-stu-id="af672-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="af672-121">Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) mit eine null Eintrags-ID, um den Stammordner des Nachrichtenspeichers zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="af672-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="af672-122">Rufen Sie [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) zum Erstellen des Ordners empfangen.</span><span class="sxs-lookup"><span data-stu-id="af672-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="af672-123">Rufen Sie [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) , um den neuen Ordner die Nachrichtenklasse IPK zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="af672-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="af672-124">Weisen Sie den Empfangsordner, den Sie für Nachrichten für verwandte Berichtnachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="af672-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="af672-125">Wenn beispielsweise Ihr Client IPM empfängt. Hinweis Nachrichten, richten Sie eine Empfangsordner für zukünftige IPM. Hinweis Nachrichten und die gleiche Empfangsordner für zukünftige Report.IPM.Note Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="af672-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

