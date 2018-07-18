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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793770"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="248c2-103">PidLidRemoteTransport (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="248c2-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="248c2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="248c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="248c2-105">Gibt an, welches Konto das Headerelement zugeordnet wird, in erster Linie auf POP belassen auf Serverfunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="248c2-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="248c2-106">Zugeordnete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="248c2-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="248c2-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="248c2-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="248c2-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="248c2-108">Property set:</span></span>  <br/> |<span data-ttu-id="248c2-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="248c2-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="248c2-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="248c2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="248c2-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="248c2-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="248c2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="248c2-112">Data type:</span></span>  <br/> |<span data-ttu-id="248c2-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="248c2-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="248c2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="248c2-114">Area:</span></span>  <br/> |<span data-ttu-id="248c2-115">Remote-Nachricht</span><span class="sxs-lookup"><span data-stu-id="248c2-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="248c2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="248c2-116">Remarks</span></span>

<span data-ttu-id="248c2-117">Diese Eigenschaft ist nur für Nachrichten mit einer Nachrichtenklasse IPM relevant. Remote.</span><span class="sxs-lookup"><span data-stu-id="248c2-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="248c2-118">Microsoft Outlook behält eine Zuordnung von verschiedenen Konten, die auf einem bestimmten Speicher in einer Nachricht Ordner verknüpften Informationen (FAI) herunterladen möchten, aber es kann auch diese Informationen in der Registrierung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="248c2-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="248c2-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="248c2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="248c2-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="248c2-120">Protocol specifications</span></span>

<span data-ttu-id="248c2-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="248c2-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="248c2-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="248c2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="248c2-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="248c2-123">Header files</span></span>

<span data-ttu-id="248c2-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="248c2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="248c2-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="248c2-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="248c2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="248c2-126">See also</span></span>



[<span data-ttu-id="248c2-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="248c2-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="248c2-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="248c2-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="248c2-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="248c2-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="248c2-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="248c2-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

