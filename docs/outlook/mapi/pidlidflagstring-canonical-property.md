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
ms.openlocfilehash: b29fdbb82635ca7706be15ee9f674262d2204ad5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576183"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="486e4-103">PidLidFlagString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="486e4-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="486e4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="486e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="486e4-105">Enthält einen Index, der eine Reihe von vordefinierten Textzeichenfolgen, die das Flag zugeordnet identifiziert.</span><span class="sxs-lookup"><span data-stu-id="486e4-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="486e4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="486e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="486e4-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="486e4-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="486e4-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="486e4-108">Property set:</span></span>  <br/> |<span data-ttu-id="486e4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="486e4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="486e4-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="486e4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="486e4-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="486e4-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="486e4-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="486e4-112">Data type:</span></span>  <br/> |<span data-ttu-id="486e4-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="486e4-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="486e4-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="486e4-114">Area:</span></span>  <br/> |<span data-ttu-id="486e4-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="486e4-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="486e4-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="486e4-116">Remarks</span></span>

<span data-ttu-id="486e4-117">Wenn diese Eigenschaft festgelegt ist, sollten Clients den entsprechenden String-Wert in den Tabellen unten (beispielsweise um eine Zeichenfolge zu ersetzen, die in der aktuellen Sprache des Benutzers übersetzt wird), und den Wert im **DispidFlagRequest** ([ ignorieren soll PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) und **DispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="486e4-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="486e4-118">Standardeinstellungen für den Benutzer für Kontaktobjekte vorgeschlagene lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="486e4-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="486e4-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="486e4-119">**Value**</span></span>|<span data-ttu-id="486e4-120">**Englische Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="486e4-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="486e4-121">0 x 00000000 oder nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="486e4-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="486e4-122">Führen Sie die Anweisungen im Zusammenhang mit **DispidFlagRequest**anzeigen.</span><span class="sxs-lookup"><span data-stu-id="486e4-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="486e4-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="486e4-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="486e4-124">"Nachverfolgung"</span><span class="sxs-lookup"><span data-stu-id="486e4-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="486e4-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="486e4-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="486e4-126">"Anrufen"</span><span class="sxs-lookup"><span data-stu-id="486e4-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="486e4-127">0 x 00000070</span><span class="sxs-lookup"><span data-stu-id="486e4-127">0x00000070</span></span>  <br/> |<span data-ttu-id="486e4-128">"Meeting anordnen"</span><span class="sxs-lookup"><span data-stu-id="486e4-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="486e4-129">0 x 00000071</span><span class="sxs-lookup"><span data-stu-id="486e4-129">0x00000071</span></span>  <br/> |<span data-ttu-id="486e4-130">"Senden Sie E-Mail"</span><span class="sxs-lookup"><span data-stu-id="486e4-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="486e4-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="486e4-131">0x00000072</span></span>  <br/> |<span data-ttu-id="486e4-132">"Senden Sie Brief"</span><span class="sxs-lookup"><span data-stu-id="486e4-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="486e4-133">Standardeinstellungen für den Benutzer für alle anderen Nachrichtenobjekte vorgeschlagenen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="486e4-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="486e4-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="486e4-134">**Value**</span></span>|<span data-ttu-id="486e4-135">**Englische Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="486e4-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="486e4-136">0 x 00000000 oder nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="486e4-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="486e4-137">Führen Sie die Anweisungen im Zusammenhang mit **DispidFlagRequest**anzeigen.</span><span class="sxs-lookup"><span data-stu-id="486e4-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="486e4-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="486e4-138">0x00000001</span></span>  <br/> |<span data-ttu-id="486e4-139">"Anrufen"</span><span class="sxs-lookup"><span data-stu-id="486e4-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="486e4-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="486e4-140">0x00000002</span></span>  <br/> |<span data-ttu-id="486e4-141">"Nicht weiterleiten"</span><span class="sxs-lookup"><span data-stu-id="486e4-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="486e4-142">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="486e4-142">0x00000003</span></span>  <br/> |<span data-ttu-id="486e4-143">"Nachverfolgung"</span><span class="sxs-lookup"><span data-stu-id="486e4-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="486e4-144">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="486e4-144">0x00000004</span></span>  <br/> |<span data-ttu-id="486e4-145">"Zu Ihrer Information"</span><span class="sxs-lookup"><span data-stu-id="486e4-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="486e4-146">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="486e4-146">0x00000005</span></span>  <br/> |<span data-ttu-id="486e4-147">"Weiterleiten"</span><span class="sxs-lookup"><span data-stu-id="486e4-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="486e4-148">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="486e4-148">0x00000006</span></span>  <br/> |<span data-ttu-id="486e4-149">"Antwort nicht erforderlich"</span><span class="sxs-lookup"><span data-stu-id="486e4-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="486e4-150">0 x 00000007</span><span class="sxs-lookup"><span data-stu-id="486e4-150">0x00000007</span></span>  <br/> |<span data-ttu-id="486e4-151">"Read"</span><span class="sxs-lookup"><span data-stu-id="486e4-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="486e4-152">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="486e4-152">0x00000008</span></span>  <br/> |<span data-ttu-id="486e4-153">"Antwort"</span><span class="sxs-lookup"><span data-stu-id="486e4-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="486e4-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="486e4-154">0x00000009</span></span>  <br/> |<span data-ttu-id="486e4-155">"Allen Antworten"</span><span class="sxs-lookup"><span data-stu-id="486e4-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="486e4-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="486e4-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="486e4-157">"Prüfung"</span><span class="sxs-lookup"><span data-stu-id="486e4-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="486e4-158">Alle oben angegebene Zeichenfolgen können in der Sprache des Benutzers, falls zutreffend übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="486e4-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="486e4-159">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="486e4-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="486e4-160">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="486e4-160">Protocol specifications</span></span>

<span data-ttu-id="486e4-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="486e4-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="486e4-162">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="486e4-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="486e4-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="486e4-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="486e4-164">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="486e4-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="486e4-165">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="486e4-165">Header files</span></span>

<span data-ttu-id="486e4-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="486e4-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="486e4-167">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="486e4-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="486e4-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="486e4-168">See also</span></span>



[<span data-ttu-id="486e4-169">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="486e4-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="486e4-170">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="486e4-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="486e4-171">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="486e4-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="486e4-172">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="486e4-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

