---
title: PidTagDetailsTable (kanonische Eigenschaft)
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
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="24e55-103">PidTagDetailsTable (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="24e55-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="24e55-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24e55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24e55-105">Enthält ein eingebettetes Anzeigetabelle-Objekt.</span><span class="sxs-lookup"><span data-stu-id="24e55-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24e55-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="24e55-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24e55-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="24e55-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="24e55-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="24e55-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24e55-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="24e55-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="24e55-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="24e55-110">Data type:</span></span>  <br/> |<span data-ttu-id="24e55-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="24e55-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="24e55-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="24e55-112">Area:</span></span>  <br/> |<span data-ttu-id="24e55-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="24e55-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24e55-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24e55-114">Remarks</span></span>

<span data-ttu-id="24e55-115">Durch Übergeben dieser Eigenschaft an die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) für das Objekt wird eine [IMAPITable-Schnittstelle](imapitableiunknown.md) zurückgegeben, die das Erstellen der Anzeigetabelle ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="24e55-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="24e55-116">MAPI verwendet diese Tabelle, um Eigenschaftenblätter für ein Adressbuchobjekt als Reaktion auf einen [IAddrBook::D etails-Aufruf anzuzeigen.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="24e55-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="24e55-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24e55-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="24e55-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="24e55-118">Header files</span></span>

<span data-ttu-id="24e55-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24e55-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="24e55-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="24e55-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="24e55-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24e55-121">Mapitags.h</span></span>
  
> <span data-ttu-id="24e55-122">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="24e55-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24e55-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24e55-123">See also</span></span>



[<span data-ttu-id="24e55-124">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="24e55-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="24e55-125">PidTagSearch (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="24e55-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="24e55-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24e55-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24e55-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="24e55-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24e55-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="24e55-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24e55-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="24e55-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

