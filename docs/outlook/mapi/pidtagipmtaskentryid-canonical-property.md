---
title: PidTagIpmTaskEntryId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aa1c4979ce66a0e32aea7b04ef4412679545b3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794535"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="db5ec-103">PidTagIpmTaskEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="db5ec-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="db5ec-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db5ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db5ec-105">Die **EntryID** des Ordners Outlook-Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="db5ec-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db5ec-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="db5ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db5ec-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="db5ec-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="db5ec-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="db5ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db5ec-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="db5ec-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="db5ec-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="db5ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="db5ec-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="db5ec-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="db5ec-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="db5ec-112">Area:</span></span>  <br/> |<span data-ttu-id="db5ec-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="db5ec-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db5ec-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db5ec-114">Remarks</span></span>

<span data-ttu-id="db5ec-115">Diese Eigenschaft lesen oder mithilfe des Protokolls-Eigenschaft und Stream-Objekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="db5ec-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="db5ec-116">Es ist lesen und Schreiben in den Ordner Posteingang oder Root.</span><span class="sxs-lookup"><span data-stu-id="db5ec-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="db5ec-117">Die Implementierung muss den Ordner Posteingang verwenden, wenn der Informationsspeicher, die von der primären messaging-Benutzer ist und den Stammordner verwendet werden muss, wenn der Informationsspeicher, ein Stellvertreter ist.</span><span class="sxs-lookup"><span data-stu-id="db5ec-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="db5ec-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db5ec-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db5ec-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="db5ec-119">Protocol specifications</span></span>

<span data-ttu-id="db5ec-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db5ec-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db5ec-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="db5ec-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db5ec-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db5ec-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db5ec-123">Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="db5ec-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="db5ec-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db5ec-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db5ec-125">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="db5ec-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db5ec-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="db5ec-126">Header files</span></span>

<span data-ttu-id="db5ec-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db5ec-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="db5ec-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="db5ec-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="db5ec-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="db5ec-129">Mapitags.h</span></span>
  
> <span data-ttu-id="db5ec-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="db5ec-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db5ec-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db5ec-131">See also</span></span>



[<span data-ttu-id="db5ec-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db5ec-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db5ec-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db5ec-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db5ec-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="db5ec-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db5ec-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="db5ec-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

