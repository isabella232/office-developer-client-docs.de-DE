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
ms.openlocfilehash: ab906d83ae4ad46747fd9037728620db1d656d25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360725"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a><span data-ttu-id="a7f64-103">PidTagViewDescriptorName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a7f64-103">PidTagViewDescriptorName Canonical Property</span></span>

  
  
<span data-ttu-id="a7f64-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7f64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7f64-105">Enthält den Namen eines Ansichtsdeskriptors.</span><span class="sxs-lookup"><span data-stu-id="a7f64-105">Contains the name of a view descriptor.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7f64-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a7f64-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7f64-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a7f64-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a7f64-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a7f64-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7f64-109">0x7006</span><span class="sxs-lookup"><span data-stu-id="a7f64-109">0x7006</span></span>  <br/> |
|<span data-ttu-id="a7f64-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a7f64-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7f64-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a7f64-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a7f64-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a7f64-112">Area:</span></span>  <br/> |<span data-ttu-id="a7f64-113">Durch nachrichtenklassendefinierte übertragungsfähige Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a7f64-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7f64-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7f64-114">Remarks</span></span>

<span data-ttu-id="a7f64-115">Diese Eigenschaften müssen auf eine nicht leere Zeichenfolge für eine Folder Associate Information (FAI)-Nachricht festgelegt werden, die Ansichtsdefinitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="a7f64-115">These properties must be set to a non-empty string for a Folder Associate Information (FAI) message that contains view definitions.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7f64-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a7f64-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7f64-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a7f64-117">Protocol specifications</span></span>

<span data-ttu-id="a7f64-118">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7f64-118">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7f64-119">Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="a7f64-119">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7f64-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a7f64-120">Header files</span></span>

<span data-ttu-id="a7f64-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7f64-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7f64-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a7f64-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7f64-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7f64-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a7f64-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a7f64-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7f64-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7f64-125">See also</span></span>



[<span data-ttu-id="a7f64-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7f64-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7f64-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a7f64-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7f64-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a7f64-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7f64-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a7f64-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

