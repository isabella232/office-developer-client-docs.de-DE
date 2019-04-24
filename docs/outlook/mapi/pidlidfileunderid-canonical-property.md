---
title: Kanonische Pidlidfileunderid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355706"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="70cca-103">Kanonische Pidlidfileunderid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="70cca-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="70cca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70cca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70cca-105">Gibt an, wie der Wert der **dispidFileUnder** ([pidlidfileunder (](pidlidfileunder-canonical-property.md))-Eigenschaft generiert und neu berechnet wird, wenn sich die Eigenschaften anderer Kontaktnamen ändern.</span><span class="sxs-lookup"><span data-stu-id="70cca-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70cca-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="70cca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70cca-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="70cca-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="70cca-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="70cca-108">Property set:</span></span>  <br/> |<span data-ttu-id="70cca-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="70cca-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="70cca-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="70cca-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="70cca-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="70cca-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="70cca-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="70cca-112">Data type:</span></span>  <br/> |<span data-ttu-id="70cca-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="70cca-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="70cca-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="70cca-114">Area:</span></span>  <br/> |<span data-ttu-id="70cca-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="70cca-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70cca-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70cca-116">Remarks</span></span>

<span data-ttu-id="70cca-117">Wenn diese Eigenschaft fehlt oder auf einen Wert festgelegt ist, der nicht in der Tabelle unten oder in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)detailliert ist, kann die Anwendung ihre eigene Logik auswählen, um den Wert der **dispidFileUnder** neu zu berechnen, wenn sich die Eigenschaften anderer Kontaktnamen ändern.</span><span class="sxs-lookup"><span data-stu-id="70cca-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="70cca-118">In der folgenden Tabelle wird die Notation <PropertyName> verwendet, um "den Wert von PropertyName" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="70cca-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="70cca-119">Wenn beispielsweise der Wert der **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))-Eigenschaft "Smith" lautet und der Wert der **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))-Eigenschaft "Ben" lautet, gibt "<PidTagGivenName> <PidTagSurname>" die Zeichenfolge "Ben Smith" an.</span><span class="sxs-lookup"><span data-stu-id="70cca-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="70cca-120">In der Tabelle gibt "\r" ein Wagenrücklaufzeichen an, "\n" gibt ein Zeilenvorschubzeichen an und <space> stellt ein Leerzeichen dar.</span><span class="sxs-lookup"><span data-stu-id="70cca-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="70cca-121">**Wert der **dispidFileUnderId** -Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="70cca-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="70cca-122">**Beschreibung der **dispidFileUnder** -Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="70cca-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70cca-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70cca-123">0x00000000</span></span>  <br/> |<span data-ttu-id="70cca-124">Leere PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="70cca-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="70cca-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="70cca-125">0x00003001</span></span>  <br/> |<span data-ttu-id="70cca-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="70cca-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="70cca-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="70cca-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="70cca-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="70cca-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="70cca-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="70cca-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="70cca-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="70cca-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="70cca-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="70cca-133">0x00008017</span></span>  <br/> |<span data-ttu-id="70cca-134">"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="70cca-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="70cca-135">0x00008018</span></span>  <br/> |<span data-ttu-id="70cca-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="70cca-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="70cca-137">0x00008019</span></span>  <br/> |<span data-ttu-id="70cca-138">"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\>Space pidtagmiddlename (\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="70cca-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="70cca-139">0x00008030</span></span>  <br/> |<span data-ttu-id="70cca-140">"\<PidTagSurname\>\<\>PidTagGivenName\<Space\>pidtagmiddlename (\>"\<</span><span class="sxs-lookup"><span data-stu-id="70cca-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="70cca-141">0x00008031</span></span>  <br/> |<span data-ttu-id="70cca-142">"\<PidTagSurname\>\<Space\>\<PidTagGivenName Space\>pidtagmiddlename (\>"\<\>\<</span><span class="sxs-lookup"><span data-stu-id="70cca-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="70cca-143">0x00008032</span></span>  <br/> |<span data-ttu-id="70cca-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<Space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="70cca-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="70cca-145">0x00008033</span></span>  <br/> |<span data-ttu-id="70cca-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<Space\>\<PidTagGivenName Space\>pidtagmiddlename (\>"\<\>\<</span><span class="sxs-lookup"><span data-stu-id="70cca-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="70cca-147">0x00008034</span></span>  <br/> |<span data-ttu-id="70cca-148">"\<PidTagSurname\>\<PidTagGivenName\>\>Space pidtagmiddlename (\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="70cca-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="70cca-149">0x00008035</span></span>  <br/> |<span data-ttu-id="70cca-150">"\<PidTagSurname\>\<Space\>\<\>PidTagGivenName Space\>pidtagmiddlename (\r\n PidTagCompanyName"\<\>\<\>\<</span><span class="sxs-lookup"><span data-stu-id="70cca-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="70cca-151">0x00008036</span></span>  <br/> |<span data-ttu-id="70cca-152">"\<PidTagSurname\>\<Space\>\<\<PidTagGivenName\>Space pidtagmiddlename (\>Space\>pidtaggeneration (\>"\<\>\<\<</span><span class="sxs-lookup"><span data-stu-id="70cca-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="70cca-153">0x00008037</span></span>  <br/> |<span data-ttu-id="70cca-154">"\<PidTagGivenName\>\<Space\>\<\<pidtagmiddlename (\>Space PidTagSurname\>Space\>pidtaggeneration (\>"\<\>\<\<</span><span class="sxs-lookup"><span data-stu-id="70cca-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="70cca-155">0x00008038</span></span>  <br/> |<span data-ttu-id="70cca-156">"\<PidTagSurname\>\<PidTagGivenName\>\>Space\>pidtagmiddlename (\>Space\>pidtaggeneration ("\<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="70cca-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="70cca-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="70cca-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="70cca-158">Gibt an, dass die Anwendung beim Anzeigen des Kontakts versuchen sollte, den aktuellen Wert von **dispidFileUnder** und andere Kontakteigenschaften zu verwenden, um eine "beste Übereinstimmung" für **dispidFileUnderId** zu einem der vorherigen Werte in dieser Tabelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="70cca-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="70cca-159">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="70cca-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="70cca-160">Gibt an, dass die Anwendung beim Anzeigen des Kontakts die entsprechenden Standardwerte (entsprechend dem Gebietsschema der Sprache) für **dispidFileUnderId** und **dispidFileUnder** aktualisieren soll, um die Auswahl zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="70cca-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="70cca-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="70cca-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="70cca-162">**dispidFileUnder** ist ein vom Benutzer bereitgestellter PT_UNICODE und sollte nicht geändert werden, wenn sich eine andere Kontaktnamens Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="70cca-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="70cca-163">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="70cca-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70cca-164">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="70cca-164">Protocol specifications</span></span>

<span data-ttu-id="70cca-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70cca-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70cca-166">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="70cca-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70cca-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70cca-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70cca-168">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="70cca-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70cca-169">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="70cca-169">Header files</span></span>

<span data-ttu-id="70cca-170">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="70cca-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="70cca-171">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="70cca-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70cca-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70cca-172">See also</span></span>



[<span data-ttu-id="70cca-173">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="70cca-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70cca-174">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="70cca-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70cca-175">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="70cca-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70cca-176">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="70cca-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

