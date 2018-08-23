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
ms.openlocfilehash: 70b0508d9a19df42e4ab164aba58aaef44b0c01a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565487"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="e7f53-103">PidTagDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7f53-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="e7f53-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7f53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7f53-105">Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e7f53-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7f53-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e7f53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7f53-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e7f53-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e7f53-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e7f53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7f53-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="e7f53-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="e7f53-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e7f53-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7f53-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e7f53-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e7f53-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e7f53-112">Area:</span></span>  <br/> |<span data-ttu-id="e7f53-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="e7f53-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7f53-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e7f53-114">Remarks</span></span>

<span data-ttu-id="e7f53-115">Ordner erfordern gleichgeordneten Knoten Unterordner eindeutigen Anzeigenamen haben.</span><span class="sxs-lookup"><span data-stu-id="e7f53-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="e7f53-116">Beispielsweise wenn ein Ordner zwei Unterordner enthält, können nicht zwei Unterordner den gleichen Wert für diese Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7f53-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="e7f53-117">Diese Beschränkung gilt nicht für andere Container, z. B. Adressbücher und Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="e7f53-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="e7f53-118">Dienstanbieter sollte den Wert dieser Eigenschaft festgelegt, sodass sie die Anbieter Typ und die Konfiguration der Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e7f53-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="e7f53-119">Weitere Informationen hilft zum unterscheiden zwischen Instanzen von Anbietern des gleichen Typs.</span><span class="sxs-lookup"><span data-stu-id="e7f53-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="e7f53-120">Nicht konfigurierte Anbieter sollte eine Zeichenfolge verwenden, die den Namen des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="e7f53-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="e7f53-121">Konfigurierte Anbieter sollten Sie dieselbe Zeichenfolge gefolgt von einer charakteristische Zeichenfolge in Klammern verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7f53-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="e7f53-122">Beispielsweise kann ein Anbieter nicht konfigurierte Nachricht diese Eigenschaften auf festgelegt:</span><span class="sxs-lookup"><span data-stu-id="e7f53-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="e7f53-123">Persönlicher Informationsspeicher</span><span class="sxs-lookup"><span data-stu-id="e7f53-123">Personal Information Store</span></span>
  
<span data-ttu-id="e7f53-124">Die konfigurierte Version kann anschließend diese Eigenschaften festgelegt werden auf:</span><span class="sxs-lookup"><span data-stu-id="e7f53-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="e7f53-125">Persönlicher Informationsspeicher (6 Februar 1998)</span><span class="sxs-lookup"><span data-stu-id="e7f53-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="e7f53-126">Für Status-Objekte enthalten diese Eigenschaften den Namen der Komponente, die von der Benutzeroberfläche angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e7f53-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e7f53-127">Semikolons können nicht innerhalb von Empfängernamen in MAPI messaging verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7f53-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e7f53-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7f53-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7f53-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e7f53-129">Protocol specifications</span></span>

<span data-ttu-id="e7f53-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f53-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f53-131">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e7f53-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7f53-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f53-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f53-133">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="e7f53-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e7f53-134">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f53-134">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f53-135">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="e7f53-135">Handles folder operations.</span></span>
    
<span data-ttu-id="e7f53-136">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f53-136">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f53-137">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e7f53-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="e7f53-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f53-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f53-139">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e7f53-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="e7f53-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f53-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f53-141">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="e7f53-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="e7f53-142">[[MS-XWDVSEC]](http://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f53-142">[[MS-XWDVSEC]](http://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f53-143">Erweitert das Protokoll WebDAV, das angibt, wie angefordert, und legen Sie die Exchange-Sicherheits-ID über WebDAV-Methoden.</span><span class="sxs-lookup"><span data-stu-id="e7f53-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7f53-144">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e7f53-144">Header files</span></span>

<span data-ttu-id="e7f53-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7f53-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7f53-146">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e7f53-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7f53-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7f53-147">Mapitags.h</span></span>
  
> <span data-ttu-id="e7f53-148">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e7f53-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7f53-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7f53-149">See also</span></span>



[<span data-ttu-id="e7f53-150">PidTagTransmittableDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7f53-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="e7f53-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7f53-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7f53-152">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7f53-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7f53-153">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e7f53-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7f53-154">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e7f53-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

