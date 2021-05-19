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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345493"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="0b9e4-103">PidTagAttachEncoding (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0b9e4-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="0b9e4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b9e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b9e4-105">Enthält einen ASN.1-Objektbezeichner, der die Codierung für eine Anlage angibt.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b9e4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0b9e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b9e4-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="0b9e4-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="0b9e4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0b9e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b9e4-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="0b9e4-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="0b9e4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0b9e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b9e4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0b9e4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0b9e4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0b9e4-112">Area:</span></span>  <br/> |<span data-ttu-id="0b9e4-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="0b9e4-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b9e4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b9e4-114">Remarks</span></span>

<span data-ttu-id="0b9e4-115">Diese Eigenschaft identifiziert den Algorithmus, der zum Transformieren der Daten in einer Anlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="0b9e4-116">**Hinweis** Die **eigenschaften PR_ATTACH_ENCODING** **und PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) sollten nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="0b9e4-117">Sie sind nicht gekoppelt oder verwandt.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-117">They are not paired or related.</span></span> <span data-ttu-id="0b9e4-118">**PR_ATTACH_TAG** identifiziert die Anwendung, die die Anlage ursprünglich generiert hat.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="0b9e4-119">"Object" hat im Begriff Objektbezeichner und in X.400 eine viel allgemeinere Bedeutung als in der objektorientierten Programmierung.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="0b9e4-120">Die Objektbezeichnersyntax und Beispielobjektbezeichner sind in der MAPIOID definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="0b9e4-121">Die Werte **für PR_ATTACH_ENCODING** sind nicht auf die werte beschränkt, die in MAPIOID.H definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="0b9e4-122">Angefügte Macintosh-Dateien können beispielsweise einen Bezeichner wie MacBinary verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="0b9e4-123">Ausführliche Informationen zu diesen Objektbezeichnern finden Sie in der Dokumentation zu ASN.1, X.208 und X.209.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="0b9e4-124">Der Objektbezeichner befindet sich im Anwendungsreferenzelement der FTBP(File Transfer Body Part)-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0b9e4-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0b9e4-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b9e4-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0b9e4-126">Protocol specifications</span></span>

<span data-ttu-id="0b9e4-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b9e4-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b9e4-128">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b9e4-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0b9e4-129">Header files</span></span>

<span data-ttu-id="0b9e4-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b9e4-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b9e4-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b9e4-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b9e4-132">Mapitags.h</span></span>
  
> <span data-ttu-id="0b9e4-133">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0b9e4-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b9e4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b9e4-134">See also</span></span>



[<span data-ttu-id="0b9e4-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b9e4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b9e4-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0b9e4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b9e4-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0b9e4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b9e4-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0b9e4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

