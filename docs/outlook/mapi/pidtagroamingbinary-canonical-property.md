---
title: PidTagRoamingBinary (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359563"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="22e84-103">PidTagRoamingBinary (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="22e84-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="22e84-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22e84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22e84-105">Enthält einen Nachrichtendatenstrom, der einer Unterklasse derIPM.Config **uration-Klasse zugeordnet** ist.</span><span class="sxs-lookup"><span data-stu-id="22e84-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22e84-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="22e84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22e84-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="22e84-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="22e84-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="22e84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22e84-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="22e84-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="22e84-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="22e84-110">Data type:</span></span>  <br/> |<span data-ttu-id="22e84-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="22e84-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="22e84-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="22e84-112">Area:</span></span>  <br/> |<span data-ttu-id="22e84-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="22e84-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22e84-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22e84-114">Remarks</span></span>

<span data-ttu-id="22e84-115">Diese Eigenschaft enthält den Datenstrom, der einer **IPM.Config-Nachricht zugeordnet** ist.</span><span class="sxs-lookup"><span data-stu-id="22e84-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="22e84-116">Das Format des Datenstroms hängt von der Nachrichtenklasse ab.</span><span class="sxs-lookup"><span data-stu-id="22e84-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="22e84-117">Beispielsweise wird eine Nachricht vom Klassentyp **IPM.Configuration. AutoComplete** würde als [AutoComplete Stream formatiert.](autocomplete-stream.md)</span><span class="sxs-lookup"><span data-stu-id="22e84-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22e84-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="22e84-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22e84-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="22e84-119">Protocol specifications</span></span>

<span data-ttu-id="22e84-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22e84-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22e84-121">Enthält Verweise auf Microsoft Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="22e84-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22e84-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22e84-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22e84-123">Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="22e84-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22e84-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="22e84-124">Header files</span></span>

<span data-ttu-id="22e84-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22e84-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="22e84-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="22e84-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="22e84-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="22e84-127">Mapitags.h</span></span>
  
> <span data-ttu-id="22e84-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="22e84-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22e84-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22e84-129">See also</span></span>



[<span data-ttu-id="22e84-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22e84-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22e84-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="22e84-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22e84-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="22e84-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22e84-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="22e84-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

