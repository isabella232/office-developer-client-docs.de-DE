---
title: Kanonische Pidtagexpirytime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryTime
api_type:
- HeaderDef
ms.assetid: 6e4d4ee9-c6b1-4987-b02e-684c2af3d21c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8d6fa58e61dde30292487c95fb8a74d568a3bbeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316373"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="fa326-103">Kanonische Pidtagexpirytime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fa326-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="fa326-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa326-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa326-105">Enthält das Datum und die Uhrzeit, zu denen das Messagingsystem den Inhalt einer Nachricht ungültig machen kann.</span><span class="sxs-lookup"><span data-stu-id="fa326-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa326-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fa326-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa326-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="fa326-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="fa326-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fa326-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa326-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="fa326-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="fa326-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fa326-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa326-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fa326-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fa326-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fa326-112">Area:</span></span>  <br/> |<span data-ttu-id="fa326-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="fa326-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa326-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa326-114">Remarks</span></span>

<span data-ttu-id="fa326-115">Diese Eigenschaft wird verwendet, um das Messagingsystem bei der Verarbeitung der übermittelten zwischenmenschlichen Nachrichten zu leiten.</span><span class="sxs-lookup"><span data-stu-id="fa326-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fa326-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fa326-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa326-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fa326-117">Protocol specifications</span></span>

<span data-ttu-id="fa326-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa326-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa326-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fa326-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa326-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa326-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa326-121">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="fa326-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa326-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="fa326-122">Header files</span></span>

<span data-ttu-id="fa326-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fa326-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa326-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="fa326-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa326-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="fa326-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fa326-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fa326-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa326-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa326-127">See also</span></span>



[<span data-ttu-id="fa326-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa326-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa326-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa326-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa326-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fa326-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa326-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fa326-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

