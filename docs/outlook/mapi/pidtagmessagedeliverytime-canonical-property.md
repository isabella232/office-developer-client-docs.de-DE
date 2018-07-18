---
title: PidTagMessageDeliveryTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4fd74e99a8073db03ad47292677ff98efca58af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794598"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="f5bd4-103">PidTagMessageDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f5bd4-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="f5bd4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5bd4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5bd4-105">Enthält Datum und Uhrzeit, wenn eine Nachricht nicht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5bd4-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5bd4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f5bd4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5bd4-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="f5bd4-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="f5bd4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="f5bd4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5bd4-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="f5bd4-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="f5bd4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f5bd4-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5bd4-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f5bd4-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f5bd4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f5bd4-112">Area:</span></span>  <br/> |<span data-ttu-id="f5bd4-113">Nachrichtzeit</span><span class="sxs-lookup"><span data-stu-id="f5bd4-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5bd4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5bd4-114">Remarks</span></span>

<span data-ttu-id="f5bd4-115">Diese Eigenschaft beschreibt Zeitpunkt, zu dem die Nachricht auf dem Server gespeichert wurde, statt die Uhrzeit des Downloads, wenn der Adressbuchhierarchie die Nachricht vom Server auf den lokalen Speicher kopiert.</span><span class="sxs-lookup"><span data-stu-id="f5bd4-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5bd4-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f5bd4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5bd4-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f5bd4-117">Protocol specifications</span></span>

<span data-ttu-id="f5bd4-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bd4-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5bd4-119">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f5bd4-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5bd4-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f5bd4-120">Header files</span></span>

<span data-ttu-id="f5bd4-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5bd4-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5bd4-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f5bd4-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5bd4-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5bd4-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f5bd4-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f5bd4-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5bd4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5bd4-125">See also</span></span>



[<span data-ttu-id="f5bd4-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5bd4-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5bd4-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5bd4-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5bd4-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f5bd4-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5bd4-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f5bd4-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

