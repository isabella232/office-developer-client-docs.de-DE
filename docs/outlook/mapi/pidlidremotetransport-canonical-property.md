---
title: PidLidRemoteTransport (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 124a0d8f23fcff9d1bca9d5debe4a9aa6fb6146c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587117"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="bb6cb-103">PidLidRemoteTransport (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bb6cb-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="bb6cb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb6cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb6cb-105">Gibt an, welches Konto das Headerelement zugeordnet wird, in erster Linie auf POP belassen auf Serverfunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="bb6cb-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb6cb-106">Zugeordnete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb6cb-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="bb6cb-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="bb6cb-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="bb6cb-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="bb6cb-108">Property set:</span></span>  <br/> |<span data-ttu-id="bb6cb-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="bb6cb-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="bb6cb-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="bb6cb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bb6cb-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="bb6cb-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="bb6cb-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bb6cb-112">Data type:</span></span>  <br/> |<span data-ttu-id="bb6cb-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="bb6cb-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="bb6cb-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bb6cb-114">Area:</span></span>  <br/> |<span data-ttu-id="bb6cb-115">Remote-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bb6cb-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb6cb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb6cb-116">Remarks</span></span>

<span data-ttu-id="bb6cb-117">Diese Eigenschaft ist nur für Nachrichten mit einer Nachrichtenklasse IPM relevant. Remote.</span><span class="sxs-lookup"><span data-stu-id="bb6cb-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="bb6cb-118">Microsoft Outlook behält eine Zuordnung von verschiedenen Konten, die auf einem bestimmten Speicher in einer Nachricht Ordner verknüpften Informationen (FAI) herunterladen möchten, aber es kann auch diese Informationen in der Registrierung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="bb6cb-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb6cb-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb6cb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb6cb-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bb6cb-120">Protocol specifications</span></span>

<span data-ttu-id="bb6cb-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="bb6cb-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="bb6cb-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bb6cb-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb6cb-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bb6cb-123">Header files</span></span>

<span data-ttu-id="bb6cb-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb6cb-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb6cb-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bb6cb-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb6cb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb6cb-126">See also</span></span>



[<span data-ttu-id="bb6cb-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb6cb-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb6cb-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb6cb-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb6cb-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bb6cb-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb6cb-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bb6cb-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

