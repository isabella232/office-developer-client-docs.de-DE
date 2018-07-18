---
title: Überprüfen und Initialisieren eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48883ec33db9ffd6b3e7cc6e16ae9c2487a31607
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795847"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="1f8ac-103">Überprüfen und Initialisieren eines Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="1f8ac-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="1f8ac-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f8ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f8ac-105">Beim Öffnen eines Nachrichtenspeichers über die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode ohne das MDB_NO_MAIL-Flag MAPI mehrere Ordner erstellt und ihnen Standardnamen und Rollen zuweist.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="1f8ac-106">MAPI ist verantwortlich für die Erstellung dieser Ordner um Inkompatibilitäten zu vermeiden, die zwangsläufig auftreten würde, wenn Clients oder Nachricht Anbieter verantwortlich für die Erstellung wurden.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="1f8ac-107">In einigen Fällen ist es erforderlich, um sicherzustellen, dass die entsprechenden Ordner erstellt wurden und dass sie gültig sind.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="1f8ac-108">Die [HrValidateIPMSubtree](hrvalidateipmsubtree.md) -Funktion ist für diesen Zweck verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="1f8ac-109">Wenn Sie den standardmäßigen Nachrichtenspeicher überprüfen, übergeben Sie die Kennzeichen MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="1f8ac-110">Eine umfangreichere Gruppe von Ordnern wird für den standardmäßigen Nachrichtenspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="1f8ac-111">Wenn **HrValidateIPMSubtree** das Flag MAPI_FULL_IPM_TREE empfängt, überprüft es die folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="1f8ac-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="1f8ac-112">Stammordner für die IPM-Unterstruktur</span><span class="sxs-lookup"><span data-stu-id="1f8ac-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="1f8ac-113">Ordner Gelöschte Objekte im Stammordner IPM</span><span class="sxs-lookup"><span data-stu-id="1f8ac-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="1f8ac-114">Ordner Posteingang im Stammordner IPM</span><span class="sxs-lookup"><span data-stu-id="1f8ac-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="1f8ac-115">Postausgang im Stammordner IPM</span><span class="sxs-lookup"><span data-stu-id="1f8ac-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="1f8ac-116">Ordner Gesendete Objekte im Stammordner IPM</span><span class="sxs-lookup"><span data-stu-id="1f8ac-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="1f8ac-117">Ansichten für Ordner im Stammordner der Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="1f8ac-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="1f8ac-118">Allgemeine Ansichten im Stammordner der Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="1f8ac-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="1f8ac-119">Suchordner im Stammordner der Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="1f8ac-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="1f8ac-120">Ist der Nachrichtenspeicher nicht Standard, können Sie festlegen oder das Flag MAPI_FULL_IPM_TREE nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="1f8ac-121">Wenn dieses Flag **HrValidateIPMSubtree** prüft, ob nur den Stammordner für die Unterstruktur nicht festgelegt ist, speichern den Ordner Gelöschte Objekte und der Stammordner für Nachricht Suchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="1f8ac-122">Um einen Nachrichtenspeicher initialisieren, speichern Sie die folgenden Eigenschaften im Arbeitsspeicher, damit sie verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="1f8ac-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="1f8ac-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f8ac-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="1f8ac-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f8ac-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="1f8ac-125">Diese Eigenschaften sind Bitmasken, die Features des Nachrichtenspeichers beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="1f8ac-126">**PR_VALID_FOLDER_MASK** verfügt über ein Bit für jeden speziellen Ordner, der im Nachrichtenspeicher vorhanden ist und verfügt über einen Eintrag zugewiesene Bezeichner, der gültig ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="1f8ac-127">Weitere Informationen zu den Zugriff auf diese Ordner und ihre Eintragsbezeichner finden Sie unter [Öffnen einen Speicherordner Nachricht](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="1f8ac-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="1f8ac-128">**PR_STORE_SUPPORT_MASK** verfügt über ein Bit für jedes Feature im Nachrichtenspeicher unterstützt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="1f8ac-129">Beispielsweise wenn ein Nachrichtenspeicher Benachrichtigung und formatierten Text unterstützt, haben dessen **PR_STORE_SUPPORT_MASK** die STORE_NOTIFY_OK und STORE_RTF_OK Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="1f8ac-130">Andere Eigenschaften, die lokal gespeichert werden sollen enthalten den Eintrag-IDs für die Ordner, die die **PR_VALID_FOLDER_MASK** -Eigenschaft als gültig beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="1f8ac-131">Jeder dieser speziellen Ordner, mit Ausnahme der Ordner Posteingang verfügt über eine Eintrags-ID-Eigenschaft zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="1f8ac-132">Beispielsweise wird die Eintrags-ID für den Ordner Postausgang seiner **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="1f8ac-133">Da diese Ordner die Ordner, die häufig geöffnet wird sind, ist es ratsam, haben ihre Eintragsbezeichner immer leicht zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="1f8ac-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

