---
title: PidTagAttachDataObject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339284"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="b220a-103">PidTagAttachDataObject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b220a-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="b220a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b220a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b220a-105">Enthält ein Attachment-Objekt, auf das in der Regel über die **Ole-IStorage-Schnittstelle** (Object Linking and Embedding) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="b220a-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b220a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b220a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b220a-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="b220a-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="b220a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b220a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b220a-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="b220a-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="b220a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b220a-110">Data type:</span></span>  <br/> |<span data-ttu-id="b220a-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b220a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b220a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b220a-112">Area:</span></span>  <br/> |<span data-ttu-id="b220a-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="b220a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b220a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b220a-114">Remarks</span></span>

<span data-ttu-id="b220a-115">Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft ATTACH_EMBEDDED_MSG **oder** **ATTACH_OLE**.</span><span class="sxs-lookup"><span data-stu-id="b220a-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="b220a-116">Der #A0 kann anhand von PR_ATTACH_TAG **(** [PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="b220a-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="b220a-117">Für eine Anlage, die dem ATTACH_EMBEDDED_MSG **zugeordnet** ist, kann die [IMessage:IMAPIProp-Schnittstelle](imessageimapiprop.md) für einen schnelleren Zugriff verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b220a-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="b220a-118">Für ein eingebettetes dynamisches #A0 enthält die **PR_ATTACH_DATA_OBJ-Eigenschaft** eigene Renderinginformationen, und die **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) -Eigenschaft sollte nicht vorhanden oder leer sein.</span><span class="sxs-lookup"><span data-stu-id="b220a-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="b220a-119">Für eine #A0 muss der Nachrichtenspeicheranbieter auf einen [IMAPIProp::OpenProperty-Aufruf](imapiprop-openproperty.md) an **PR_ATTACH_DATA_OBJ** reagieren und kann optional auf einen Aufruf von **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) reagieren.</span><span class="sxs-lookup"><span data-stu-id="b220a-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="b220a-120">Die **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** haben dieselbe Eigenschafts-ID und sind somit zwei Wiedergaben derselben Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b220a-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="b220a-121">Für ein Speicherobjekt, z. B. eine Zusammengesetztdatei im OLE 2.0-Docfile-Format, ermöglichen einige Dienstanbieter das Öffnen mit der MAPI **IStreamDocfile-Schnittstelle,** einer Unterklasse von **IStream** ohne zusätzliche Member, die zur Optimierung der Leistung entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="b220a-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="b220a-122">Das potenzielle Speichern reicht aus,  um den Versuch zu rechtfertigen, PR_ATTACH_DATA_OBJ **IStreamDocfile zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="b220a-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="b220a-123">Wenn **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgegeben wird, kann der Client  die PR_ATTACH_DATA_BIN **IStream öffnen.**</span><span class="sxs-lookup"><span data-stu-id="b220a-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="b220a-124">Wenn die Clientanwendung oder der Dienstanbieter ein Anlagenunterobjekt nicht mithilfe von PR_ATTACH_DATA_OBJ mithilfe von **PR_ATTACH_METHOD** öffnen **kann,** sollte PR_ATTACH_DATA_BIN **.**</span><span class="sxs-lookup"><span data-stu-id="b220a-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="b220a-125">Weitere Informationen zu OLE-Schnittstellen und -Formaten finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="b220a-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b220a-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b220a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b220a-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b220a-127">Protocol specifications</span></span>

<span data-ttu-id="b220a-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b220a-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b220a-129">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="b220a-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="b220a-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b220a-130">Header Files</span></span>

<span data-ttu-id="b220a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b220a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b220a-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b220a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b220a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b220a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b220a-134">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b220a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b220a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b220a-135">See also</span></span>



[<span data-ttu-id="b220a-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b220a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b220a-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b220a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b220a-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b220a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b220a-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b220a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

