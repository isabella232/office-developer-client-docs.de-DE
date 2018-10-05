---
title: PidTagAttachEncoding (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382771"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="d3784-103">PidTagAttachEncoding (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d3784-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="d3784-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3784-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3784-105">ASN. 1 Objektbezeichner, der angibt, die Codierung für eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="d3784-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3784-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d3784-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3784-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="d3784-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="d3784-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d3784-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d3784-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="d3784-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="d3784-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d3784-110">Data type:</span></span>  <br/> |<span data-ttu-id="d3784-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d3784-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d3784-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d3784-112">Area:</span></span>  <br/> |<span data-ttu-id="d3784-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="d3784-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3784-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3784-114">Remarks</span></span>

<span data-ttu-id="d3784-115">Diese Eigenschaft gibt den Algorithmus zum Transformieren der Daten in einer Anlage.</span><span class="sxs-lookup"><span data-stu-id="d3784-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="d3784-116">**Hinweis** Die **PR_ATTACH_ENCODING** und **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) Eigenschaften darf nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="d3784-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="d3784-117">Sie werden nicht verbunden oder verwandte.</span><span class="sxs-lookup"><span data-stu-id="d3784-117">They are not paired or related.</span></span> <span data-ttu-id="d3784-118">**PR_ATTACH_TAG** identifiziert die Anwendung, die die Anlage ursprünglich erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="d3784-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="d3784-119">"Objekt" hat eine sehr viel allgemeine Bedeutung in den Begriff Objektbezeichner und x. 400-, als im objektorientiertes Programmieren.</span><span class="sxs-lookup"><span data-stu-id="d3784-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="d3784-120">Die Objekt-ID zu Syntax und Beispiel-Objekt-IDs werden in der MAPIOID definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="d3784-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="d3784-121">Werte für **PR_ATTACH_ENCODING** sind nicht auf den in MAPIOID definierten beschränkt. H.</span><span class="sxs-lookup"><span data-stu-id="d3784-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="d3784-122">Angefügte Macintosh-Dateien können beispielsweise einen Bezeichner wie MacBinary verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3784-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="d3784-123">Umfassende Informationen zu diesen Objektbezeichner finden Sie in der Dokumentation auf ASN. 1, X.208 und X.209.</span><span class="sxs-lookup"><span data-stu-id="d3784-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="d3784-124">Die Objekt-ID wird im Application-Referenz-Element der Umgebung FTBP (File Transfer Body Part) gefunden.</span><span class="sxs-lookup"><span data-stu-id="d3784-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d3784-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3784-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3784-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d3784-126">Protocol specifications</span></span>

<span data-ttu-id="d3784-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3784-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3784-128">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="d3784-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3784-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d3784-129">Header files</span></span>

<span data-ttu-id="d3784-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3784-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3784-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d3784-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d3784-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d3784-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d3784-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d3784-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3784-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3784-134">See also</span></span>



[<span data-ttu-id="d3784-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3784-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3784-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3784-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3784-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d3784-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3784-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d3784-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

