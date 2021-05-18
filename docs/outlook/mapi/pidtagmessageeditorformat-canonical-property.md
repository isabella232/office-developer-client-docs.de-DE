---
title: PidTagMessageEditorFormat (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325634"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="0ab3d-103">PidTagMessageEditorFormat (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0ab3d-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="0ab3d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ab3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ab3d-105">Gibt das Format für einen Editor an, der zum Anzeigen einer Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ab3d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0ab3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ab3d-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="0ab3d-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="0ab3d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0ab3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ab3d-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="0ab3d-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="0ab3d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0ab3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ab3d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0ab3d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0ab3d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0ab3d-112">Area:</span></span>  <br/> |<span data-ttu-id="0ab3d-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="0ab3d-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ab3d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0ab3d-114">Remarks</span></span>

<span data-ttu-id="0ab3d-115">Die möglichen Werte **für PR_MSG_EDITOR_FORMAT** können einer der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="0ab3d-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="0ab3d-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0ab3d-116">**Value**</span></span>|<span data-ttu-id="0ab3d-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ab3d-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ab3d-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="0ab3d-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="0ab3d-119">Das Zu verwendende Format des Editors ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="0ab3d-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="0ab3d-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="0ab3d-121">Der Editor sollte die Nachricht im Nur-Text-Format anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="0ab3d-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="0ab3d-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="0ab3d-123">Der Editor sollte die Nachricht im HTML-Format anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="0ab3d-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="0ab3d-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="0ab3d-125">Der Editor sollte die Nachricht im Rich-Text-Format anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="0ab3d-126">Standardmäßig E-Mail-Nachrichten (mit der Nachrichtenklasse **IPM. Hinweis** oder mit einer benutzerdefinierten Nachrichtenklasse, die von **IPM abgeleitet ist. Hinweis**) von einem POP3/SMTP-E-Mail-Konto gesendet werden im Transport Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="0ab3d-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="0ab3d-127">Die **PR_MSG_EDITOR_FORMAT-Eigenschaft** kann verwendet werden, um beim Senden einer Nachricht nur Nur-Text und nicht TNEF zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="0ab3d-128">Wenn **PR_MSG_EDITOR_FORMAT** auf EDITOR_FORMAT_PLAINTEXT **festgelegt** ist, wird die Nachricht als Nur-Text-Nachricht ohne TNEF gesendet.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="0ab3d-129">Wenn **PR_MSG_EDITOR_FORMAT** auf **EDITOR_FORMAT_RTF** festgelegt ist, ist die TNEF-Codierung implizit aktiviert, und die Nachricht wird mithilfe des standardmäßigen Internetformats gesendet, das im Outlook ist.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="0ab3d-130">Es gibt zwei weitere Möglichkeiten, die Verwendung von TNEF beim Senden einer Nachricht zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="0ab3d-131">Das Festlegen der **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) benannten Eigenschaft auf True in einer Nachricht gibt an, dass TNEF beim Konvertieren der Nachricht von MAPI in MIME/SMTP enthalten sein sollte.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="0ab3d-132">Beachten Sie, dass **dispidUseTNEF** nur gilt, wenn die Nachricht von einem POP3/SMTP-E-Mail-Konto gesendet wird, und gilt nicht, wenn die Nachricht von anderen Anbietern gesendet wird, z. B. Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="0ab3d-133">**dispidUseTNEF** überschreibt die Einstellung in **PR_MSG_EDITOR_FORMAT**.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="0ab3d-134">Das **CCSF_USE_TNEF** beim Aufrufen von [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) zum Konvertieren einer ausgehenden MAPI-Nachricht in einen MIME-Stream kann auch TNEF erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="0ab3d-135">Dies gilt auch **dann, wenn dispidUseTNEF** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="0ab3d-136">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0ab3d-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ab3d-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0ab3d-137">Protocol specifications</span></span>

<span data-ttu-id="0ab3d-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ab3d-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ab3d-139">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ab3d-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ab3d-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ab3d-141">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="0ab3d-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ab3d-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ab3d-143">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ab3d-144">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0ab3d-144">Header files</span></span>

<span data-ttu-id="0ab3d-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ab3d-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ab3d-146">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ab3d-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0ab3d-147">Mapitags.h</span></span>
  
> <span data-ttu-id="0ab3d-148">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0ab3d-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ab3d-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ab3d-149">See also</span></span>



[<span data-ttu-id="0ab3d-150">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ab3d-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ab3d-151">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0ab3d-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ab3d-152">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0ab3d-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ab3d-153">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0ab3d-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

