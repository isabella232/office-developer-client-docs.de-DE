---
title: Kanonische Pidtagattachcontentbase (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentBase
api_type:
- HeaderDef
ms.assetid: 35c10264-6998-4c46-8cef-82708c96d9c7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ec1db68d9168e7260a32aaf7708897df6124725a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360508"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="b31cf-103">Kanonische Pidtagattachcontentbase (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b31cf-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="b31cf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b31cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b31cf-105">Enthält die Inhalts Basis Kopfzeile einer MIME-Nachrichtenanlage (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="b31cf-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b31cf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b31cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b31cf-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="b31cf-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="b31cf-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b31cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b31cf-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="b31cf-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="b31cf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b31cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="b31cf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b31cf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b31cf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b31cf-112">Area:</span></span>  <br/> |<span data-ttu-id="b31cf-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="b31cf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b31cf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b31cf-114">Remarks</span></span>

<span data-ttu-id="b31cf-115">Diese Eigenschaften werden für die MHTML-Unterstützung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b31cf-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="b31cf-116">Sie stellen die Inhalts Basis Kopfzeile für den entsprechenden MIME-Textteil dar.</span><span class="sxs-lookup"><span data-stu-id="b31cf-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b31cf-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b31cf-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b31cf-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b31cf-118">Protocol specifications</span></span>

<span data-ttu-id="b31cf-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b31cf-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b31cf-120">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="b31cf-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b31cf-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b31cf-121">Header files</span></span>

<span data-ttu-id="b31cf-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b31cf-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="b31cf-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b31cf-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="b31cf-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b31cf-124">Mapitags.h</span></span>
  
> <span data-ttu-id="b31cf-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b31cf-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b31cf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b31cf-126">See also</span></span>



[<span data-ttu-id="b31cf-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b31cf-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b31cf-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b31cf-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b31cf-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b31cf-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b31cf-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b31cf-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

