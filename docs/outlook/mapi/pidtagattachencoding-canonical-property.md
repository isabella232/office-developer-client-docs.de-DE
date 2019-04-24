---
title: Kanonische Pidtagattachencoding (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345493"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="0ec6b-103">Kanonische Pidtagattachencoding (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0ec6b-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="0ec6b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ec6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ec6b-105">Enthält einen ASN. 1-Objektbezeichner, der die Codierung für eine Anlage angibt.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ec6b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0ec6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ec6b-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="0ec6b-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="0ec6b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0ec6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ec6b-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="0ec6b-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="0ec6b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0ec6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ec6b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ec6b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0ec6b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0ec6b-112">Area:</span></span>  <br/> |<span data-ttu-id="0ec6b-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="0ec6b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ec6b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ec6b-114">Remarks</span></span>

<span data-ttu-id="0ec6b-115">Diese Eigenschaft gibt den Algorithmus an, der zum Transformieren der Daten in einer Anlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="0ec6b-116">**Hinweis** Die Eigenschaften **PR_ATTACH_ENCODING** und **PR_ATTACH_TAG** ([pidtagattachtag (](pidtagattachtag-canonical-property.md)) sollten nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="0ec6b-117">Sie sind nicht gekoppelt oder verknüpft.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-117">They are not paired or related.</span></span> <span data-ttu-id="0ec6b-118">**PR_ATTACH_TAG** identifiziert die Anwendung, die die Anlage ursprünglich generiert hat.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="0ec6b-119">"Object" hat eine wesentlich allgemeinere Bedeutung in der Term-Objekt-ID und in X. 400 als bei der objektorientierten Programmierung.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="0ec6b-120">Die Objekt-ID-Syntax und die Sample-Objekt-IDs werden in der MAPIOID definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="0ec6b-121">Werte für **PR_ATTACH_ENCODING** sind nicht auf diejenigen beschränkt, die in MAPIOID definiert sind. H.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="0ec6b-122">Beispielsweise können angeschlossene Macintosh-Dateien einen Bezeichner wie MacBinary verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="0ec6b-123">Vollständige Informationen zu diesen Objektbezeichnern finden Sie in der Dokumentation zu ASN. 1, X. 208 und X. 209.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="0ec6b-124">Der Objektbezeichner befindet sich im Application-Reference-Element der FTBP (File Transfer Body Teil)-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0ec6b-125">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0ec6b-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ec6b-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0ec6b-126">Protocol specifications</span></span>

<span data-ttu-id="0ec6b-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ec6b-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ec6b-128">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ec6b-129">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0ec6b-129">Header files</span></span>

<span data-ttu-id="0ec6b-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0ec6b-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ec6b-131">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ec6b-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0ec6b-132">Mapitags.h</span></span>
  
> <span data-ttu-id="0ec6b-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0ec6b-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ec6b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ec6b-134">See also</span></span>



[<span data-ttu-id="0ec6b-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ec6b-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ec6b-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ec6b-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ec6b-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0ec6b-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ec6b-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0ec6b-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

