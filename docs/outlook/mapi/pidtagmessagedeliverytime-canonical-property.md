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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397345"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="a9e89-103">PidTagMessageDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a9e89-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="a9e89-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9e89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9e89-105">Enthält Datum und Uhrzeit, wenn eine Nachricht nicht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a9e89-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9e89-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a9e89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9e89-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="a9e89-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="a9e89-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a9e89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9e89-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="a9e89-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="a9e89-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a9e89-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9e89-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a9e89-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a9e89-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9e89-112">Area:</span></span>  <br/> |<span data-ttu-id="a9e89-113">Nachrichtzeit</span><span class="sxs-lookup"><span data-stu-id="a9e89-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9e89-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9e89-114">Remarks</span></span>

<span data-ttu-id="a9e89-115">Diese Eigenschaft beschreibt Zeitpunkt, zu dem die Nachricht auf dem Server gespeichert wurde, statt die Uhrzeit des Downloads, wenn der Adressbuchhierarchie die Nachricht vom Server auf den lokalen Speicher kopiert.</span><span class="sxs-lookup"><span data-stu-id="a9e89-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9e89-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a9e89-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9e89-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a9e89-117">Protocol specifications</span></span>

<span data-ttu-id="a9e89-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9e89-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9e89-119">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a9e89-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9e89-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a9e89-120">Header files</span></span>

<span data-ttu-id="a9e89-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9e89-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9e89-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a9e89-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9e89-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9e89-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a9e89-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a9e89-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9e89-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9e89-125">See also</span></span>



[<span data-ttu-id="a9e89-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9e89-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9e89-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9e89-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9e89-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a9e89-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9e89-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a9e89-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

