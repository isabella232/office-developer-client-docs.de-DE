---
title: PidTagIdentitySearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12226039457782162eb74a19713fa77936332f80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565144"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="07e10-103">PidTagIdentitySearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="07e10-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="07e10-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07e10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07e10-105">Enthält den Search-Schlüssel für einen Dienstanbieter Identität in einem messaging-System angegeben.</span><span class="sxs-lookup"><span data-stu-id="07e10-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07e10-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="07e10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07e10-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="07e10-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="07e10-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="07e10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07e10-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="07e10-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="07e10-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="07e10-110">Data type:</span></span>  <br/> |<span data-ttu-id="07e10-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="07e10-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="07e10-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="07e10-112">Area:</span></span>  <br/> |<span data-ttu-id="07e10-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="07e10-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07e10-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="07e10-114">Remarks</span></span>

<span data-ttu-id="07e10-115">Diese Eigenschaft wird nicht als eine Eigenschaft für jedes Objekt, sondern nur als eine Spalte in einer Statustabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07e10-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="07e10-116">Es ist Teil der Identität des Dienstanbieters die Tabellenzeile Status verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="07e10-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="07e10-117">Identität des Anbieters in der Regel zu ihrer Firma auf dem Server verweist, doch verweisen auf eine beliebige Darstellung, die der Anbieter innerhalb der messaging-System definiert.</span><span class="sxs-lookup"><span data-stu-id="07e10-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="07e10-118">Ein Dienstanbieter, die die Eigenschaften Identity Einrichtung sollte alle diese sind.</span><span class="sxs-lookup"><span data-stu-id="07e10-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="07e10-119">Anbieter, die den Dienst angehören, sollte die gleichen Werte für die Identitätseigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="07e10-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="07e10-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="07e10-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="07e10-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="07e10-121">Header files</span></span>

<span data-ttu-id="07e10-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07e10-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="07e10-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="07e10-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="07e10-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="07e10-124">Mapitags.h</span></span>
  
> <span data-ttu-id="07e10-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="07e10-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07e10-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07e10-126">See also</span></span>



[<span data-ttu-id="07e10-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="07e10-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="07e10-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07e10-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07e10-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07e10-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07e10-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="07e10-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07e10-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="07e10-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

