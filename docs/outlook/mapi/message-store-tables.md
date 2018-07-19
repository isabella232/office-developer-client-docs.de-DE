---
title: Nachrichtenspeichertabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793272"
---
# <a name="message-store-tables"></a><span data-ttu-id="e2593-103">Nachrichtenspeichertabellen</span><span class="sxs-lookup"><span data-stu-id="e2593-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="e2593-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2593-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2593-105">Die Nachricht Store-Tabelle enthält Informationen zu Anbietern Nachricht im aktuellen Profil.</span><span class="sxs-lookup"><span data-stu-id="e2593-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="e2593-106">Es wird eine Meldung Store-Tabelle für jedes MAPI-Sitzung von MAPI implementiert und von Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2593-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="e2593-107">Clients können diese Tabelle beispielsweise nach allen Instanzen eines bestimmten Anbieters suchen oder suchen Sie einen bestimmten Nachrichtenspeicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2593-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="e2593-108">Die Tabelle Store ist dynamisch.</span><span class="sxs-lookup"><span data-stu-id="e2593-108">The message store table is dynamic.</span></span> <span data-ttu-id="e2593-109">Wenn der Benutzer von einer Clientanwendung aus das Profil bearbeitet, werden, Ändern der Standard-Informationsspeicher, beispielsweise die Werte der **PR_DEFAULT_STORE** Eigenschaften für die betroffenen Nachrichtenspeicher unmittelbar aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e2593-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="e2593-110">Clientzugriff durch Aufrufen der Methode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) die Nachricht Store-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e2593-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="e2593-111">Die folgenden Eigenschaften bilden die erforderliche Spalte in der Nachricht Store Tabelle festgelegt:</span><span class="sxs-lookup"><span data-stu-id="e2593-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2593-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e2593-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e2593-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e2593-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e2593-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e2593-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e2593-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e2593-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e2593-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e2593-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e2593-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2593-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2593-122">See also</span></span>



[<span data-ttu-id="e2593-123">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="e2593-123">MAPI Tables</span></span>](mapi-tables.md)

