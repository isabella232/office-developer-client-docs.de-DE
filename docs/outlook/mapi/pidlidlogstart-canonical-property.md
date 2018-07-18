---
title: PidLidLogStart (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 55ba18a1dcbce5e3f7996184dae45a638f9531e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793657"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="9f9cc-103">PidLidLogStart (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9f9cc-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="9f9cc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f9cc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f9cc-105">Stellt das Startdatum und die Uhrzeit für die Journalnachricht.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f9cc-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9f9cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f9cc-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="9f9cc-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="9f9cc-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="9f9cc-108">Property set:</span></span>  <br/> |<span data-ttu-id="9f9cc-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="9f9cc-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="9f9cc-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="9f9cc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9f9cc-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="9f9cc-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="9f9cc-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9f9cc-112">Data type:</span></span>  <br/> |<span data-ttu-id="9f9cc-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9f9cc-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9f9cc-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9f9cc-114">Area:</span></span>  <br/> |<span data-ttu-id="9f9cc-115">Journal</span><span class="sxs-lookup"><span data-stu-id="9f9cc-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f9cc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f9cc-116">Remarks</span></span>

<span data-ttu-id="9f9cc-117">Die Zeit in koordinierter Weltzeit (UTC), wenn die Aktivität begann muss die Eigenschaft **DispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f9cc-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9f9cc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f9cc-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9f9cc-119">Protocol specifications</span></span>

<span data-ttu-id="9f9cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f9cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f9cc-121">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f9cc-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f9cc-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f9cc-123">Gibt die Eigenschaften und Operationen, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f9cc-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9f9cc-124">Header files</span></span>

<span data-ttu-id="9f9cc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f9cc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f9cc-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f9cc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f9cc-127">See also</span></span>



[<span data-ttu-id="9f9cc-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f9cc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f9cc-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f9cc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f9cc-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9f9cc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f9cc-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9f9cc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

