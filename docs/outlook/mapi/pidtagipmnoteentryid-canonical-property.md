---
title: Kanonische PidTagIpmNoteEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmNoteEntryId
api_type:
- HeaderDef
ms.assetid: c003f7b9-b0cd-4656-98fa-3466fda6832c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1d46110585fb5075041942560b3a8bd5d0b125a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794531"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a><span data-ttu-id="9cbd4-103">Kanonische PidTagIpmNoteEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9cbd4-103">PidTagIpmNoteEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9cbd4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9cbd4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9cbd4-105">Die **EntryID** des Ordners Outlook-Notizen enthält.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-105">Contains the **EntryID** of the Outlook Notes folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cbd4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9cbd4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cbd4-107">PR_IPM_NOTE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9cbd4-107">PR_IPM_NOTE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="9cbd4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="9cbd4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9cbd4-109">0x36D3</span><span class="sxs-lookup"><span data-stu-id="9cbd4-109">0x36D3</span></span>  <br/> |
|<span data-ttu-id="9cbd4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9cbd4-110">Data type:</span></span>  <br/> |<span data-ttu-id="9cbd4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9cbd4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9cbd4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9cbd4-112">Area:</span></span>  <br/> |<span data-ttu-id="9cbd4-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="9cbd4-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cbd4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9cbd4-114">Remarks</span></span>

<span data-ttu-id="9cbd4-115">Diese Eigenschaft wird in den Ordner Posteingang als auch im Stammordner des Nachrichtenspeichers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="9cbd4-116">Zugriff auf die Eigenschaft auf einen bestimmten Nachrichtenspeicher folgendermaßen Sie vor:</span><span class="sxs-lookup"><span data-stu-id="9cbd4-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="9cbd4-117">Suchen Sie zunächst nach der Eigenschaft im Ordner Posteingang.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="9cbd4-118">Verwenden Sie [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , um einen Verweis auf die **Eintrags-ID** für den Ordner Posteingang abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="9cbd4-119">Wenn ** IMsgStore::GetReceiveFolder ** erfolgreich ausgeführt wurde, und klicken Sie dann den Verweis auf die **EntryID** des Posteingang und [IMsgStore::OpenEntry](imsgstore-openentry.md) verwenden, um den Posteingang zu öffnen, und rufen Sie einen Verweis auf ein Objekt **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="9cbd4-119">If ** IMsgStore::GetReceiveFolder ** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="9cbd4-120">Wenn **IMsgStore::OpenEntry** erfolgreich ist, müssen verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder** -Objekt und [IMAPIProp::GetProps](imapiprop-getprops.md) dann, um die gewünschte Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="9cbd4-121">Wenn Schritt 1, 2 oder 3 fehlschlägt, suchen Sie nach der-Eigenschaft im Stammordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="9cbd4-122">Verwenden Sie hierzu **IMsgStore::OpenEntry**, Angeben von NULL für die **LpEntryID**, um den Stammordner des Nachrichtenspeichers öffnen, und rufen Sie einen Verweis auf das **IMAPIFolder** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="9cbd4-123">Wenn Stammordner öffnen erfolgreich ist, müssen verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder** -Objekt und **IMAPIProp::GetProps** dann, um die gewünschte Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="9cbd4-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9cbd4-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cbd4-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9cbd4-125">Protocol specifications</span></span>

<span data-ttu-id="9cbd4-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cbd4-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cbd4-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9cbd4-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cbd4-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cbd4-129">Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="9cbd4-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cbd4-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cbd4-131">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9cbd4-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9cbd4-132">Header files</span></span>

<span data-ttu-id="9cbd4-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cbd4-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cbd4-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="9cbd4-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9cbd4-135">Mapitags.h</span></span>
  
> <span data-ttu-id="9cbd4-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9cbd4-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cbd4-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cbd4-137">See also</span></span>



[<span data-ttu-id="9cbd4-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cbd4-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cbd4-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cbd4-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cbd4-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9cbd4-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cbd4-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9cbd4-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

