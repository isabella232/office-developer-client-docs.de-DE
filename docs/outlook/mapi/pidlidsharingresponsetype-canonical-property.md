---
title: PidLidSharingResponseType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 34e8a3c73715a75b8007646e5ba3b0dc3e1ae919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331192"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="4510a-103">PidLidSharingResponseType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4510a-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="4510a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4510a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4510a-105">Gibt den Typ der Antwort an, mit der der Empfänger der Freigabeanforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="4510a-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="4510a-106">Dies ist eine Eigenschaft einer Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="4510a-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4510a-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4510a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="4510a-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="4510a-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="4510a-109">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="4510a-109">Property set:</span></span>  <br/> |<span data-ttu-id="4510a-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="4510a-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="4510a-111">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4510a-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4510a-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="4510a-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="4510a-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4510a-113">Data type:</span></span>  <br/> |<span data-ttu-id="4510a-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4510a-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4510a-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4510a-115">Area:</span></span>  <br/> |<span data-ttu-id="4510a-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="4510a-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4510a-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4510a-117">Remarks</span></span>

<span data-ttu-id="4510a-118">Der Wert dieser Eigenschaft muss auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4510a-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="4510a-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4510a-119">**Value**</span></span>|<span data-ttu-id="4510a-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4510a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4510a-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4510a-121">0x00000000</span></span>  <br/> |<span data-ttu-id="4510a-122">Keine Antwort</span><span class="sxs-lookup"><span data-stu-id="4510a-122">No response</span></span>  <br/> |
|<span data-ttu-id="4510a-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4510a-123">0x00000001</span></span>  <br/> |<span data-ttu-id="4510a-124">Akzeptiert</span><span class="sxs-lookup"><span data-stu-id="4510a-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="4510a-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4510a-125">0x00000002</span></span>  <br/> |<span data-ttu-id="4510a-126">Verweigert</span><span class="sxs-lookup"><span data-stu-id="4510a-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4510a-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4510a-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4510a-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4510a-128">Protocol specifications</span></span>

<span data-ttu-id="4510a-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4510a-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4510a-130">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4510a-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4510a-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4510a-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4510a-132">Gibt Postfachordner zwischen Clients zurück.</span><span class="sxs-lookup"><span data-stu-id="4510a-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4510a-133">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4510a-133">Header files</span></span>

<span data-ttu-id="4510a-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4510a-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="4510a-135">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4510a-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4510a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4510a-136">See also</span></span>



[<span data-ttu-id="4510a-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4510a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4510a-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4510a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4510a-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4510a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4510a-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4510a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

