---
title: PidTagDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360802"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="e690c-103">PidTagDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e690c-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="e690c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e690c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e690c-105">Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e690c-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e690c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e690c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e690c-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e690c-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e690c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e690c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e690c-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="e690c-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="e690c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e690c-110">Data type:</span></span>  <br/> |<span data-ttu-id="e690c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e690c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e690c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e690c-112">Area:</span></span>  <br/> |<span data-ttu-id="e690c-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="e690c-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e690c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e690c-114">Remarks</span></span>

<span data-ttu-id="e690c-115">Ordner erfordern gleichgeordnete Unterordner, um eindeutige Anzeigenamen zu haben.</span><span class="sxs-lookup"><span data-stu-id="e690c-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="e690c-116">Wenn ein Ordner beispielsweise zwei Unterordner enthält, können die beiden Unterordner nicht denselben Wert für diese Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="e690c-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="e690c-117">Diese Einschränkung gilt nicht für andere Container, z. B. Adressbücher und Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="e690c-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="e690c-118">Dienstanbieter sollten den Wert dieser Eigenschaft so festlegen, dass sie sowohl den Anbietertyp als auch Konfigurationsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e690c-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="e690c-119">Die zusätzlichen Informationen helfen, zwischen Instanzen von Anbietern desselben Typs zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e690c-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="e690c-120">Nicht konfigurierte Anbieter sollten eine Zeichenfolge verwenden, die den Anbieter benennt.</span><span class="sxs-lookup"><span data-stu-id="e690c-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="e690c-121">Konfigurierte Anbieter sollten dieselbe Zeichenfolge gefolgt von einer unterscheidenden Zeichenfolge in Klammern verwenden.</span><span class="sxs-lookup"><span data-stu-id="e690c-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="e690c-122">Ein nicht konfigurierter Nachrichtenspeicheranbieter kann beispielsweise folgende Eigenschaften festlegen:</span><span class="sxs-lookup"><span data-stu-id="e690c-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="e690c-123">Personenbezogene Store</span><span class="sxs-lookup"><span data-stu-id="e690c-123">Personal Information Store</span></span>
  
<span data-ttu-id="e690c-124">Die konfigurierte Version kann dann die folgenden Eigenschaften festlegen:</span><span class="sxs-lookup"><span data-stu-id="e690c-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="e690c-125">Personal Information Store (6. Februar 1998)</span><span class="sxs-lookup"><span data-stu-id="e690c-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="e690c-126">Für Statusobjekte enthalten diese Eigenschaften den Namen der Komponente, die von der Benutzeroberfläche angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e690c-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e690c-127">Semikolons können nicht innerhalb von Empfängernamen in MAPI-Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e690c-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e690c-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e690c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e690c-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e690c-129">Protocol specifications</span></span>

<span data-ttu-id="e690c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e690c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e690c-131">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e690c-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e690c-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e690c-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e690c-133">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="e690c-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e690c-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e690c-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e690c-135">Verarbeitet Ordnervorgänge.</span><span class="sxs-lookup"><span data-stu-id="e690c-135">Handles folder operations.</span></span>
    
<span data-ttu-id="e690c-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e690c-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e690c-137">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e690c-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="e690c-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e690c-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e690c-139">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="e690c-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="e690c-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e690c-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e690c-141">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="e690c-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="e690c-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e690c-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e690c-143">Erweitert das WebDAV-Protokoll, das angibt, wie der Sicherheitsdeskriptor Exchange WebDAV-Methoden an- und festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e690c-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e690c-144">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e690c-144">Header files</span></span>

<span data-ttu-id="e690c-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e690c-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="e690c-146">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e690c-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="e690c-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e690c-147">Mapitags.h</span></span>
  
> <span data-ttu-id="e690c-148">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e690c-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e690c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e690c-149">See also</span></span>



[<span data-ttu-id="e690c-150">PidTagTransmittableDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e690c-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="e690c-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e690c-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e690c-152">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e690c-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e690c-153">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e690c-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e690c-154">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e690c-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

