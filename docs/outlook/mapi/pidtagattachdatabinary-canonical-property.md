---
title: PidTagAttachDataBinary (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3646f3e3906e62fe148fe1c2b6ddca39013391e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794092"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="e12ac-103">PidTagAttachDataBinary (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e12ac-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="e12ac-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e12ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e12ac-105">Enthält die binären Anlagedaten in der Regel über die Schnittstelle Object Linking and Embedding (OLE) **IStream** zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="e12ac-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e12ac-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e12ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e12ac-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="e12ac-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="e12ac-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e12ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e12ac-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="e12ac-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="e12ac-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e12ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="e12ac-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e12ac-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e12ac-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e12ac-112">Area:</span></span>  <br/> |<span data-ttu-id="e12ac-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="e12ac-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e12ac-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e12ac-114">Remarks</span></span>

<span data-ttu-id="e12ac-115">Diese Eigenschaft enthält das Attachment-Objekt, wenn der Wert der Eigenschaft **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) ATTACH_BY_VALUE, ist die übliche Anlage-Methode und die einzige unterstützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e12ac-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="e12ac-116">**PR_ATTACH_DATA_BIN** enthält auch Anlage OLE 1.0 **OLESTREAM** , wenn der Wert der **PR_ATTACH_METHOD** ATTACH_OLE ist.</span><span class="sxs-lookup"><span data-stu-id="e12ac-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="e12ac-117">**OLESTREAM** Anlagen können durch Aufrufen der OLE **:: CopyTo** -Methode in eine Datei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="e12ac-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="e12ac-118">Das Codierungstyp OLE kann von der **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))-Eigenschaft ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e12ac-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="e12ac-119">Für ein OLE-Dokument-Dateianlage Anbieter die Nachricht muss auf einen Aufruf [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) reagieren und reagiert optional zu einem Anruf auf **PR_ATTACH_DATA_BIN **.</span><span class="sxs-lookup"><span data-stu-id="e12ac-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="e12ac-120">Beachten Sie, dass **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** der Bezeichner für die gleichen freigeben, und daher zwei Darstellungen der gleichen-Eigenschaft werden.</span><span class="sxs-lookup"><span data-stu-id="e12ac-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="e12ac-121">Für ein Speicherobjekt können beispielsweise eine Verbunddatei in OLE 2.0-Dokumentdatei-Format, einige Dienstanbieter mit der MAPI- **IStreamDocfile** -Schnittstelle für verbesserte Leistung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="e12ac-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="e12ac-122">Ein Anbieter, der **IStreamDocfile** unterstützt muss es auf **PR_ATTACH_DATA_OBJ** verfügbar machen und kann optional auf **PR_ATTACH_DATA_BIN**machen.</span><span class="sxs-lookup"><span data-stu-id="e12ac-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="e12ac-123">Weitere Informationen zu OLE-Schnittstellen und Formate finden Sie unter [OLE und Daten übertragen](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="e12ac-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e12ac-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e12ac-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e12ac-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e12ac-125">Protocol specifications</span></span>

<span data-ttu-id="e12ac-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e12ac-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e12ac-127">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="e12ac-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="e12ac-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e12ac-128">Header Files</span></span>

<span data-ttu-id="e12ac-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e12ac-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e12ac-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e12ac-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="e12ac-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e12ac-131">Mapitags.h</span></span>
  
> <span data-ttu-id="e12ac-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e12ac-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e12ac-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e12ac-133">See also</span></span>



[<span data-ttu-id="e12ac-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e12ac-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e12ac-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e12ac-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e12ac-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e12ac-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e12ac-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e12ac-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

