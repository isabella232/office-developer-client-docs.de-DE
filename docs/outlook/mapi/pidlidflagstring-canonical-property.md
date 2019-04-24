---
title: Kanonische Pidlidflagstring (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357785"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="e1ac2-103">Kanonische Pidlidflagstring (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e1ac2-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="e1ac2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1ac2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1ac2-105">Enthält einen Index, der eine Reihe vordefinierter Textzeichenfolgen identifiziert, die mit dem Flag verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1ac2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e1ac2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1ac2-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="e1ac2-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="e1ac2-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="e1ac2-108">Property set:</span></span>  <br/> |<span data-ttu-id="e1ac2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e1ac2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e1ac2-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="e1ac2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e1ac2-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="e1ac2-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="e1ac2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e1ac2-112">Data type:</span></span>  <br/> |<span data-ttu-id="e1ac2-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1ac2-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1ac2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e1ac2-114">Area:</span></span>  <br/> |<span data-ttu-id="e1ac2-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e1ac2-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1ac2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1ac2-116">Remarks</span></span>

<span data-ttu-id="e1ac2-117">Wenn diese Eigenschaft festgelegt ist, sollten Clients den entsprechenden Zeichenfolgenwert in den folgenden Tabellen verwenden (beispielsweise, um eine Zeichenfolge zu ersetzen, die in die Sprache des aktuellen Benutzers übersetzt wird), und den in **dispidFlagRequest** festgelegten Wert ignorieren sollte ([ Pidlidflagrequest (](pidlidflagrequest-canonical-property.md)) und **dispidValidFlagStringProof** ([pidlidvalidflagstringproof (](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1ac2-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="e1ac2-118">Folgende Standardwerte werden dem Benutzer für Kontaktobjekte vorgeschlagen:</span><span class="sxs-lookup"><span data-stu-id="e1ac2-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="e1ac2-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-119">**Value**</span></span>|<span data-ttu-id="e1ac2-120">**Englische Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1ac2-121">0x00000000 oder nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="e1ac2-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="e1ac2-122">BeFolgen Sie die Anweisungen im Zusammenhang mit der Anzeige von **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="e1ac2-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="e1ac2-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="e1ac2-124">"NachVerfolgen"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="e1ac2-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="e1ac2-126">Rufen</span><span class="sxs-lookup"><span data-stu-id="e1ac2-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="e1ac2-127">0x00000070</span></span>  <br/> |<span data-ttu-id="e1ac2-128">"Besprechung anOrdnen"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="e1ac2-129">0x00000071</span></span>  <br/> |<span data-ttu-id="e1ac2-130">"E-Mail senden"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="e1ac2-131">0x00000072</span></span>  <br/> |<span data-ttu-id="e1ac2-132">"Brief senden"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="e1ac2-133">Dem Benutzer vorgeschlagene Standardwerte für alle anderen Nachrichtenobjekte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e1ac2-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="e1ac2-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-134">**Value**</span></span>|<span data-ttu-id="e1ac2-135">**Englische Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1ac2-136">0x00000000 oder nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="e1ac2-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="e1ac2-137">BeFolgen Sie die Anweisungen im Zusammenhang mit der Anzeige von **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="e1ac2-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e1ac2-138">0x00000001</span></span>  <br/> |<span data-ttu-id="e1ac2-139">Rufen</span><span class="sxs-lookup"><span data-stu-id="e1ac2-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e1ac2-140">0x00000002</span></span>  <br/> |<span data-ttu-id="e1ac2-141">"Nicht weiterleiten"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e1ac2-142">0x00000003</span></span>  <br/> |<span data-ttu-id="e1ac2-143">"NachVerfolgen"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e1ac2-144">0x00000004</span></span>  <br/> |<span data-ttu-id="e1ac2-145">"Zu Ihren Informationen"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e1ac2-146">0x00000005</span></span>  <br/> |<span data-ttu-id="e1ac2-147">"Weiterleiten"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="e1ac2-148">0x00000006</span></span>  <br/> |<span data-ttu-id="e1ac2-149">"Keine Antwort erforderlich"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="e1ac2-150">0x00000007</span></span>  <br/> |<span data-ttu-id="e1ac2-151">Lesen</span><span class="sxs-lookup"><span data-stu-id="e1ac2-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e1ac2-152">0x00000008</span></span>  <br/> |<span data-ttu-id="e1ac2-153">"Antworten"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e1ac2-154">0x00000009</span></span>  <br/> |<span data-ttu-id="e1ac2-155">"Allen Antworten"</span><span class="sxs-lookup"><span data-stu-id="e1ac2-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="e1ac2-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="e1ac2-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="e1ac2-157">Bewertung</span><span class="sxs-lookup"><span data-stu-id="e1ac2-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="e1ac2-158">Alle oben angegebenen Zeichenfolgen können ggf. in die Sprache des Benutzers übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1ac2-159">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e1ac2-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1ac2-160">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e1ac2-160">Protocol specifications</span></span>

<span data-ttu-id="e1ac2-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1ac2-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1ac2-162">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1ac2-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1ac2-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1ac2-164">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1ac2-165">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e1ac2-165">Header files</span></span>

<span data-ttu-id="e1ac2-166">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e1ac2-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1ac2-167">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1ac2-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1ac2-168">See also</span></span>



[<span data-ttu-id="e1ac2-169">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1ac2-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1ac2-170">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1ac2-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1ac2-171">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e1ac2-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1ac2-172">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e1ac2-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

