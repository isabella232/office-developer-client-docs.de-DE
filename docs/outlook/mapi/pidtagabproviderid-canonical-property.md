---
title: PidTagAbProviderId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794024"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="98c4d-103">PidTagAbProviderId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="98c4d-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="98c4d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98c4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98c4d-105">Enthält ein Adressbuchanbieter [MAPIUID](mapiuid.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="98c4d-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98c4d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="98c4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98c4d-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="98c4d-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="98c4d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="98c4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98c4d-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="98c4d-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="98c4d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="98c4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="98c4d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="98c4d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="98c4d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="98c4d-112">Area:</span></span>  <br/> |<span data-ttu-id="98c4d-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="98c4d-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98c4d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98c4d-114">Remarks</span></span>

<span data-ttu-id="98c4d-115">Die Struktur **MAPIUID** identifiziert, welche Adressbuchanbieter diesem Container in der Containerhierarchie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="98c4d-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="98c4d-116">Der Wert ist für jeden Anbieter eindeutig.</span><span class="sxs-lookup"><span data-stu-id="98c4d-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="98c4d-117">Adressbuch-Dienstanbieter kann mehrere Bezeichner bereit.</span><span class="sxs-lookup"><span data-stu-id="98c4d-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="98c4d-118">Beispielsweise kann ein Anbieter, der zwei verschiedene Container liefert in **PR_AB_PROVIDER_ID** eindeutigen Bezeichnern für jeden Container veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="98c4d-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="98c4d-119">**PR_AB_PROVIDER_ID** ist vergleichbar mit der **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))-Eigenschaft für Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="98c4d-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="98c4d-120">Clientanwendungen können **PR_AB_PROVIDER_ID** um verwandte Zeilen in einer Address Book Hierarchie-Tabelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="98c4d-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98c4d-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="98c4d-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="98c4d-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="98c4d-122">Header files</span></span>

<span data-ttu-id="98c4d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98c4d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="98c4d-124">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="98c4d-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="98c4d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98c4d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="98c4d-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="98c4d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98c4d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98c4d-127">See also</span></span>



[<span data-ttu-id="98c4d-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="98c4d-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="98c4d-129">PidTagStoreProvider (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="98c4d-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="98c4d-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98c4d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98c4d-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="98c4d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98c4d-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="98c4d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

