---
title: PidTagAttachTag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361082"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="4bc20-103">PidTagAttachTag (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4bc20-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="4bc20-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bc20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bc20-105">Enthält einen ASN.1-Objektbezeichner, der die Anwendung an gibt, die eine Anlage bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="4bc20-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4bc20-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4bc20-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4bc20-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="4bc20-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="4bc20-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4bc20-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4bc20-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="4bc20-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="4bc20-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4bc20-110">Data type:</span></span>  <br/> |<span data-ttu-id="4bc20-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4bc20-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4bc20-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4bc20-112">Area:</span></span>  <br/> |<span data-ttu-id="4bc20-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="4bc20-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4bc20-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4bc20-114">Remarks</span></span>

<span data-ttu-id="4bc20-115">Diese Eigenschaft identifiziert die Anwendung, die die Anlage ursprünglich generiert hat.</span><span class="sxs-lookup"><span data-stu-id="4bc20-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="4bc20-116">**Hinweis** Die **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) und **PR_ATTACH_TAG** eigenschaften sollten nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="4bc20-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="4bc20-117">Sie sind nicht gekoppelt oder verwandt.</span><span class="sxs-lookup"><span data-stu-id="4bc20-117">They are not paired or related.</span></span> <span data-ttu-id="4bc20-118">**PR_ATTACH_ENCODING** identifiziert den Algorithmus, der zum Transformieren der Daten in einer Anlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4bc20-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="4bc20-119">"Object" hat eine viel allgemeinere Bedeutung im Begriff Objektbezeichner und in der X.400-Verwendung als in der objektorientierten Programmierung.</span><span class="sxs-lookup"><span data-stu-id="4bc20-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="4bc20-120">Die Objektbezeichnersyntax und Beispielobjektbezeichner sind in der MAPIOID definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="4bc20-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="4bc20-121">Die Werte **für PR_ATTACH_TAG** sind nicht auf die werte beschränkt, die in MAPIOID.H definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4bc20-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="4bc20-122">Ausführliche Informationen zu diesen Objektbezeichnern finden Sie in der Dokumentation zu ASN.1, X.208 und X.209.</span><span class="sxs-lookup"><span data-stu-id="4bc20-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="4bc20-123">Der Objektbezeichner befindet sich im Application-Reference-Element der File Transfer Body Part (FTBP)-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4bc20-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4bc20-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4bc20-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4bc20-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4bc20-125">Protocol specifications</span></span>

<span data-ttu-id="4bc20-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bc20-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4bc20-127">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="4bc20-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4bc20-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4bc20-128">Header files</span></span>

<span data-ttu-id="4bc20-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4bc20-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="4bc20-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4bc20-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="4bc20-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4bc20-131">Mapitags.h</span></span>
  
> <span data-ttu-id="4bc20-132">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4bc20-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4bc20-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bc20-133">See also</span></span>



[<span data-ttu-id="4bc20-134">PidTagAttachMimeTag (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4bc20-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="4bc20-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4bc20-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4bc20-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4bc20-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4bc20-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4bc20-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4bc20-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4bc20-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

