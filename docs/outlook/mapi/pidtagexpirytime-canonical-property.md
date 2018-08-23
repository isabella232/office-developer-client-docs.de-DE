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
ms.openlocfilehash: 21e052545c9c5e68bf1bc2f8c1ead054163f3b8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566145"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="00373-103">PidTagExpiryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="00373-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="00373-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00373-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00373-105">Enthält Datum und Uhrzeit, wann das messaging-System den Inhalt einer Nachricht ungültig machen können.</span><span class="sxs-lookup"><span data-stu-id="00373-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00373-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="00373-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00373-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="00373-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="00373-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="00373-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00373-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="00373-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="00373-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="00373-110">Data type:</span></span>  <br/> |<span data-ttu-id="00373-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="00373-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="00373-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="00373-112">Area:</span></span>  <br/> |<span data-ttu-id="00373-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="00373-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00373-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="00373-114">Remarks</span></span>

<span data-ttu-id="00373-115">Diese Eigenschaft wird verwendet, um die direkte Nachrichtensystem in Behandlung Nachrichten zwischen Personen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="00373-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="00373-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="00373-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00373-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="00373-117">Protocol specifications</span></span>

<span data-ttu-id="00373-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00373-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00373-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="00373-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00373-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00373-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00373-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="00373-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00373-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="00373-122">Header files</span></span>

<span data-ttu-id="00373-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00373-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="00373-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="00373-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="00373-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00373-125">Mapitags.h</span></span>
  
> <span data-ttu-id="00373-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="00373-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00373-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00373-127">See also</span></span>



[<span data-ttu-id="00373-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00373-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00373-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00373-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00373-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="00373-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00373-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="00373-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

