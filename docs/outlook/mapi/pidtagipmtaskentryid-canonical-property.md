---
title: Kanonische Pidtagipmtaskentryid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c3845c745dcd2c18525f147308233b94fbce70d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327844"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="83016-103">Kanonische Pidtagipmtaskentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="83016-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="83016-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83016-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83016-105">Enthält die **Eintrags** -Nr. des Outlook-Aufgabenordners.</span><span class="sxs-lookup"><span data-stu-id="83016-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83016-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="83016-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="83016-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="83016-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="83016-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="83016-108">Identifier:</span></span>  <br/> |<span data-ttu-id="83016-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="83016-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="83016-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="83016-110">Data type:</span></span>  <br/> |<span data-ttu-id="83016-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="83016-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="83016-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="83016-112">Area:</span></span>  <br/> |<span data-ttu-id="83016-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="83016-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83016-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83016-114">Remarks</span></span>

<span data-ttu-id="83016-115">Diese Eigenschaft wird mithilfe der Eigenschaft und des Stream-Objekt Protokolls gelesen oder geschrieben.</span><span class="sxs-lookup"><span data-stu-id="83016-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="83016-116">Sie wird aus dem Posteingang oder Stammordner gelesen und in diesen geschrieben.</span><span class="sxs-lookup"><span data-stu-id="83016-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="83016-117">Die Implementierung muss den Ordner Posteingang verwenden, wenn es sich um den Speicher des primären Messaging Benutzers handelt, und Sie muss den Stammordner verwenden, wenn der Speicher der eines Stellvertreters ist.</span><span class="sxs-lookup"><span data-stu-id="83016-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="83016-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="83016-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="83016-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="83016-119">Protocol specifications</span></span>

<span data-ttu-id="83016-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83016-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83016-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="83016-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="83016-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83016-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83016-123">Gibt die Eigenschaften und Vorgänge zum Erstellen und suchen der speziellen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="83016-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="83016-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83016-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83016-125">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="83016-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="83016-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="83016-126">Header files</span></span>

<span data-ttu-id="83016-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="83016-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="83016-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="83016-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="83016-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="83016-129">Mapitags.h</span></span>
  
> <span data-ttu-id="83016-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="83016-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83016-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83016-131">See also</span></span>



[<span data-ttu-id="83016-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83016-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="83016-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83016-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="83016-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="83016-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="83016-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="83016-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

