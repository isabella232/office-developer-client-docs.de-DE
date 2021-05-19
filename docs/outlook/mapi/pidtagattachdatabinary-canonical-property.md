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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356546"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="825fd-103">PidTagAttachDataBinary (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="825fd-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="825fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="825fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="825fd-105">Enthält binäre Anlagendaten, auf die in der Regel über die Ole-IStream-Schnittstelle (Object Linking and Embedding) **zugegriffen** wird.</span><span class="sxs-lookup"><span data-stu-id="825fd-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="825fd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="825fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="825fd-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="825fd-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="825fd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="825fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="825fd-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="825fd-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="825fd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="825fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="825fd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="825fd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="825fd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="825fd-112">Area:</span></span>  <br/> |<span data-ttu-id="825fd-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="825fd-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="825fd-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="825fd-114">Remarks</span></span>

<span data-ttu-id="825fd-115">Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft ATTACH_BY_VALUE ist, was die übliche Anlagemethode ist und die einzige, die unterstützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="825fd-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="825fd-116">**PR_ATTACH_DATA_BIN** enthält auch eine OLE 1.0-OLESTREAM-Anlage, wenn der Wert PR_ATTACH_METHOD **wert** ATTACH_OLE. </span><span class="sxs-lookup"><span data-stu-id="825fd-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="825fd-117">**OLESTREAM-Anlagen** können durch Aufrufen der OLE **IStream::CopyTo-Methode** in eine Datei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="825fd-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="825fd-118">Der #A0 kann anhand der **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="825fd-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="825fd-119">Für eine #A0 muss der Nachrichtenspeicheranbieter auf einen [IMAPIProp::OpenProperty-Aufruf](imapiprop-openproperty.md) von **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) reagieren und kann optional auf einen Aufruf von PR_ATTACH_DATA_BIN **.**</span><span class="sxs-lookup"><span data-stu-id="825fd-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="825fd-120">Beachten **Sie, PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** denselben Eigenschaftenbezeichner verwenden und somit zwei Wiedergaben derselben Eigenschaft sind.</span><span class="sxs-lookup"><span data-stu-id="825fd-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="825fd-121">Für ein Speicherobjekt, z. B. eine Zusammengesetztdatei im OLE 2.0-Docfile-Format, ermöglichen einige Dienstanbieter das Öffnen mit der **MAPI-IStreamDocfile-Schnittstelle,** um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="825fd-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="825fd-122">Ein Anbieter, der **IStreamDocfile**  unterstützt, muss es auf PR_ATTACH_DATA_OBJ verfügbar machen und kann es optional auf **PR_ATTACH_DATA_BIN.**</span><span class="sxs-lookup"><span data-stu-id="825fd-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="825fd-123">Weitere Informationen zu OLE-Schnittstellen und -Formaten finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="825fd-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="825fd-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="825fd-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="825fd-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="825fd-125">Protocol specifications</span></span>

<span data-ttu-id="825fd-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="825fd-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="825fd-127">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="825fd-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="825fd-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="825fd-128">Header Files</span></span>

<span data-ttu-id="825fd-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="825fd-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="825fd-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="825fd-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="825fd-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="825fd-131">Mapitags.h</span></span>
  
> <span data-ttu-id="825fd-132">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="825fd-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="825fd-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="825fd-133">See also</span></span>



[<span data-ttu-id="825fd-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="825fd-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="825fd-135">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="825fd-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="825fd-136">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="825fd-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="825fd-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="825fd-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

