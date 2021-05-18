---
title: PidTagRoamingXmlStream (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingXmlStream
api_type:
- COM
ms.assetid: ce55b50e-3dbf-4690-9102-c08f35ada82e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3e7ce1f810a1dd37cd4370ceb423b664d75878a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359542"
---
# <a name="pidtagroamingxmlstream-canonical-property"></a><span data-ttu-id="895b0-103">PidTagRoamingXmlStream (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="895b0-103">PidTagRoamingXmlStream Canonical Property</span></span>

  
  
<span data-ttu-id="895b0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="895b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="895b0-105">Enthält einen beliebigen XML-Stream.</span><span class="sxs-lookup"><span data-stu-id="895b0-105">Contains an arbitrary XML stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="895b0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="895b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="895b0-107">PR_ROAMING_XMLSTREAM</span><span class="sxs-lookup"><span data-stu-id="895b0-107">PR_ROAMING_XMLSTREAM</span></span>  <br/> |
|<span data-ttu-id="895b0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="895b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="895b0-109">0x7C08</span><span class="sxs-lookup"><span data-stu-id="895b0-109">0x7C08</span></span>  <br/> |
|<span data-ttu-id="895b0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="895b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="895b0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="895b0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="895b0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="895b0-112">Area:</span></span>  <br/> |<span data-ttu-id="895b0-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="895b0-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="895b0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="895b0-114">Remarks</span></span>

<span data-ttu-id="895b0-115">Diese Eigenschaft enthält einen beliebigen Stream von XML-Daten.</span><span class="sxs-lookup"><span data-stu-id="895b0-115">This property contains an arbitrary stream of XML data.</span></span> <span data-ttu-id="895b0-116">Andere Eigenschaften in der Nachricht können bestimmte Schemas enthalten, die in dieser Eigenschaft verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="895b0-116">Other properties in the message may imply specific schemas to use in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="895b0-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="895b0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="895b0-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="895b0-118">Protocol specifications</span></span>

<span data-ttu-id="895b0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="895b0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="895b0-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="895b0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="895b0-121">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="895b0-121">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="895b0-122">Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="895b0-122">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="895b0-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="895b0-123">Header files</span></span>

<span data-ttu-id="895b0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="895b0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="895b0-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="895b0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="895b0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="895b0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="895b0-127">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="895b0-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="895b0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="895b0-128">See also</span></span>



[<span data-ttu-id="895b0-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="895b0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="895b0-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="895b0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="895b0-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="895b0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="895b0-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="895b0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

