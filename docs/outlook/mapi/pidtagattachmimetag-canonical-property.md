---
title: Kanonische PidTagAttachMimeTag-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6f65d67903fa9ebb255345f8666cd53de5512cab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794114"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="47a01-103">Kanonische PidTagAttachMimeTag-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="47a01-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="47a01-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47a01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47a01-105">Enthält Formatierung Informationen über eine Anlage Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="47a01-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47a01-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="47a01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47a01-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="47a01-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="47a01-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="47a01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47a01-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="47a01-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="47a01-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="47a01-110">Data type:</span></span>  <br/> |<span data-ttu-id="47a01-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47a01-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="47a01-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="47a01-112">Area:</span></span>  <br/> |<span data-ttu-id="47a01-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="47a01-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47a01-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47a01-114">Remarks</span></span>

<span data-ttu-id="47a01-115">Wenn die **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))-Eigenschaft den Wert **OID_MIMETAG**enthält, sollte der Adressbuchhierarchie sehen Sie sich diese Eigenschaften, um zu bestimmen, wie die Anlage formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="47a01-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="47a01-116">Diese Eigenschaften werden aus dem Content-Type-Parameter des eingehenden MIME-Header kopiert.</span><span class="sxs-lookup"><span data-stu-id="47a01-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="47a01-117">Die Zusammensetzung der Zeichenfolge ist im Dokument RFC 1521 definiert.</span><span class="sxs-lookup"><span data-stu-id="47a01-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="47a01-118">Das Format ist Typ/Untertyp wie Anwendung/Binär oder Text/Plain.</span><span class="sxs-lookup"><span data-stu-id="47a01-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="47a01-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="47a01-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47a01-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="47a01-120">Protocol specifications</span></span>

<span data-ttu-id="47a01-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47a01-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47a01-122">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="47a01-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="47a01-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47a01-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47a01-124">Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="47a01-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47a01-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="47a01-125">Header files</span></span>

<span data-ttu-id="47a01-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47a01-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="47a01-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="47a01-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="47a01-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47a01-128">Mapitags.h</span></span>
  
> <span data-ttu-id="47a01-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="47a01-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47a01-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47a01-130">See also</span></span>



[<span data-ttu-id="47a01-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47a01-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47a01-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47a01-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47a01-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="47a01-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47a01-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="47a01-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

