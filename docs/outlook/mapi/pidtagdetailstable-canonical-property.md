---
title: Kanonische Pidtagdetailstable (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419254"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="985d3-103">Kanonische Pidtagdetailstable (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="985d3-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="985d3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="985d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="985d3-105">Enthält ein eingebettetes Anzeige Table-Objekt.</span><span class="sxs-lookup"><span data-stu-id="985d3-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="985d3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="985d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="985d3-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="985d3-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="985d3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="985d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="985d3-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="985d3-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="985d3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="985d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="985d3-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="985d3-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="985d3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="985d3-112">Area:</span></span>  <br/> |<span data-ttu-id="985d3-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="985d3-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="985d3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="985d3-114">Remarks</span></span>

<span data-ttu-id="985d3-115">Wenn Sie diese Eigenschaft an die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode für das Objekt übergeben, wird eine [IMAPITable](imapitableiunknown.md) -Schnittstelle zurückgegeben, die die Erstellung der Anzeigetabelle ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="985d3-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="985d3-116">MAPI verwendet diese Tabelle, um Eigenschaftenblätter für ein Adressbuchobjekt als Reaktion auf einen [IAddrBook::D ails](iaddrbook-details.md) -Aufruf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="985d3-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="985d3-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="985d3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="985d3-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="985d3-118">Header files</span></span>

<span data-ttu-id="985d3-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="985d3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="985d3-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="985d3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="985d3-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="985d3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="985d3-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="985d3-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="985d3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="985d3-123">See also</span></span>



[<span data-ttu-id="985d3-124">Kanonische Pidtagcreatetemplates (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="985d3-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="985d3-125">Kanonische Pidtagsearch (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="985d3-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="985d3-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="985d3-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="985d3-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="985d3-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="985d3-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="985d3-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="985d3-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="985d3-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

