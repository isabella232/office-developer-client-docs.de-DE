---
title: Kanonische Pidtagstoreprovider (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278708"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="2be7d-103">Kanonische Pidtagstoreprovider (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2be7d-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="2be7d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2be7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2be7d-105">Enthält eine vom Anbieter definierte [MAPIUID](mapiuid.md) -Struktur, die den Typ des Nachrichtenspeichers angibt.</span><span class="sxs-lookup"><span data-stu-id="2be7d-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2be7d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2be7d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2be7d-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="2be7d-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="2be7d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2be7d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2be7d-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="2be7d-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="2be7d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2be7d-110">Data type:</span></span>  <br/> |<span data-ttu-id="2be7d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2be7d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2be7d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2be7d-112">Area:</span></span>  <br/> |<span data-ttu-id="2be7d-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2be7d-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2be7d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2be7d-114">Remarks</span></span>

<span data-ttu-id="2be7d-115">Die [MAPIUID](mapiuid.md) -Struktur gibt den Typ des Nachrichtenspeichers an.</span><span class="sxs-lookup"><span data-stu-id="2be7d-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="2be7d-116">Der Wert wird von Nachrichtenspeicher Anbietern auf Nachrichtenspeicher Objekten berechnet und ist für jeden Anbieter eindeutig.</span><span class="sxs-lookup"><span data-stu-id="2be7d-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="2be7d-117">Sie wird in der Regel zum Durchsuchen der Nachrichtenspeichertabelle verwendet, um einen Speicher des gewünschten Typs zu finden, beispielsweise öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="2be7d-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="2be7d-118">Diese Eigenschaft entspricht der **PR_AB_PROVIDER_ID** ([pidtagabproviderid (](pidtagabproviderid-canonical-property.md))-Eigenschaft für Adressbücher.</span><span class="sxs-lookup"><span data-stu-id="2be7d-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2be7d-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2be7d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2be7d-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2be7d-120">Header files</span></span>

<span data-ttu-id="2be7d-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2be7d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="2be7d-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2be7d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="2be7d-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2be7d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2be7d-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2be7d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2be7d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2be7d-125">See also</span></span>



[<span data-ttu-id="2be7d-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2be7d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2be7d-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2be7d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2be7d-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2be7d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2be7d-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2be7d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

