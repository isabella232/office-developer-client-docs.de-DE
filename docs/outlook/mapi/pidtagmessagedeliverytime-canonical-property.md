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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8ebaea7fb6888e51ee1ef658db53dcf3050644da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325613"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="39afe-103">PidTagMessageDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="39afe-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="39afe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39afe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39afe-105">Enthält das Datum und die Uhrzeit, zu der eine Nachricht zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="39afe-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39afe-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="39afe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39afe-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="39afe-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="39afe-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="39afe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39afe-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="39afe-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="39afe-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="39afe-110">Data type:</span></span>  <br/> |<span data-ttu-id="39afe-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="39afe-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="39afe-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="39afe-112">Area:</span></span>  <br/> |<span data-ttu-id="39afe-113">Nachrichtenzeit</span><span class="sxs-lookup"><span data-stu-id="39afe-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39afe-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39afe-114">Remarks</span></span>

<span data-ttu-id="39afe-115">Diese Eigenschaft beschreibt den Zeitpunkt, zu dem die Nachricht auf dem Server gespeichert wurde, und nicht den Downloadzeitpunkt, zu dem der Transportanbieter die Nachricht vom Server in den lokalen Speicher kopiert hat.</span><span class="sxs-lookup"><span data-stu-id="39afe-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="39afe-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="39afe-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39afe-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="39afe-117">Protocol specifications</span></span>

<span data-ttu-id="39afe-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39afe-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39afe-119">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="39afe-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39afe-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="39afe-120">Header files</span></span>

<span data-ttu-id="39afe-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39afe-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="39afe-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="39afe-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="39afe-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="39afe-123">Mapitags.h</span></span>
  
> <span data-ttu-id="39afe-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="39afe-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39afe-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39afe-125">See also</span></span>



[<span data-ttu-id="39afe-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39afe-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39afe-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="39afe-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39afe-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="39afe-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39afe-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="39afe-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

