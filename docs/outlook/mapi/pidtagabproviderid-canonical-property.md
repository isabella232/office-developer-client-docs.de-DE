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
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422243"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="98dee-103">PidTagAbProviderId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="98dee-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="98dee-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98dee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98dee-105">Enthält die [MAPIUID-Struktur](mapiuid.md) eines Adressbuchanbieters.</span><span class="sxs-lookup"><span data-stu-id="98dee-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98dee-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="98dee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98dee-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="98dee-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="98dee-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="98dee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98dee-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="98dee-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="98dee-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="98dee-110">Data type:</span></span>  <br/> |<span data-ttu-id="98dee-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="98dee-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="98dee-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="98dee-112">Area:</span></span>  <br/> |<span data-ttu-id="98dee-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="98dee-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98dee-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98dee-114">Remarks</span></span>

<span data-ttu-id="98dee-115">Die **MAPIUID-Struktur** gibt an, welcher Adressbuchanbieter diesen bestimmten Container in der Containerhierarchie liefert.</span><span class="sxs-lookup"><span data-stu-id="98dee-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="98dee-116">Der Wert ist für jeden Anbieter eindeutig.</span><span class="sxs-lookup"><span data-stu-id="98dee-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="98dee-117">Ein Adressbuchanbieter kann mehrere Bezeichner bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="98dee-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="98dee-118">Beispielsweise kann ein Anbieter, der zwei verschiedene Container liefert, **PR_AB_PROVIDER_ID** eindeutige Bezeichner für jeden Container veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="98dee-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="98dee-119">**PR_AB_PROVIDER_ID** entspricht der **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) -Eigenschaft für Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="98dee-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="98dee-120">Clientanwendungen können **PR_AB_PROVIDER_ID** zum Suchen verwandter Zeilen in einer Adressbuchhierarchietabelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="98dee-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98dee-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="98dee-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="98dee-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="98dee-122">Header files</span></span>

<span data-ttu-id="98dee-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98dee-123">Mapitags.h</span></span>
  
> <span data-ttu-id="98dee-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="98dee-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="98dee-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98dee-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="98dee-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="98dee-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98dee-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98dee-127">See also</span></span>



[<span data-ttu-id="98dee-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="98dee-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="98dee-129">PidTagStoreProvider (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="98dee-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="98dee-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="98dee-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98dee-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="98dee-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98dee-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="98dee-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

