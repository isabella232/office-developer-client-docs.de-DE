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
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405352"
---
# <a name="message-store-tables"></a><span data-ttu-id="ad568-103">Nachrichtenspeichertabellen</span><span class="sxs-lookup"><span data-stu-id="ad568-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="ad568-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad568-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad568-105">Die Nachrichtenspeichertabelle enthält Informationen zu Nachrichtenspeicher Anbietern im aktuellen Profil.</span><span class="sxs-lookup"><span data-stu-id="ad568-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="ad568-106">Es gibt eine Nachrichtenspeichertabelle für jede MAPI-Sitzung, die von MAPI implementiert und von Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad568-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="ad568-107">Clients können diese Tabelle verwenden, um beispielsweise alle Instanzen eines bestimmten Anbieters zu finden oder einen bestimmten Nachrichtenspeicher zu finden.</span><span class="sxs-lookup"><span data-stu-id="ad568-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="ad568-108">Die Nachrichtenspeichertabelle ist dynamisch.</span><span class="sxs-lookup"><span data-stu-id="ad568-108">The message store table is dynamic.</span></span> <span data-ttu-id="ad568-109">Wenn der Benutzer einer Clientanwendung das Profil bearbeitet und den Standardnachrichtenspeicher ändert, werden beispielsweise die Werte der **PR_DEFAULT_STORE** -Eigenschaften für die betroffenen Nachrichtenspeicher sofort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ad568-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="ad568-110">Clients greifen auf die Nachrichtenspeichertabelle zu, indem Sie die [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ad568-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="ad568-111">Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in der Nachrichtenspeichertabelle dar:</span><span class="sxs-lookup"><span data-stu-id="ad568-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad568-112">**PR_DEFAULT_STORE** ([Pidtagdefaultstore (](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ad568-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ad568-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ad568-115">**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ad568-116">**PR_MDB_PROVIDER** ([Pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ad568-117">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ad568-118">**PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ad568-119">**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ad568-120">**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ad568-121">**PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad568-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad568-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad568-122">See also</span></span>



[<span data-ttu-id="ad568-123">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="ad568-123">MAPI Tables</span></span>](mapi-tables.md)

