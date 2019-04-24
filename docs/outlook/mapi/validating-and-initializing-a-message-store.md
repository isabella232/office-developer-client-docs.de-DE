---
title: ÜberPrüfen und Initialisieren eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329582"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="8216f-103">ÜberPrüfen und Initialisieren eines Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="8216f-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="8216f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8216f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8216f-105">Wenn Sie einen Nachrichtenspeicher über die [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) -Methode öffnen, ohne das MDB_NO_MAIL-Flag festzulegen, erstellt MAPI mehrere Ordner und weist Ihnen Standardnamen und Rollen zu.</span><span class="sxs-lookup"><span data-stu-id="8216f-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="8216f-106">MAPI ist für die Erstellung dieser Ordner verantwortlich, um die Unverträglichkeiten zu vermeiden, die unvermeidlich wären, wenn entweder Clients oder Nachrichtenspeicher Anbieter für die Erstellung verantwortlich waren.</span><span class="sxs-lookup"><span data-stu-id="8216f-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="8216f-107">Manchmal muss überprüft werden, ob die entsprechenden Ordner erstellt wurden und dass Sie gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8216f-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="8216f-108">Die [HrValidateIPMSubtree](hrvalidateipmsubtree.md) -Funktion steht zu diesem Zweck zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8216f-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="8216f-109">Wenn Sie den Standardnachrichtenspeicher überprüfen, führen Sie das MAPI_FULL_IPM_TREE-Flag aus.</span><span class="sxs-lookup"><span data-stu-id="8216f-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="8216f-110">Eine umfangreichere Gruppe von Ordnern wird für den Standardnachrichtenspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="8216f-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="8216f-111">Wenn **HrValidateIPMSubtree** das MAPI_FULL_IPM_TREE-Flag erhält, prüft es die folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="8216f-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="8216f-112">Stammordner für die IPM-Unterstruktur</span><span class="sxs-lookup"><span data-stu-id="8216f-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="8216f-113">Ordner "Gelöschte Elemente" im IPM-Stammordner</span><span class="sxs-lookup"><span data-stu-id="8216f-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="8216f-114">PostEingangsordner im IPM-Stammordner</span><span class="sxs-lookup"><span data-stu-id="8216f-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="8216f-115">Ausgangsordner im IPM-Stammordner</span><span class="sxs-lookup"><span data-stu-id="8216f-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="8216f-116">Ordner "Gesendete Elemente" im IPM-Stammordner</span><span class="sxs-lookup"><span data-stu-id="8216f-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="8216f-117">Ordneransichten im Stammordner des Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="8216f-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="8216f-118">Allgemeine Ansichten im Stammordner des Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="8216f-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="8216f-119">Suchordner im Stammordner des Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="8216f-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="8216f-120">Wenn der Nachrichtenspeicher nicht der Standardwert ist, können Sie das MAPI_FULL_IPM_TREE-Flag festlegen oder nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="8216f-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="8216f-121">Wenn dieses Flag nicht festgelegt ist, sucht **HrValidateIPMSubtree** nur nach dem Stammordner für die Unterstruktur, dem Ordner "Gelöschte Elemente" und dem Stammordner für die Suchergebnisse des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="8216f-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="8216f-122">Um einen Nachrichtenspeicher zu initialisieren, speichern Sie die folgenden Eigenschaften im Arbeitsspeicher, damit Sie sofort verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="8216f-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="8216f-123">**PR_VALID_FOLDER_MASK** ([Pidtagvalidfoldermask (](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8216f-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="8216f-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8216f-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="8216f-125">Diese Eigenschaften sind Bitmasken, die Features des Nachrichtenspeichers beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8216f-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="8216f-126">**PR_VALID_FOLDER_MASK** hat ein Bit für jeden speziellen Ordner festgelegt, der im Nachrichtenspeicher vorhanden ist und einen gültigen Eintragsbezeichner besitzt.</span><span class="sxs-lookup"><span data-stu-id="8216f-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="8216f-127">Weitere Informationen zum Zugriff auf diese Ordner und ihre Eintragsbezeichner finden Sie unter [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="8216f-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="8216f-128">**PR_STORE_SUPPORT_MASK** hat für jedes im Nachrichtenspeicher unterstützte Feature ein Bit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8216f-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="8216f-129">Wenn beispielsweise ein Nachrichtenspeicher Benachrichtigungen und formatierten Text unterstützt, werden für dessen **PR_STORE_SUPPORT_MASK** die Bits STORE_NOTIFY_OK und STORE_RTF_OK festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8216f-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="8216f-130">Andere Eigenschaften, die lokal gespeichert werden sollen, sind die Eintrags-IDs für die Ordner, die von der **PR_VALID_FOLDER_MASK** -Eigenschaft als gültig beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8216f-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="8216f-131">Jedem dieser speziellen Ordner, mit Ausnahme des Ordners "Inbox", ist eine Eintrags-ID-Eigenschaft zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8216f-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="8216f-132">Beispielsweise ist die Eintrags-ID für den Ordner Postausgang Ihre **PR_IPM_OUTBOX_ENTRYID** ([pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8216f-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="8216f-133">Da es sich bei diesen Ordnern um die Ordner handelt, die häufig geöffnet werden, empfiehlt es sich, die Eingabe Kennungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8216f-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

