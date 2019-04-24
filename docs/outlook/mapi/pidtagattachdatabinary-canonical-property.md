---
title: Kanonische Pidtagattachdatabinary (-Eigenschaft
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
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356546"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="bd76a-103">Kanonische Pidtagattachdatabinary (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bd76a-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="bd76a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd76a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd76a-105">Enthält binäre Anlagendaten, auf die normalerweise über die **IStream** -Schnittstelle Object Linking and Embedding (OLE) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="bd76a-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd76a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bd76a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd76a-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="bd76a-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="bd76a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bd76a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd76a-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="bd76a-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="bd76a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bd76a-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd76a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd76a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bd76a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bd76a-112">Area:</span></span>  <br/> |<span data-ttu-id="bd76a-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="bd76a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd76a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd76a-114">Remarks</span></span>

<span data-ttu-id="bd76a-115">Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft ATTACH_BY_VALUE ist, bei dem es sich um die übliche Anlagemethode handelt und die einzige, die unterstützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="bd76a-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="bd76a-116">**PR_ATTACH_DATA_BIN** enthält auch eine OLE 1,0- **OLESTREAM** -Anlage, wenn der Wert von **PR_ATTACH_METHOD** ATTACH_OLE ist.</span><span class="sxs-lookup"><span data-stu-id="bd76a-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="bd76a-117">**OLESTREAM** -Anlagen können durch Aufrufen der OLE **IStream:: CopyTo** -Methode in eine Datei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd76a-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="bd76a-118">Der OLE-Codierungs kann anhand der **PR_ATTACH_TAG** ([pidtagattachtag (](pidtagattachtag-canonical-property.md))-Eigenschaft bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="bd76a-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="bd76a-119">Bei einer OLE-Dokumentdatei Anlage muss der Nachrichtenspeicher Anbieter auf einen [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Aufruf unter **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md)) Antworten und optional auf einen Aufruf von \*\*PR_ATTACH_DATA_BIN \*\*.</span><span class="sxs-lookup"><span data-stu-id="bd76a-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="bd76a-120">Beachten Sie, dass **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** denselben Eigenschaftenbezeichner verwenden und daher zwei Darstellungen derselben Eigenschaft sind.</span><span class="sxs-lookup"><span data-stu-id="bd76a-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="bd76a-121">Bei einem Speicherobjekt, wie beispielsweise einer Verbunddatei im DOCFILE-Format von OLE 2,0, können einige Dienstanbieter diese mit der MAPI- **IStreamDocfile** -Schnittstelle für eine verbesserte Leistung öffnen.</span><span class="sxs-lookup"><span data-stu-id="bd76a-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="bd76a-122">Ein Anbieter, der **IStreamDocfile** unterstützt, muss ihn auf **PR_ATTACH_DATA_OBJ** verfügbar machen und optional auf **PR_ATTACH_DATA_BIN**verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="bd76a-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="bd76a-123">Weitere Informationen zu OLE-Schnittstellen und Formaten finden Sie unter [OLE und Daten Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd76a-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bd76a-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bd76a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd76a-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bd76a-125">Protocol specifications</span></span>

<span data-ttu-id="bd76a-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd76a-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd76a-127">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="bd76a-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="bd76a-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bd76a-128">Header Files</span></span>

<span data-ttu-id="bd76a-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bd76a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd76a-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bd76a-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd76a-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bd76a-131">Mapitags.h</span></span>
  
> <span data-ttu-id="bd76a-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bd76a-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd76a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd76a-133">See also</span></span>



[<span data-ttu-id="bd76a-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd76a-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd76a-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd76a-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd76a-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bd76a-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd76a-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bd76a-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

