---
title: PidTagAttachMethod (kanonische Eigenschaft)
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Zuletzt geändert: 07 September 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400726"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="854a3-103">PidTagAttachMethod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="854a3-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="854a3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="854a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="854a3-105">Enthält eine benutzerdefinierte MAPI-Konstante darstellt, die den Inhalt einer Anlage zugegriffen werden können wie.</span><span class="sxs-lookup"><span data-stu-id="854a3-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="854a3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="854a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="854a3-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="854a3-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="854a3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="854a3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="854a3-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="854a3-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="854a3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="854a3-110">Data type:</span></span>  <br/> |<span data-ttu-id="854a3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="854a3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="854a3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="854a3-112">Area:</span></span>  <br/> |<span data-ttu-id="854a3-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="854a3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="854a3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="854a3-114">Remarks</span></span>

<span data-ttu-id="854a3-115">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="854a3-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="854a3-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="854a3-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="854a3-117">Die Anlage wurde soeben erstellt.</span><span class="sxs-lookup"><span data-stu-id="854a3-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="854a3-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="854a3-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="854a3-119">Die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))-Eigenschaft enthält die Anlagendaten.</span><span class="sxs-lookup"><span data-stu-id="854a3-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="854a3-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="854a3-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="854a3-121">Der **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))-Eigenschaft enthält einen vollqualifizierten Pfad, identifiziert die Anlage an Empfänger mit Zugriff auf eine gemeinsame Datei Server.</span><span class="sxs-lookup"><span data-stu-id="854a3-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="854a3-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="854a3-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="854a3-123">Die **PR_ATTACH_PATHNAME** oder **PR_ATTACH_LONG_PATHNAME** -Eigenschaft enthält einen vollqualifizierten Pfad, die das Attachment-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="854a3-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="854a3-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="854a3-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="854a3-125">Die **PR_ATTACH_PATHNAME** oder **PR_ATTACH_LONG_PATHNAME** -Eigenschaft enthält einen vollqualifizierten Pfad, die das Attachment-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="854a3-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="854a3-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="854a3-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="854a3-127">Die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft enthält ein eingebettetes Objekt, das die **IMessage** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="854a3-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="854a3-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="854a3-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="854a3-129">Die Anlage ist ein eingebettetes OLE-Objekt.</span><span class="sxs-lookup"><span data-stu-id="854a3-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="854a3-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="854a3-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="854a3-131">Gescannt ist nicht in der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="854a3-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="854a3-132">Wenn erstellt, haben alle Attachment-Objekte **PR_ATTACH_METHOD** Anfangswert **NO_ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="854a3-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="854a3-133">Clientanwendungen und Dienstanbieter sind nur erforderlich, zur Unterstützung der Anlage-Methode den Wert **ATTACH_BY_VALUE** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="854a3-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="854a3-134">Die anderen Anlage Methoden sind optional.</span><span class="sxs-lookup"><span data-stu-id="854a3-134">The other attachment methods are optional.</span></span> <span data-ttu-id="854a3-135">Nachrichtenspeicher erzwingt Konsistenz zwischen dem Wert der **PR_ATTACH_METHOD** und die Werte der anderen Eigenschaften Anlage nicht.</span><span class="sxs-lookup"><span data-stu-id="854a3-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="854a3-136">Universal naming Convention (UNC) Namen werden für vollqualifizierte Pfade empfohlen, die mit **ATTACH_BY_REFERENCE** und **ATTACH_BY_REF_ONLY**verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="854a3-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="854a3-137">Mit **ATTACH_BY_REF_RESOLVE**ist ein absoluter Pfad schneller, da die MAPI-Warteschlange das Attachment-Objekts **ATTACH_BY_VALUE**konvertiert.</span><span class="sxs-lookup"><span data-stu-id="854a3-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="854a3-138">Wenn **ATTACH_BY_REFERENCE** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein.</span><span class="sxs-lookup"><span data-stu-id="854a3-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="854a3-139">Kopieren der Anlagendaten in die **PR_ATTACH_DATA_BIN** -Eigenschaft kann ein ausgehender Gateway Anlage **ATTACH_BY_REFERENCE** in Anlage **ATTACH_BY_VALUE** deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="854a3-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="854a3-140">Wenn **ATTACH_BY_REF_RESOLVE** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein.</span><span class="sxs-lookup"><span data-stu-id="854a3-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="854a3-141">Wenn die Nachricht mit der **ATTACH_BY_REF_RESOLVE** Anlage gesendet wird, kopiert die MAPI-Warteschlange die Anlagendaten in eine Anlage **ATTACH_BY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="854a3-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="854a3-142">Dieser Prozess Lösung platziert die Anlagedaten in **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="854a3-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="854a3-143">Wenn **ATTACH_BY_REF_ONLY** festgelegt ist, **PR_ATTACH_DATA_BIN** muss leer sein, und Nachrichtensystem wird nie der Anlage Verweis aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="854a3-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="854a3-144">Verwenden Sie diesen Wert, wenn Sie den Link jedoch nicht die Daten senden möchten.</span><span class="sxs-lookup"><span data-stu-id="854a3-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="854a3-145">Wenn das OLE-Objekt im OLE 2.0 **IStorage** Format ist, sind die Daten über **PR_ATTACH_DATA_OBJ**zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="854a3-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="854a3-146">Wenn das OLE-Objekt im OLE 1.0 **OLESTREAM** Format ist, können die Daten als **IStream**über **PR_ATTACH_DATA_BIN** zugreifen.</span><span class="sxs-lookup"><span data-stu-id="854a3-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="854a3-147">Der Typ der Codierung OLE kann durch den Wert **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="854a3-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="854a3-148">Weitere Informationen zu OLE-Schnittstellen und Formate finden Sie unter der *OLE Programmer's Reference* .</span><span class="sxs-lookup"><span data-stu-id="854a3-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="854a3-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="854a3-149">Remarks</span></span>

<span data-ttu-id="854a3-150">Wenn die **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE**ist, ist gescannt nicht in der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="854a3-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="854a3-151">Stattdessen enthält die **PR_ATTACH_LONG_FILENAME** -Eigenschaft eine absolute URL zu gescannt, der online gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="854a3-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="854a3-152">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="854a3-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="854a3-153">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="854a3-153">Protocol specifications</span></span>

<span data-ttu-id="854a3-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="854a3-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="854a3-155">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="854a3-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="854a3-156">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="854a3-156">Header files</span></span>

<span data-ttu-id="854a3-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="854a3-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="854a3-158">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="854a3-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="854a3-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="854a3-159">Mapitags.h</span></span>
  
> <span data-ttu-id="854a3-160">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="854a3-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="854a3-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="854a3-161">See also</span></span>



[<span data-ttu-id="854a3-162">PidTagStoreSupportMask (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="854a3-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="854a3-163">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="854a3-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="854a3-164">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="854a3-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="854a3-165">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="854a3-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="854a3-166">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="854a3-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

