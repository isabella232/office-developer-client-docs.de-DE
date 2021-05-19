---
title: PidTagSearchFolderLastUsed (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderLastUsed
api_type:
- COM
ms.assetid: e4071307-6205-4079-ab65-7499d14f145c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7ff6df6eddc8e610341cb09ccb152f4ad748a984
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336533"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="936ff-103">PidTagSearchFolderLastUsed (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="936ff-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="936ff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="936ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="936ff-105">Stellt das letzte Mal dar, bei dem auf den Ordner zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="936ff-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="936ff-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="936ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="936ff-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="936ff-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="936ff-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="936ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="936ff-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="936ff-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="936ff-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="936ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="936ff-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="936ff-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="936ff-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="936ff-112">Area:</span></span>  <br/> |<span data-ttu-id="936ff-113">Suche</span><span class="sxs-lookup"><span data-stu-id="936ff-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="936ff-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="936ff-114">Remarks</span></span>

<span data-ttu-id="936ff-115">Diese Eigenschaft muss als Anzahl von Minuten seit Mitternacht koordinierte Weltzeit (UTC) 1. Januar 1601 formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="936ff-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="936ff-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="936ff-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="936ff-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="936ff-117">Protocol specifications</span></span>

<span data-ttu-id="936ff-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="936ff-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="936ff-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="936ff-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="936ff-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="936ff-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="936ff-121">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="936ff-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="936ff-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="936ff-122">Header files</span></span>

<span data-ttu-id="936ff-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="936ff-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="936ff-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="936ff-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="936ff-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="936ff-125">Mapitags.h</span></span>
  
> <span data-ttu-id="936ff-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="936ff-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="936ff-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="936ff-127">See also</span></span>



[<span data-ttu-id="936ff-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="936ff-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="936ff-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="936ff-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="936ff-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="936ff-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="936ff-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="936ff-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

