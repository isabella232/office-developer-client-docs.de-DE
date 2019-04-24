---
title: Kanonische Pidlidremotetransport (-Eigenschaft
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
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285179"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="24f95-103">Kanonische Pidlidremotetransport (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24f95-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="24f95-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24f95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24f95-105">Gibt an, mit welchem Konto das Kopfzeilenelement verknüpft ist, und zwar in erster Linie für die Implementierung der Funktion "POP-Leave auf dem Server".</span><span class="sxs-lookup"><span data-stu-id="24f95-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24f95-106">Zugeordnete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24f95-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="24f95-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="24f95-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="24f95-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="24f95-108">Property set:</span></span>  <br/> |<span data-ttu-id="24f95-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="24f95-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="24f95-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="24f95-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="24f95-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="24f95-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="24f95-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="24f95-112">Data type:</span></span>  <br/> |<span data-ttu-id="24f95-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="24f95-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="24f95-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="24f95-114">Area:</span></span>  <br/> |<span data-ttu-id="24f95-115">Remote Nachricht</span><span class="sxs-lookup"><span data-stu-id="24f95-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24f95-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24f95-116">Remarks</span></span>

<span data-ttu-id="24f95-117">Diese Eigenschaft ist nur für Nachrichten relevant, die über eine Nachrichtenklasse von IPM verfügen. Remote.</span><span class="sxs-lookup"><span data-stu-id="24f95-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="24f95-118">In Microsoft Outlook werden verschiedene Konten, die in einen bestimmten Informationsspeicher heruntergeladen werden, in einer FAI-Nachricht (Folder Associated Information) aufbewahrt, aber diese Informationen können auch in der Registrierung aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="24f95-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="24f95-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24f95-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24f95-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="24f95-120">Protocol specifications</span></span>

<span data-ttu-id="24f95-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="24f95-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="24f95-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="24f95-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24f95-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="24f95-123">Header files</span></span>

<span data-ttu-id="24f95-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="24f95-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="24f95-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="24f95-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24f95-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24f95-126">See also</span></span>



[<span data-ttu-id="24f95-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24f95-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24f95-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24f95-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24f95-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="24f95-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24f95-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="24f95-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

