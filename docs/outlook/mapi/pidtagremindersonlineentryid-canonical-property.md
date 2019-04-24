---
title: Kanonische Pidtagremindersonlineentryid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d845a37f9248a30dadd4db7722d8bed0f9f8d264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355062"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a><span data-ttu-id="921cc-103">Kanonische Pidtagremindersonlineentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="921cc-103">PidTagRemindersOnlineEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="921cc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="921cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="921cc-105">Enthält die **Eintrags** -Nr. des Ordners "Erinnerungen".</span><span class="sxs-lookup"><span data-stu-id="921cc-105">Contains the **EntryID** of the reminders folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="921cc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="921cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="921cc-107">PR_REM_ONLINE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="921cc-107">PR_REM_ONLINE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="921cc-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="921cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="921cc-109">0x36D5</span><span class="sxs-lookup"><span data-stu-id="921cc-109">0x36D5</span></span>  <br/> |
|<span data-ttu-id="921cc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="921cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="921cc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="921cc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="921cc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="921cc-112">Area:</span></span>  <br/> |<span data-ttu-id="921cc-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="921cc-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="921cc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="921cc-114">Remarks</span></span>

<span data-ttu-id="921cc-115">Diese Eigenschaft wird im Ordner Posteingang und im Stammordner des Nachrichtenspeichers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="921cc-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="921cc-116">Gehen Sie folgendermaßen vor, um auf die Eigenschaft in einem bestimmten Nachrichtenspeicher zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="921cc-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="921cc-117">Suchen Sie zunächst nach der-Eigenschaft im Ordner Posteingang.</span><span class="sxs-lookup"><span data-stu-id="921cc-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="921cc-118">Verwenden Sie [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) , um einen Verweis auf die **Eintrags** -Nr. für den Posteingangsordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="921cc-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="921cc-119">Wenn **IMsgStore:: GetReceiveFolder** erfolgreich ist, verwenden Sie den Verweis auf die **Eintrags** -und [IMsgStore:: OpenEntry](imsgstore-openentry.md) , um den Posteingang zu öffnen und einen Verweis auf ein **IMAPIFolder** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="921cc-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="921cc-120">Wenn **IMsgStore:: OpenEntry** erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder** -Objekt und [IMAPIProp::](imapiprop-getprops.md) GetProps, um die gewünschte Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="921cc-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="921cc-121">Wenn Schritt 1, 2 oder 3 fehlschlägt, suchen Sie nach der Eigenschaft im Stammordner.</span><span class="sxs-lookup"><span data-stu-id="921cc-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="921cc-122">Zu diesem Zweck verwenden Sie **IMsgStore:: OpenEntry**, angeben von NULL für **lpEntryID**, um den Stammordner des Nachrichtenspeichers zu öffnen und einen Verweis auf das **IMAPIFolder** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="921cc-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="921cc-123">Wenn das Öffnen des Stammordners erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder** -Objekt und **IMAPIProp::** GetProps, um die gewünschte Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="921cc-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="921cc-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="921cc-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="921cc-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="921cc-125">Protocol specifications</span></span>

<span data-ttu-id="921cc-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="921cc-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="921cc-127">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="921cc-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="921cc-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="921cc-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="921cc-129">Gibt die Eigenschaften und Vorgänge zum Erstellen und suchen der speziellen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="921cc-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="921cc-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="921cc-130">Header files</span></span>

<span data-ttu-id="921cc-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="921cc-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="921cc-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="921cc-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="921cc-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="921cc-133">Mapitags.h</span></span>
  
> <span data-ttu-id="921cc-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="921cc-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="921cc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="921cc-135">See also</span></span>



[<span data-ttu-id="921cc-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="921cc-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="921cc-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="921cc-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="921cc-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="921cc-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="921cc-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="921cc-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

