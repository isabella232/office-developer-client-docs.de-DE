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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4666a5837c9f9f2ceb209088929aa3d343eb02f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794374"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="1e251-103">PidTagExpiryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1e251-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="1e251-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e251-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e251-105">Enthält Datum und Uhrzeit, wann das messaging-System den Inhalt einer Nachricht ungültig machen können.</span><span class="sxs-lookup"><span data-stu-id="1e251-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e251-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1e251-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e251-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="1e251-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="1e251-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1e251-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e251-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="1e251-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="1e251-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1e251-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e251-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1e251-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1e251-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1e251-112">Area:</span></span>  <br/> |<span data-ttu-id="1e251-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="1e251-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e251-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e251-114">Remarks</span></span>

<span data-ttu-id="1e251-115">Diese Eigenschaft wird verwendet, um die direkte Nachrichtensystem in Behandlung Nachrichten zwischen Personen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="1e251-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e251-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1e251-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e251-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1e251-117">Protocol specifications</span></span>

<span data-ttu-id="1e251-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e251-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e251-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1e251-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1e251-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e251-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e251-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1e251-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e251-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1e251-122">Header files</span></span>

<span data-ttu-id="1e251-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e251-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e251-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1e251-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e251-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e251-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1e251-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1e251-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e251-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e251-127">See also</span></span>



[<span data-ttu-id="1e251-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e251-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e251-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e251-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e251-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1e251-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e251-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1e251-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

