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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384982"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="625ad-103">PidLidUseTnef (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="625ad-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="625ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="625ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="625ad-105">Gibt an, ob Transport Neutral Encapsulation Format (TNEF) für eine Nachricht eingeschlossen werden soll, wenn die Nachricht von MAPI (MULTIPURPOSE Internet Mail Extensions) oder Simple Mail Transfer Protocol (SMTP)-Format konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="625ad-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="625ad-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="625ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="625ad-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="625ad-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="625ad-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="625ad-108">Property set:</span></span>  <br/> |<span data-ttu-id="625ad-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="625ad-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="625ad-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="625ad-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="625ad-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="625ad-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="625ad-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="625ad-112">Data type:</span></span>  <br/> |<span data-ttu-id="625ad-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="625ad-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="625ad-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="625ad-114">Area:</span></span>  <br/> |<span data-ttu-id="625ad-115">Laufzeit-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="625ad-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="625ad-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="625ad-116">Remarks</span></span>

<span data-ttu-id="625ad-117">Diese Eigenschaft gibt an, ob TNEF für eine Nachricht eingeschlossen werden soll, wenn dieser Nachricht von TNEF in MIME- oder SMTP-Format konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="625ad-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="625ad-118">Diese Eigenschaft ist nicht vorhanden, und gegebenenfalls TNEF darf nicht enthalten sein für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="625ad-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="625ad-119">Diese Eigenschaft gilt nur, wenn die Nachricht aus einem POP3/SMTP-Mail-Konto gesendet wird und wird nicht angewendet, wenn die Nachricht von anderen Anbietern wie beispielsweise Microsoft Exchange Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="625ad-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="625ad-120">Unter bestimmten Umständen wie beim Stimmabgabe Schaltflächen aktiviert sind, oder eine OLE eingebettete Objekt an eine Nachricht angefügt ist kann Outlook diese Eigenschaft so erzwingen Sie die Verwendung von TNEF festlegen.</span><span class="sxs-lookup"><span data-stu-id="625ad-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="625ad-121">Die **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md))-Eigenschaft kann nur nur-Text und nicht-TNEF zu erzwingen, beim Senden einer Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="625ad-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="625ad-122">Da **PidLidUseTNEF** die Einstellung in **PR_MSG_EDITOR_FORMAT**überschreibt, sollte auch eine Anwendung, die nur-Text für eine ausgehende Nachricht erzwingen möchte **PidLidUseTNEF** suchen und ihn auf FALSE zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="625ad-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="625ad-123">Darüber hinaus muss das Add-in die Nachrichtenfunktionen entfernen, die TNEF benötigen, um Endbenutzern nicht genutzt werden Anlagen für die Nachricht zu vermeiden, die schließlich gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="625ad-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="625ad-124">Verwenden Sie das Kennzeichen **CCSF_USE_TNEF** beim Aufruf von [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) zum Konvertieren einer ausgehenden MAPI-Nachricht in einen MIME-Stream kann auch TNEF durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="625ad-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="625ad-125">Dies gilt, auch wenn **PidLidUseTNEF** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="625ad-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="625ad-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="625ad-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="625ad-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="625ad-127">Protocol specifications</span></span>

<span data-ttu-id="625ad-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="625ad-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="625ad-129">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="625ad-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="625ad-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="625ad-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="625ad-131">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="625ad-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="625ad-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="625ad-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="625ad-133">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="625ad-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="625ad-134">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="625ad-134">Header files</span></span>

<span data-ttu-id="625ad-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="625ad-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="625ad-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="625ad-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="625ad-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="625ad-137">See also</span></span>



[<span data-ttu-id="625ad-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="625ad-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="625ad-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="625ad-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="625ad-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="625ad-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="625ad-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="625ad-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

