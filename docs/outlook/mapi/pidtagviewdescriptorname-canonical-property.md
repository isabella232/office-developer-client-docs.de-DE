---
title: PidTagViewDescriptorName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 55d838661dcbe0efb604e6a623a434f9ae87512e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567783"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a><span data-ttu-id="87c5a-103">PidTagViewDescriptorName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="87c5a-103">PidTagViewDescriptorName Canonical Property</span></span>

  
  
<span data-ttu-id="87c5a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87c5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87c5a-105">Der Name der eine Ansicht Deskriptor enthält.</span><span class="sxs-lookup"><span data-stu-id="87c5a-105">Contains the name of a view descriptor.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87c5a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="87c5a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87c5a-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span><span class="sxs-lookup"><span data-stu-id="87c5a-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span></span>  <br/> |
|<span data-ttu-id="87c5a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="87c5a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87c5a-109">0x7006</span><span class="sxs-lookup"><span data-stu-id="87c5a-109">0x7006</span></span>  <br/> |
|<span data-ttu-id="87c5a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="87c5a-110">Data type:</span></span>  <br/> |<span data-ttu-id="87c5a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87c5a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="87c5a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="87c5a-112">Area:</span></span>  <br/> |<span data-ttu-id="87c5a-113">Nachricht-Klasse definiert Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="87c5a-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87c5a-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="87c5a-114">Remarks</span></span>

<span data-ttu-id="87c5a-115">Diese Eigenschaften müssen auf eine nicht leere Zeichenfolge für eine Nachricht Ordner zuordnen Informationen (FAI) festgelegt werden, die Ansichtsdefinitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="87c5a-115">These properties must be set to a non-empty string for a Folder Associate Information (FAI) message that contains view definitions.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87c5a-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="87c5a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87c5a-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="87c5a-117">Protocol specifications</span></span>

<span data-ttu-id="87c5a-118">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87c5a-118">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87c5a-119">Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="87c5a-119">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87c5a-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="87c5a-120">Header files</span></span>

<span data-ttu-id="87c5a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87c5a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="87c5a-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="87c5a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="87c5a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="87c5a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="87c5a-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="87c5a-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87c5a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87c5a-125">See also</span></span>



[<span data-ttu-id="87c5a-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87c5a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87c5a-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87c5a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87c5a-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="87c5a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87c5a-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="87c5a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

