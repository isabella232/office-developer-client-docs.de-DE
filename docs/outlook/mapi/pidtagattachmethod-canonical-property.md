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
description: 'Letzte Änderung: 07. September 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327258"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="73644-103">PidTagAttachMethod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="73644-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="73644-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73644-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73644-105">Enthält eine MAPI-definierte Konstante, die den Zugriff auf den Inhalt einer Anlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="73644-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73644-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="73644-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73644-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="73644-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="73644-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="73644-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73644-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="73644-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="73644-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="73644-110">Data type:</span></span>  <br/> |<span data-ttu-id="73644-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="73644-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="73644-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="73644-112">Area:</span></span>  <br/> |<span data-ttu-id="73644-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="73644-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73644-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="73644-114">Remarks</span></span>

<span data-ttu-id="73644-115">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="73644-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="73644-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="73644-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="73644-117">Die Anlage wurde gerade erstellt.</span><span class="sxs-lookup"><span data-stu-id="73644-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="73644-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="73644-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="73644-119">Die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) -Eigenschaft enthält die Anlagendaten.</span><span class="sxs-lookup"><span data-stu-id="73644-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="73644-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="73644-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="73644-121">Die **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) -Eigenschaft enthält einen vollqualifizierten Pfad, der die Anlage für Empfänger mit Zugriff auf einen gemeinsamen Dateiserver identifiziert.</span><span class="sxs-lookup"><span data-stu-id="73644-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="73644-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="73644-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="73644-123">Die **PR_ATTACH_PATHNAME-** **oder PR_ATTACH_LONG_PATHNAME-Eigenschaft** enthält einen vollqualifizierten Pfad, der die Anlage identifiziert.</span><span class="sxs-lookup"><span data-stu-id="73644-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="73644-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="73644-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="73644-125">Die **PR_ATTACH_PATHNAME-** **oder PR_ATTACH_LONG_PATHNAME-Eigenschaft** enthält einen vollqualifizierten Pfad, der die Anlage identifiziert.</span><span class="sxs-lookup"><span data-stu-id="73644-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="73644-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="73644-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="73644-127">Die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft enthält ein eingebettetes Objekt, das die **IMessage-Schnittstelle** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73644-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="73644-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="73644-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="73644-129">Die Anlage ist ein eingebettetes OLE-Objekt.</span><span class="sxs-lookup"><span data-stu-id="73644-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="73644-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="73644-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="73644-131">Der Anlageninhalt befindet sich nicht in der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="73644-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="73644-132">Beim Erstellen verfügen alle Anlagenobjekte über einen **PR_ATTACH_METHOD** Wert von **NO_ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="73644-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="73644-133">Clientanwendungen und Dienstanbieter müssen nur die Anlagemethode unterstützen, die durch den Wert ATTACH_BY_VALUE **wird.**</span><span class="sxs-lookup"><span data-stu-id="73644-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="73644-134">Die anderen Anlagenmethoden sind optional.</span><span class="sxs-lookup"><span data-stu-id="73644-134">The other attachment methods are optional.</span></span> <span data-ttu-id="73644-135">Der Nachrichtenspeicher erzwingt keine Konsistenz  zwischen dem Wert PR_ATTACH_METHOD und den Werten der anderen Anlageneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="73644-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="73644-136">Namen der universellen Benennungskonvention (Universal Naming Convention, UNC) werden für vollqualifizierte Pfade empfohlen, die mit ATTACH_BY_REFERENCE **und** **ATTACH_BY_REF_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="73644-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="73644-137">Bei **ATTACH_BY_REF_RESOLVE** ist ein absoluter Pfad schneller, da der MAPI-Spooler die Anlage in **ATTACH_BY_VALUE.**</span><span class="sxs-lookup"><span data-stu-id="73644-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="73644-138">Wenn **ATTACH_BY_REFERENCE** festgelegt ist, **PR_ATTACH_DATA_BIN** leer sein.</span><span class="sxs-lookup"><span data-stu-id="73644-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="73644-139">Ein ausgehendes Gateway kann eine **ATTACH_BY_REFERENCE** anlage in eine ATTACH_BY_VALUE anlage  verwandeln, indem die Anlagendaten in die PR_ATTACH_DATA_BIN **werden.**</span><span class="sxs-lookup"><span data-stu-id="73644-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="73644-140">Wenn **ATTACH_BY_REF_RESOLVE** festgelegt ist, **muss PR_ATTACH_DATA_BIN** leer sein.</span><span class="sxs-lookup"><span data-stu-id="73644-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="73644-141">Wenn die Nachricht, die die **ATTACH_BY_REF_RESOLVE** enthält, gesendet wird, kopiert der MAPI-Spooler die Anlagendaten in eine **ATTACH_BY_VALUE** Anlage.</span><span class="sxs-lookup"><span data-stu-id="73644-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="73644-142">Bei diesem Auflösungsprozess werden die Anlagendaten in **PR_ATTACH_DATA_BIN.**</span><span class="sxs-lookup"><span data-stu-id="73644-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="73644-143">Wenn **ATTACH_BY_REF_ONLY** festgelegt ist, **PR_ATTACH_DATA_BIN** leer sein, und das Messagingsystem löst den Anlagenverweis nie auf.</span><span class="sxs-lookup"><span data-stu-id="73644-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="73644-144">Verwenden Sie diesen Wert, wenn Sie den Link senden möchten, jedoch nicht die Daten.</span><span class="sxs-lookup"><span data-stu-id="73644-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="73644-145">Wenn sich das OLE-Objekt im OLE 2.0-IStorage-Format befindet, ist der Zugriff auf die **Daten** über PR_ATTACH_DATA_OBJ. </span><span class="sxs-lookup"><span data-stu-id="73644-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="73644-146">Wenn sich das OLE-Objekt im OLE 1.0-OLESTREAM-Format befindet, kann über PR_ATTACH_DATA_BIN **als** IStream auf die **Daten zugegriffen werden.** </span><span class="sxs-lookup"><span data-stu-id="73644-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="73644-147">Der Typ der #A0 kann durch den Wert PR_ATTACH_TAG **(** [PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="73644-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="73644-148">Weitere Informationen zu OLE-Schnittstellen und -Formaten finden Sie unter  *OLE Programmer's Reference*  .</span><span class="sxs-lookup"><span data-stu-id="73644-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="73644-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="73644-149">Remarks</span></span>

<span data-ttu-id="73644-150">Wenn die **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE** wird, befindet sich der Anlageninhalt nicht in der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="73644-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="73644-151">Stattdessen enthält die **PR_ATTACH_LONG_FILENAME-Eigenschaft** eine absolute URL zum Anlageninhalt, der online gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="73644-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="73644-152">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="73644-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73644-153">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="73644-153">Protocol specifications</span></span>

<span data-ttu-id="73644-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73644-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73644-155">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="73644-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73644-156">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="73644-156">Header files</span></span>

<span data-ttu-id="73644-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73644-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="73644-158">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="73644-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="73644-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73644-159">Mapitags.h</span></span>
  
> <span data-ttu-id="73644-160">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="73644-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73644-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73644-161">See also</span></span>



[<span data-ttu-id="73644-162">PidTagStoreSupportMask (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="73644-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="73644-163">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73644-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73644-164">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="73644-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73644-165">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="73644-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73644-166">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="73644-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

