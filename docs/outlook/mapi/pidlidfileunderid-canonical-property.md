---
title: PidLidFileUnderId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355706"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="67485-103">PidLidFileUnderId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="67485-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="67485-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67485-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67485-105">Gibt an, wie der Wert der **eigenschaft dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) generiert und neu kompiliert wird, wenn sich andere Kontaktnameneigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="67485-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67485-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="67485-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67485-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="67485-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="67485-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="67485-108">Property set:</span></span>  <br/> |<span data-ttu-id="67485-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="67485-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="67485-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="67485-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="67485-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="67485-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="67485-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="67485-112">Data type:</span></span>  <br/> |<span data-ttu-id="67485-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="67485-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="67485-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="67485-114">Area:</span></span>  <br/> |<span data-ttu-id="67485-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="67485-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67485-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67485-116">Remarks</span></span>

<span data-ttu-id="67485-117">Wenn diese Eigenschaft fehlt oder auf einen Wert festgelegt ist, der in der folgenden Tabelle oder in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)nicht angegeben ist, kann die Anwendung eine eigene Logik auswählen, um den Wert des **dispidFileUnder** neu zu kompilieren, wenn sich andere Kontaktnameneigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="67485-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="67485-118">In der folgenden Tabelle wird die Notation verwendet, <PropertyName> um "den Wert von PropertyName" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="67485-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="67485-119">Wenn beispielsweise der Wert der **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))-Eigenschaft "Smith" und der Wert der **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))-Eigenschaft "Ben" ist, gibt " " die Zeichenfolge <PidTagGivenName> <PidTagSurname> "Ben Smith" an.</span><span class="sxs-lookup"><span data-stu-id="67485-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="67485-120">In der Tabelle gibt "\r" ein Wagenrücklaufzeichen an, "\n" gibt ein Zeilenvorschubzeichen an und stellt ein Leerzeichen <space> dar.</span><span class="sxs-lookup"><span data-stu-id="67485-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="67485-121">\*\*Wert der \*\*dispidFileUnderId-Eigenschaft\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="67485-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="67485-122">\*\*Beschreibung der \*\*dispidFileUnder-Eigenschaft\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="67485-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67485-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67485-123">0x00000000</span></span>  <br/> |<span data-ttu-id="67485-124">Leere PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="67485-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="67485-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="67485-125">0x00003001</span></span>  <br/> |<span data-ttu-id="67485-126">" \< PidTagDisplayName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="67485-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="67485-128">" \< PidTagGivenName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="67485-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="67485-130">" \< PidTagSurname \> "</span><span class="sxs-lookup"><span data-stu-id="67485-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="67485-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="67485-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="67485-132">" \< PidTagCompanyName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="67485-133">0x00008017</span></span>  <br/> |<span data-ttu-id="67485-134">" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="67485-135">0x00008018</span></span>  <br/> |<span data-ttu-id="67485-136">" \< PidTagCompanyName \>\r\n\< PidTagSurname , space \> \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="67485-137">0x00008019</span></span>  <br/> |<span data-ttu-id="67485-138">" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="67485-139">0x00008030</span></span>  <br/> |<span data-ttu-id="67485-140">" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="67485-141">0x00008031</span></span>  <br/> |<span data-ttu-id="67485-142">" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="67485-143">0x00008032</span></span>  <br/> |<span data-ttu-id="67485-144">" \< PidTagCompanyName \>\r\n\< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="67485-145">0x00008033</span></span>  <br/> |<span data-ttu-id="67485-146">" \< PidTagCompanyName \>\r\n\< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="67485-147">0x00008034</span></span>  <br/> |<span data-ttu-id="67485-148">" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \>\r\n\< PidTagCompanyName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="67485-149">0x00008035</span></span>  <br/> |<span data-ttu-id="67485-150">" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "</span><span class="sxs-lookup"><span data-stu-id="67485-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="67485-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="67485-151">0x00008036</span></span>  <br/> |<span data-ttu-id="67485-152">" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName space \> \< \> \< PidTagGeneration \> "</span><span class="sxs-lookup"><span data-stu-id="67485-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="67485-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="67485-153">0x00008037</span></span>  <br/> |<span data-ttu-id="67485-154">" \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagSurname space \> \< \> \< PidTagGeneration \> "</span><span class="sxs-lookup"><span data-stu-id="67485-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="67485-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="67485-155">0x00008038</span></span>  <br/> |<span data-ttu-id="67485-156">" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagGeneration \> "</span><span class="sxs-lookup"><span data-stu-id="67485-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="67485-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="67485-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="67485-158">Gibt an, dass die Anwendung beim Anzeigen des Kontakts versuchen soll, den aktuellen Wert **von dispidFileUnder** und andere Kontakteigenschaften zu verwenden, um eine "beste Übereinstimmung" für **dispidFileUnderId** mit einem der vorherigen Werte in dieser Tabelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="67485-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="67485-159">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="67485-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="67485-160">Gibt an, dass die Anwendung beim Anzeigen des Kontakts die entsprechenden Standardwerte (gemäß dem Sprach-Locale) für **dispidFileUnderId** auswählen und **dispidFileUnder** aktualisieren soll, um der Auswahl zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="67485-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="67485-161">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="67485-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="67485-162">**dispidFileUnder** ist eine vom Benutzer bereitgestellte PT_UNICODE und sollte nicht geändert werden, wenn sich eine andere Kontaktnameneigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="67485-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="67485-163">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="67485-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67485-164">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="67485-164">Protocol specifications</span></span>

<span data-ttu-id="67485-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67485-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67485-166">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="67485-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67485-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67485-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67485-168">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="67485-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67485-169">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="67485-169">Header files</span></span>

<span data-ttu-id="67485-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67485-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="67485-171">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="67485-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67485-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67485-172">See also</span></span>



[<span data-ttu-id="67485-173">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67485-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67485-174">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="67485-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67485-175">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="67485-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67485-176">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="67485-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

