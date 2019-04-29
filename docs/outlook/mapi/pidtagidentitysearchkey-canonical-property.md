---
title: Kanonische Pidtagidentitysearchkey (-Eigenschaft
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
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423748"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="bc7d4-103">Kanonische Pidtagidentitysearchkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bc7d4-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="bc7d4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc7d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc7d4-105">Enthält den Suchschlüssel für die Identität eines Dienstanbieters gemäß der Definition in einem Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc7d4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bc7d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc7d4-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="bc7d4-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="bc7d4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bc7d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc7d4-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="bc7d4-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="bc7d4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bc7d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc7d4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bc7d4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bc7d4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bc7d4-112">Area:</span></span>  <br/> |<span data-ttu-id="bc7d4-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="bc7d4-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc7d4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc7d4-114">Remarks</span></span>

<span data-ttu-id="bc7d4-115">Diese Eigenschaft wird nicht als Eigenschaft für ein Objekt, sondern nur als Spalte in einer Statustabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="bc7d4-116">Sie ist Teil der Identität des Dienstanbieters, der die Zeile der Statustabelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="bc7d4-117">Die Identität des Anbieters bezieht sich in der Regel auf sein Konto auf dem Server, kann jedoch auf eine beliebige Darstellung verweisen, die der Anbieter innerhalb des Messagingsystems definiert.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="bc7d4-118">Ein Dienstanbieter, der eine beliebige Identitätseigenschaft bereit liefert, sollte alle Bereitstellung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="bc7d4-119">Anbieter, die zum gleichen Nachrichtendienst gehören, sollten dieselben Werte für die Identitätseigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bc7d4-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bc7d4-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bc7d4-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bc7d4-121">Header files</span></span>

<span data-ttu-id="bc7d4-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bc7d4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc7d4-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc7d4-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bc7d4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="bc7d4-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc7d4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc7d4-126">See also</span></span>



[<span data-ttu-id="bc7d4-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="bc7d4-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="bc7d4-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc7d4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc7d4-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc7d4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc7d4-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bc7d4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc7d4-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bc7d4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

