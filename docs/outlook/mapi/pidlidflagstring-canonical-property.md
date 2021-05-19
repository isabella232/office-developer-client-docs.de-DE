---
title: PidLidFlagString (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357785"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="b5c5e-103">PidLidFlagString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b5c5e-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="b5c5e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5c5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5c5e-105">Enthält einen Index, der eine der vordefinierten Textzeichenfolgen identifiziert, die dem Flag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5c5e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b5c5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5c5e-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="b5c5e-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="b5c5e-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="b5c5e-108">Property set:</span></span>  <br/> |<span data-ttu-id="b5c5e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b5c5e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b5c5e-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b5c5e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b5c5e-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="b5c5e-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="b5c5e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b5c5e-112">Data type:</span></span>  <br/> |<span data-ttu-id="b5c5e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b5c5e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b5c5e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b5c5e-114">Area:</span></span>  <br/> |<span data-ttu-id="b5c5e-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b5c5e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5c5e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5c5e-116">Remarks</span></span>

<span data-ttu-id="b5c5e-117">Wenn diese Eigenschaft festgelegt ist, sollten Clients den entsprechenden Zeichenfolgenwert in den folgenden Tabellen verwenden (beispielsweise, um eine Zeichenfolge zu ersetzen, die in die Sprache des aktuellen Benutzers übersetzt wird), und den in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) und **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) festgelegten Wert ignorieren.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="b5c5e-118">Folgende Standardeinstellungen werden dem Benutzer für Kontaktobjekte vorgeschlagen:</span><span class="sxs-lookup"><span data-stu-id="b5c5e-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="b5c5e-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b5c5e-119">**Value**</span></span>|<span data-ttu-id="b5c5e-120">**Englische Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b5c5e-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5c5e-121">0x00000000 oder nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="b5c5e-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="b5c5e-122">Befolgen Sie die Anweisungen zum Anzeigen von **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="b5c5e-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="b5c5e-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="b5c5e-124">"Follow up"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="b5c5e-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="b5c5e-126">"Anruf"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="b5c5e-127">0x00000070</span></span>  <br/> |<span data-ttu-id="b5c5e-128">"Besprechung anordnen"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="b5c5e-129">0x00000071</span></span>  <br/> |<span data-ttu-id="b5c5e-130">"E-Mail senden"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="b5c5e-131">0x00000072</span></span>  <br/> |<span data-ttu-id="b5c5e-132">"Brief senden"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="b5c5e-133">Für alle anderen Nachrichtenobjekte werden dem Benutzer die folgenden Standardwerte vorgeschlagen:</span><span class="sxs-lookup"><span data-stu-id="b5c5e-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="b5c5e-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b5c5e-134">**Value**</span></span>|<span data-ttu-id="b5c5e-135">**Englische Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b5c5e-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5c5e-136">0x00000000 oder nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="b5c5e-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="b5c5e-137">Befolgen Sie die Anweisungen zum Anzeigen von **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="b5c5e-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b5c5e-138">0x00000001</span></span>  <br/> |<span data-ttu-id="b5c5e-139">"Anruf"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b5c5e-140">0x00000002</span></span>  <br/> |<span data-ttu-id="b5c5e-141">"Nicht weiterleiten"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b5c5e-142">0x00000003</span></span>  <br/> |<span data-ttu-id="b5c5e-143">"Follow up"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b5c5e-144">0x00000004</span></span>  <br/> |<span data-ttu-id="b5c5e-145">"For Your Information"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b5c5e-146">0x00000005</span></span>  <br/> |<span data-ttu-id="b5c5e-147">"Weiterleiten"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="b5c5e-148">0x00000006</span></span>  <br/> |<span data-ttu-id="b5c5e-149">"Keine Antwort erforderlich"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="b5c5e-150">0x00000007</span></span>  <br/> |<span data-ttu-id="b5c5e-151">"Read"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b5c5e-152">0x00000008</span></span>  <br/> |<span data-ttu-id="b5c5e-153">"Antworten"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b5c5e-154">0x00000009</span></span>  <br/> |<span data-ttu-id="b5c5e-155">"Allen antworten"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="b5c5e-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="b5c5e-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="b5c5e-157">"Review"</span><span class="sxs-lookup"><span data-stu-id="b5c5e-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="b5c5e-158">Alle oben angegebenen Zeichenfolgen können gegebenenfalls in die Sprache des Benutzers übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5c5e-159">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b5c5e-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5c5e-160">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b5c5e-160">Protocol specifications</span></span>

<span data-ttu-id="b5c5e-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5c5e-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5c5e-162">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5c5e-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5c5e-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5c5e-164">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5c5e-165">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b5c5e-165">Header files</span></span>

<span data-ttu-id="b5c5e-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5c5e-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5c5e-167">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5c5e-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5c5e-168">See also</span></span>



[<span data-ttu-id="b5c5e-169">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5c5e-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5c5e-170">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b5c5e-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5c5e-171">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b5c5e-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5c5e-172">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b5c5e-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

