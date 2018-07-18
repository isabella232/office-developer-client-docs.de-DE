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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 08e2403be35b87393d22f9109f59c0572c53073b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793613"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="f3e2f-103">PidLidFileUnderId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f3e2f-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="f3e2f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3e2f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3e2f-105">Gibt an, wie generieren und den Wert der Eigenschaft **DispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) neu berechnen, wenn andere Kontakt benennen Eigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3e2f-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f3e2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3e2f-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="f3e2f-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="f3e2f-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="f3e2f-108">Property set:</span></span>  <br/> |<span data-ttu-id="f3e2f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="f3e2f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="f3e2f-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="f3e2f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f3e2f-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="f3e2f-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="f3e2f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f3e2f-112">Data type:</span></span>  <br/> |<span data-ttu-id="f3e2f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f3e2f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f3e2f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f3e2f-114">Area:</span></span>  <br/> |<span data-ttu-id="f3e2f-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="f3e2f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3e2f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3e2f-116">Remarks</span></span>

<span data-ttu-id="f3e2f-117">Wenn diese Eigenschaft nicht vorhanden ist oder auf einen anderen Wert nicht um einen detaillierten in der folgenden Tabelle oder in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)festlegen, können die Anwendung seine eigene Logik für den Wert der **DispidFileUnder** als andere Kontaktnamen Eigenschaften Änderung neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="f3e2f-118">In der folgenden Tabelle, die Notation <PropertyName> wird verwendet, um "den Wert von PropertyName" angeben.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="f3e2f-119">Wenn der Wert der Eigenschaft **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) ist "Smith", und der Wert der Eigenschaft **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) "Peter", dann beträgt beispielsweise "<PidTagGivenName> <PidTagSurname>" gibt die Zeichenfolge "Ben Smith".</span><span class="sxs-lookup"><span data-stu-id="f3e2f-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="f3e2f-120">In der Tabelle "\r" gibt ein Wagenrücklaufzeichen, "\n" gibt ein Zeichen Zeilenvorschub und <space> ein Leerzeichen dar.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="f3e2f-121">**Der Wert der **DispidFileUnderId** -Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f3e2f-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="f3e2f-122">**Beschreibung der **DispidFileUnder** -Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f3e2f-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3e2f-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3e2f-123">0x00000000</span></span>  <br/> |<span data-ttu-id="f3e2f-124">Leere PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="f3e2f-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="f3e2f-125">0x00003001</span></span>  <br/> |<span data-ttu-id="f3e2f-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="f3e2f-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="f3e2f-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="f3e2f-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="f3e2f-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="f3e2f-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="f3e2f-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="f3e2f-133">0x00008017</span></span>  <br/> |<span data-ttu-id="f3e2f-134">"\<PidTagSurname\>,\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="f3e2f-135">0x00008018</span></span>  <br/> |<span data-ttu-id="f3e2f-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="f3e2f-137">0x00008019</span></span>  <br/> |<span data-ttu-id="f3e2f-138">"\<PidTagSurname\>,\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="f3e2f-139">0x00008030</span></span>  <br/> |<span data-ttu-id="f3e2f-140">"\<PidTagSurname\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="f3e2f-141">0x00008031</span></span>  <br/> |<span data-ttu-id="f3e2f-142">"\<PidTagSurname\>\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="f3e2f-143">0x00008032</span></span>  <br/> |<span data-ttu-id="f3e2f-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="f3e2f-145">0x00008033</span></span>  <br/> |<span data-ttu-id="f3e2f-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="f3e2f-147">0x00008034</span></span>  <br/> |<span data-ttu-id="f3e2f-148">"\<PidTagSurname\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="f3e2f-149">0x00008035</span></span>  <br/> |<span data-ttu-id="f3e2f-150">"\<PidTagSurname\>\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="f3e2f-151">0x00008036</span></span>  <br/> |<span data-ttu-id="f3e2f-152">"\<PidTagSurname\>\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\<Speicherplatz\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="f3e2f-153">0x00008037</span></span>  <br/> |<span data-ttu-id="f3e2f-154">"\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\<Speicherplatz\>\<PidTagSurname\>\<Speicherplatz\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="f3e2f-155">0x00008038</span></span>  <br/> |<span data-ttu-id="f3e2f-156">"\<PidTagSurname\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\<Speicherplatz\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="f3e2f-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="f3e2f-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="f3e2f-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="f3e2f-158">Gibt an, dass, wenn den Kontakt angezeigt werden, die Anwendung sollte den aktuellen Wert der **DispidFileUnder** und andere Kontakten Eigenschaften verwenden, um "beste Übereinstimmung" für **DispidFileUnderId** auf einen der vorherigen Werte in dieser Tabelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="f3e2f-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="f3e2f-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="f3e2f-160">Gibt an, dass beim Anzeigen des Kontakts die Anwendung wählen Sie die entsprechenden Standardwerte (gemäß dem Gebietsschema) für **DispidFileUnderId** und **DispidFileUnder** die Wahl entsprechend aktualisieren sollten.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="f3e2f-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="f3e2f-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="f3e2f-162">**DispidFileUnder** ist eine vom Benutzer bereitgestellte PT_UNICODE und sollte nicht geändert werden, wenn eine andere Kontaktnamen-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f3e2f-163">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f3e2f-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3e2f-164">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f3e2f-164">Protocol specifications</span></span>

<span data-ttu-id="f3e2f-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3e2f-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3e2f-166">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3e2f-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3e2f-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3e2f-168">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3e2f-169">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f3e2f-169">Header files</span></span>

<span data-ttu-id="f3e2f-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3e2f-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3e2f-171">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3e2f-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3e2f-172">See also</span></span>



[<span data-ttu-id="f3e2f-173">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3e2f-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3e2f-174">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3e2f-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3e2f-175">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f3e2f-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3e2f-176">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f3e2f-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

