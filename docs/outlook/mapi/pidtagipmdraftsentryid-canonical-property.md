---
title: PidTagIpmDraftsEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmDraftsEntryId
api_type:
- HeaderDef
ms.assetid: 17d64211-6265-41f4-b016-3677d75af966
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e259c86803147d782469c8d86b23694d8b54e69d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327888"
---
# <a name="pidtagipmdraftsentryid-canonical-property"></a><span data-ttu-id="5dc07-103">PidTagIpmDraftsEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5dc07-103">PidTagIpmDraftsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5dc07-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dc07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dc07-105">Enthält die **EntryID** des ordners Outlook Drafts.</span><span class="sxs-lookup"><span data-stu-id="5dc07-105">Contains the **EntryID** of the Outlook Drafts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5dc07-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5dc07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5dc07-107">PR_IPM_DRAFTS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5dc07-107">PR_IPM_DRAFTS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5dc07-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5dc07-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5dc07-109">0x36D7</span><span class="sxs-lookup"><span data-stu-id="5dc07-109">0x36D7</span></span>  <br/> |
|<span data-ttu-id="5dc07-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5dc07-110">Data type:</span></span>  <br/> |<span data-ttu-id="5dc07-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5dc07-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5dc07-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5dc07-112">Area:</span></span>  <br/> |<span data-ttu-id="5dc07-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="5dc07-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dc07-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5dc07-114">Remarks</span></span>

<span data-ttu-id="5dc07-115">Diese Eigenschaft wird im Ordner Posteingang sowie im Stammordner des Nachrichtenspeichers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5dc07-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="5dc07-116">Gehen Sie wie folgt vor, um auf die Eigenschaft in einem bestimmten Nachrichtenspeicher zu zugreifen:</span><span class="sxs-lookup"><span data-stu-id="5dc07-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="5dc07-117">Suchen Sie zunächst im Ordner Posteingang nach der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5dc07-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="5dc07-118">Verwenden [Sie IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) um einen Verweis auf die **EntryID** für den Posteingangsordner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dc07-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="5dc07-119">Wenn **IMsgStore::GetReceiveFolder** erfolgreich ist, verwenden Sie den Verweis auf die **EntryID** des Posteingangs und [IMsgStore::OpenEntry,](imsgstore-openentry.md) um den Posteingang zu öffnen und einen Verweis auf ein **IMAPIFolder-Objekt** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dc07-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="5dc07-120">Wenn **IMsgStore::OpenEntry** erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder-Objekt** und [IMAPIProp::GetProps,](imapiprop-getprops.md) um die gewünschte Eigenschaft zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dc07-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="5dc07-121">Wenn in Schritt 1, 2 oder 3 ein Fehler auftritt, suchen Sie im Stammordner nach der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5dc07-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="5dc07-122">Verwenden Sie **dazu IMsgStore::OpenEntry,** und geben Sie NULL für **lpEntryID** an, um den Stammordner des Nachrichtenspeichers zu öffnen und einen Verweis auf das **IMAPIFolder-Objekt** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dc07-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="5dc07-123">Wenn das Öffnen des Stammordners erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder-Objekt** und **IMAPIProp::GetProps,** um die gewünschte Eigenschaft zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dc07-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="5dc07-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5dc07-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5dc07-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5dc07-125">Protocol specifications</span></span>

<span data-ttu-id="5dc07-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dc07-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dc07-127">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5dc07-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5dc07-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dc07-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dc07-129">Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="5dc07-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5dc07-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5dc07-130">Header files</span></span>

<span data-ttu-id="5dc07-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5dc07-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5dc07-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5dc07-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5dc07-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5dc07-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5dc07-134">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5dc07-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5dc07-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dc07-135">See also</span></span>



[<span data-ttu-id="5dc07-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5dc07-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5dc07-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5dc07-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5dc07-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5dc07-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5dc07-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5dc07-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

