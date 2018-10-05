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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401573"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="0dd42-103">PidTagMessageEditorFormat (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0dd42-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="0dd42-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dd42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dd42-105">Gibt das Format für einen-Editor zu verwenden, um eine Nachricht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0dd42-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0dd42-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0dd42-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0dd42-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="0dd42-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="0dd42-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0dd42-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0dd42-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="0dd42-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="0dd42-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0dd42-110">Data type:</span></span>  <br/> |<span data-ttu-id="0dd42-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0dd42-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0dd42-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0dd42-112">Area:</span></span>  <br/> |<span data-ttu-id="0dd42-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="0dd42-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0dd42-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0dd42-114">Remarks</span></span>

<span data-ttu-id="0dd42-115">Die möglichen Werte für **PR_MSG_EDITOR_FORMAT** können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="0dd42-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="0dd42-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0dd42-116">**Value**</span></span>|<span data-ttu-id="0dd42-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0dd42-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0dd42-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="0dd42-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="0dd42-119">Das Format für den Editor an ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="0dd42-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="0dd42-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="0dd42-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="0dd42-121">Im Editor sollten die Nachricht im nur-Text-Format angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0dd42-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="0dd42-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="0dd42-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="0dd42-123">Im Editor sollten die Nachricht im HTML-Format angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0dd42-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="0dd42-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="0dd42-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="0dd42-125">Im Editor sollten die Nachricht im RTF-Format angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0dd42-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="0dd42-126">Standardmäßig Mail-Nachrichten (mit der Nachrichtenklasse IPM **. Hinweis** oder mit einer benutzerdefinierten Nachrichtenklasse IPM **abgeleitet. Beachten Sie**) gesendet von einem POP3/SMTP e-Mail Konto in Transport Neutral Encapsulation Format (TNEF) gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dd42-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="0dd42-127">Die **PR_MSG_EDITOR_FORMAT** -Eigenschaft kann nur nur-Text und nicht-TNEF zu erzwingen, beim Senden einer Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dd42-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="0dd42-128">Wenn **bei** **PR_MSG_EDITOR_FORMAT** festgelegt ist, wird die Nachricht als nur-Text ohne TNEF gesendet.</span><span class="sxs-lookup"><span data-stu-id="0dd42-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="0dd42-129">Wenn **PR_MSG_EDITOR_FORMAT** auf **EDITOR_FORMAT_RTF**festgelegt ist, TNEF-Codierung ist implizit aktiviert, und die Nachricht wird gesendet, mit der Internet-Standardformat, das im Outlook-Client angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0dd42-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="0dd42-130">Es gibt zwei andere Methoden, um die Verwendung von TNEF erzwingen beim Senden einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0dd42-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="0dd42-131">Festlegen der **DispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) mit dem Namen-Eigenschaft auf True für eine Nachricht gibt an, dass beim Konvertieren der Nachricht von MAPI in MIME/SMTP TNEF eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0dd42-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="0dd42-132">Hinweis: Diese **DispidUseTNEF** gilt nur, wenn die Nachricht wird aus einem POP3/SMTP-Mail-Konto gesendet, und wird nicht angewendet, wenn die Nachricht von anderen Anbietern wie beispielsweise Microsoft Exchange Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0dd42-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="0dd42-133">**DispidUseTNEF** überschreibt die Einstellung in **PR_MSG_EDITOR_FORMAT**.</span><span class="sxs-lookup"><span data-stu-id="0dd42-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="0dd42-134">Verwenden die Kennzeichen **CCSF_USE_TNEF** beim Aufruf von [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) zum ausgehenden MAPI-Nachrichten in einen MIME-Stream konvertieren kann auch TNEF erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0dd42-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="0dd42-135">Dies gilt, auch wenn **DispidUseTNEF** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0dd42-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="0dd42-136">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0dd42-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0dd42-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0dd42-137">Protocol specifications</span></span>

<span data-ttu-id="0dd42-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dd42-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dd42-139">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0dd42-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0dd42-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dd42-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dd42-141">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="0dd42-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="0dd42-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dd42-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dd42-143">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0dd42-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0dd42-144">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0dd42-144">Header files</span></span>

<span data-ttu-id="0dd42-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0dd42-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="0dd42-146">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0dd42-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="0dd42-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0dd42-147">Mapitags.h</span></span>
  
> <span data-ttu-id="0dd42-148">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0dd42-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0dd42-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dd42-149">See also</span></span>



[<span data-ttu-id="0dd42-150">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0dd42-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0dd42-151">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0dd42-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0dd42-152">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0dd42-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0dd42-153">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0dd42-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

