---
title: PidLidVerbResponse (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidVerbResponse
api_type:
- COM
ms.assetid: 6f3db5ac-f1cb-4c55-ab88-c126dd5f48ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2fa762a44a107f826923d71faa79fe865413c55c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581041"
---
# <a name="pidlidverbresponse-canonical-property"></a><span data-ttu-id="a5e6d-103">PidLidVerbResponse (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a5e6d-103">PidLidVerbResponse Canonical Property</span></span>

  
  
<span data-ttu-id="a5e6d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5e6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5e6d-105">Gibt die Stimmabgabe Option, die einem Teilnehmer ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a5e6d-105">Specifies the voting option that a respondent selected.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5e6d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a5e6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5e6d-107">dispidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="a5e6d-107">dispidVerbResponse</span></span>  <br/> |
|<span data-ttu-id="a5e6d-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="a5e6d-108">Property set:</span></span>  <br/> |<span data-ttu-id="a5e6d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a5e6d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a5e6d-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="a5e6d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5e6d-111">0x00008524</span><span class="sxs-lookup"><span data-stu-id="a5e6d-111">0x00008524</span></span>  <br/> |
|<span data-ttu-id="a5e6d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a5e6d-112">Data type:</span></span>  <br/> |<span data-ttu-id="a5e6d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a5e6d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a5e6d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a5e6d-114">Area:</span></span>  <br/> |<span data-ttu-id="a5e6d-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="a5e6d-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5e6d-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a5e6d-116">Remarks</span></span>

<span data-ttu-id="a5e6d-117">Diese Eigenschaft wird normalerweise auf einen der getrennten Werte festgelegt, die in der Eigenschaft **DispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) enthalten sind, auf denen der Befragten stimmen.</span><span class="sxs-lookup"><span data-stu-id="a5e6d-117">This property is usually set to one of the delimited values that are contained in the **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) property on which the respondent votes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5e6d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a5e6d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5e6d-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a5e6d-119">Protocol specifications</span></span>

<span data-ttu-id="a5e6d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5e6d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5e6d-121">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a5e6d-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5e6d-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5e6d-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5e6d-123">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a5e6d-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5e6d-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a5e6d-124">Header files</span></span>

<span data-ttu-id="a5e6d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5e6d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5e6d-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a5e6d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5e6d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5e6d-127">See also</span></span>



[<span data-ttu-id="a5e6d-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5e6d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5e6d-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5e6d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5e6d-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a5e6d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5e6d-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a5e6d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

