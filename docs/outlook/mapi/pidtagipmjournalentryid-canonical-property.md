---
title: Kanonische Pidtagipmjournalentryid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmJournalEntryId
api_type:
- HeaderDef
ms.assetid: a3765b9d-a108-46d7-a97c-a825ae3980be
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b5dfc378a2558e906bec018608e2d2c776090c06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327909"
---
# <a name="pidtagipmjournalentryid-canonical-property"></a><span data-ttu-id="473d2-103">Kanonische Pidtagipmjournalentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="473d2-103">PidTagIpmJournalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="473d2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="473d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="473d2-105">Enthält die **Eintrags** -Nr. des Outlook-Journal Ordners.</span><span class="sxs-lookup"><span data-stu-id="473d2-105">Contains the **EntryID** of the Outlook Journal folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="473d2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="473d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="473d2-107">PR_IPM_JOURNAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="473d2-107">PR_IPM_JOURNAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="473d2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="473d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="473d2-109">0x36D2</span><span class="sxs-lookup"><span data-stu-id="473d2-109">0x36D2</span></span>  <br/> |
|<span data-ttu-id="473d2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="473d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="473d2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="473d2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="473d2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="473d2-112">Area:</span></span>  <br/> |<span data-ttu-id="473d2-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="473d2-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="473d2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="473d2-114">Remarks</span></span>

<span data-ttu-id="473d2-115">Diese Eigenschaft wird im Ordner Posteingang und im Stammordner des Nachrichtenspeichers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="473d2-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="473d2-116">Gehen Sie folgendermaßen vor, um auf die Eigenschaft in einem bestimmten Nachrichtenspeicher zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="473d2-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="473d2-117">Suchen Sie zunächst nach der-Eigenschaft im Ordner Posteingang.</span><span class="sxs-lookup"><span data-stu-id="473d2-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="473d2-118">Verwenden Sie [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) , um einen Verweis auf die **Eintrags** -Nr. für den Posteingangsordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="473d2-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="473d2-119">Wenn **IMsgStore:: GetReceiveFolder** erfolgreich ist, verwenden Sie den Verweis auf die **Eintrags** -und [IMsgStore:: OpenEntry](imsgstore-openentry.md) , um den Posteingang zu öffnen und einen Verweis auf ein **IMAPIFolder** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="473d2-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="473d2-120">Wenn **IMsgStore:: OpenEntry** erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder** -Objekt und [IMAPIProp::](imapiprop-getprops.md) GetProps, um die gewünschte Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="473d2-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="473d2-121">Wenn Schritt 1, 2 oder 3 fehlschlägt, suchen Sie nach der Eigenschaft im Stammordner.</span><span class="sxs-lookup"><span data-stu-id="473d2-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="473d2-122">Zu diesem Zweck verwenden Sie **IMsgStore:: OpenEntry**, angeben von NULL für **lpEntryID**, um den Stammordner des Nachrichtenspeichers zu öffnen und einen Verweis auf das **IMAPIFolder** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="473d2-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="473d2-123">Wenn das Öffnen des Stammordners erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder** -Objekt und **IMAPIProp::** GetProps, um die gewünschte Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="473d2-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="473d2-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="473d2-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="473d2-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="473d2-125">Protocol specifications</span></span>

<span data-ttu-id="473d2-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="473d2-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="473d2-127">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="473d2-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="473d2-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="473d2-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="473d2-129">Gibt die Eigenschaften und Vorgänge zum Erstellen und suchen der speziellen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="473d2-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="473d2-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="473d2-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="473d2-131">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="473d2-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="473d2-132">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="473d2-132">Header files</span></span>

<span data-ttu-id="473d2-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="473d2-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="473d2-134">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="473d2-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="473d2-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="473d2-135">Mapitags.h</span></span>
  
> <span data-ttu-id="473d2-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="473d2-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="473d2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="473d2-137">See also</span></span>



[<span data-ttu-id="473d2-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="473d2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="473d2-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="473d2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="473d2-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="473d2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="473d2-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="473d2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

