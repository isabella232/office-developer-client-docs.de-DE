---
title: Kanonische PidTagDetailsTable-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794301"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="54dd1-103">Kanonische PidTagDetailsTable-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="54dd1-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="54dd1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54dd1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54dd1-105">Enthält eine eingebettete Anzeige Table-Objekt.</span><span class="sxs-lookup"><span data-stu-id="54dd1-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54dd1-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="54dd1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54dd1-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="54dd1-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="54dd1-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="54dd1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54dd1-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="54dd1-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="54dd1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="54dd1-110">Data type:</span></span>  <br/> |<span data-ttu-id="54dd1-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="54dd1-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="54dd1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="54dd1-112">Area:</span></span>  <br/> |<span data-ttu-id="54dd1-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="54dd1-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54dd1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54dd1-114">Remarks</span></span>

<span data-ttu-id="54dd1-115">Übergeben diese Eigenschaft an die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für das Objekt gibt eine [IMAPITable](imapitableiunknown.md) -Schnittstelle, mit der Erstellung der Tabelle anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="54dd1-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="54dd1-116">MAPI verwendet diese Tabelle, um die Eigenschaftenseiten für ein Address Book-Objekt als Reaktion auf einen Anruf [IAddrBook::Details](iaddrbook-details.md) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54dd1-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="54dd1-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="54dd1-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="54dd1-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="54dd1-118">Header files</span></span>

<span data-ttu-id="54dd1-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54dd1-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="54dd1-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="54dd1-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="54dd1-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="54dd1-121">Mapitags.h</span></span>
  
> <span data-ttu-id="54dd1-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="54dd1-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54dd1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54dd1-123">See also</span></span>



[<span data-ttu-id="54dd1-124">Kanonische PidTagCreateTemplates-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="54dd1-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="54dd1-125">Kanonische PidTagSearch-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="54dd1-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="54dd1-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54dd1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54dd1-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54dd1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54dd1-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="54dd1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54dd1-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="54dd1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

