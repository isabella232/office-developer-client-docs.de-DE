---
title: PidLidUseTnef (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315421"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="4e4ab-103">PidLidUseTnef (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4e4ab-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="4e4ab-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e4ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e4ab-105">Gibt an, ob das TNEF (Transport Neutral Encapsulation Format) in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von MAPI in mime (Multipurpose Internet Mail Extensions) oder SMTP (Simple Mail Transfer Protocol) konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e4ab-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4e4ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e4ab-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="4e4ab-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="4e4ab-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="4e4ab-108">Property set:</span></span>  <br/> |<span data-ttu-id="4e4ab-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4e4ab-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4e4ab-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4e4ab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4e4ab-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="4e4ab-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="4e4ab-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4e4ab-112">Data type:</span></span>  <br/> |<span data-ttu-id="4e4ab-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4e4ab-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4e4ab-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4e4ab-114">Area:</span></span>  <br/> |<span data-ttu-id="4e4ab-115">Laufzeitkonfiguration</span><span class="sxs-lookup"><span data-stu-id="4e4ab-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e4ab-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e4ab-116">Remarks</span></span>

<span data-ttu-id="4e4ab-117">Diese Eigenschaft gibt an, ob TNEF in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von TNEF in das MIME- oder SMTP-Format konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="4e4ab-118">Diese Eigenschaft ist möglicherweise nicht vorhanden, und falls ja, darf TNEF nicht in die Nachricht eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="4e4ab-119">Diese Eigenschaft gilt nur, wenn die Nachricht von einem POP3/SMTP-E-Mail-Konto gesendet wird und nicht angewendet wird, wenn die Nachricht von anderen Anbietern gesendet wird, z. B. Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="4e4ab-120">Unter bestimmten Umständen, z. B. wenn Abstimmungsschaltflächen aktiviert sind oder ein eingebettetes OLE-Objekt an eine Nachricht angefügt ist, kann Outlook diese Eigenschaft so festlegen, dass die Verwendung von TNEF erzwingen wird.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="4e4ab-121">Die **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) kann verwendet werden, um beim Senden einer Nachricht nur Nur-Text und nicht TNEF zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="4e4ab-122">Da **PidLidUseTNEF** die Einstellung in **PR_MSG_EDITOR_FORMAT** außer Kraft setzt, sollte eine Anwendung, die Nur-Text für eine ausgehende Nachricht erzwingen möchte, auch **nach PidLidUseTNEF** suchen und auf FALSE zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="4e4ab-123">Darüber hinaus muss das Add-In die Nachrichtenfeatures entfernen, für die TNEF erforderlich war, um unbrauchbare Anlagen für die Nachricht zu vermeiden, die schließlich gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="4e4ab-124">Verwenden Sie **das CCSF_USE_TNEF** beim Aufrufen von [IConverterSession::MAPIToMIMEStm,](iconvertersession-mapitomimestm.md) um eine ausgehende MAPI-Nachricht in einen MIME-Stream zu konvertieren, um auch TNEF zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="4e4ab-125">Dies gilt auch dann, **wenn PidLidUseTNEF** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4e4ab-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4e4ab-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e4ab-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4e4ab-127">Protocol specifications</span></span>

<span data-ttu-id="4e4ab-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e4ab-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e4ab-129">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e4ab-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e4ab-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e4ab-131">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4e4ab-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e4ab-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e4ab-133">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e4ab-134">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4e4ab-134">Header files</span></span>

<span data-ttu-id="4e4ab-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e4ab-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e4ab-136">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4e4ab-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e4ab-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e4ab-137">See also</span></span>



[<span data-ttu-id="4e4ab-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e4ab-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e4ab-139">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4e4ab-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e4ab-140">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4e4ab-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e4ab-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4e4ab-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

