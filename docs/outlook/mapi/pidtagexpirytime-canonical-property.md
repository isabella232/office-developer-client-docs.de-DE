---
title: PidTagExpiryTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d6fa58e61dde30292487c95fb8a74d568a3bbeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316373"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="90498-103">PidTagExpiryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="90498-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="90498-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90498-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90498-105">Enthält das Datum und die Uhrzeit, zu der das Messagingsystem den Inhalt einer Nachricht ungültig erklären kann.</span><span class="sxs-lookup"><span data-stu-id="90498-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90498-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="90498-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90498-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="90498-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="90498-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="90498-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90498-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="90498-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="90498-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="90498-110">Data type:</span></span>  <br/> |<span data-ttu-id="90498-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="90498-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="90498-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="90498-112">Area:</span></span>  <br/> |<span data-ttu-id="90498-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="90498-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90498-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90498-114">Remarks</span></span>

<span data-ttu-id="90498-115">Diese Eigenschaft wird verwendet, um das Messagingsystem bei der Verarbeitung von übermittelten zwischenmenschlichen Nachrichten an das Messagingsystem weiter zu senden.</span><span class="sxs-lookup"><span data-stu-id="90498-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90498-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="90498-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90498-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="90498-117">Protocol specifications</span></span>

<span data-ttu-id="90498-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90498-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90498-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="90498-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90498-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90498-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90498-121">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="90498-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90498-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="90498-122">Header files</span></span>

<span data-ttu-id="90498-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90498-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="90498-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="90498-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="90498-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90498-125">Mapitags.h</span></span>
  
> <span data-ttu-id="90498-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="90498-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90498-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90498-127">See also</span></span>



[<span data-ttu-id="90498-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90498-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90498-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="90498-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90498-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="90498-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90498-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="90498-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

