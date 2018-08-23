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
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585787"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="8b394-103">PidTagDetailsTable (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8b394-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="8b394-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b394-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b394-105">Enthält eine eingebettete Anzeige Table-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b394-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b394-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8b394-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b394-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="8b394-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="8b394-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8b394-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b394-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="8b394-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="8b394-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8b394-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b394-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="8b394-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="8b394-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8b394-112">Area:</span></span>  <br/> |<span data-ttu-id="8b394-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="8b394-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b394-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="8b394-114">Remarks</span></span>

<span data-ttu-id="8b394-115">Übergeben diese Eigenschaft an die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für das Objekt gibt eine [IMAPITable](imapitableiunknown.md) -Schnittstelle, mit der Erstellung der Tabelle anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="8b394-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="8b394-116">MAPI verwendet diese Tabelle, um die Eigenschaftenseiten für ein Address Book-Objekt als Reaktion auf einen Anruf [IAddrBook::Details](iaddrbook-details.md) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b394-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b394-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8b394-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8b394-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8b394-118">Header files</span></span>

<span data-ttu-id="8b394-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b394-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b394-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8b394-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b394-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b394-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8b394-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8b394-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b394-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b394-123">See also</span></span>



[<span data-ttu-id="8b394-124">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8b394-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="8b394-125">PidTagSearch (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8b394-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="8b394-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b394-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b394-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b394-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b394-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8b394-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b394-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8b394-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

