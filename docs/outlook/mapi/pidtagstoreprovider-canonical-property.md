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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412051"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="1986e-103">Kanonische Pidtagstoreprovider (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1986e-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="1986e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1986e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1986e-105">Enthält eine vom Anbieter definierte [MAPIUID](mapiuid.md) -Struktur, die den Typ des Nachrichtenspeichers angibt.</span><span class="sxs-lookup"><span data-stu-id="1986e-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1986e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1986e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1986e-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="1986e-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="1986e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1986e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1986e-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="1986e-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="1986e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1986e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1986e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1986e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1986e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1986e-112">Area:</span></span>  <br/> |<span data-ttu-id="1986e-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1986e-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1986e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1986e-114">Remarks</span></span>

<span data-ttu-id="1986e-115">Die [MAPIUID](mapiuid.md) -Struktur gibt den Typ des Nachrichtenspeichers an.</span><span class="sxs-lookup"><span data-stu-id="1986e-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="1986e-116">Der Wert wird von Nachrichtenspeicher Anbietern auf Nachrichtenspeicher Objekten berechnet und ist für jeden Anbieter eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1986e-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="1986e-117">Sie wird in der Regel zum Durchsuchen der Nachrichtenspeichertabelle verwendet, um einen Speicher des gewünschten Typs zu finden, beispielsweise öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="1986e-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="1986e-118">Diese Eigenschaft entspricht der **PR_AB_PROVIDER_ID** ([pidtagabproviderid (](pidtagabproviderid-canonical-property.md))-Eigenschaft für Adressbücher.</span><span class="sxs-lookup"><span data-stu-id="1986e-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1986e-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1986e-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1986e-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="1986e-120">Header files</span></span>

<span data-ttu-id="1986e-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1986e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1986e-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="1986e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1986e-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1986e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1986e-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1986e-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1986e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1986e-125">See also</span></span>



[<span data-ttu-id="1986e-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1986e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1986e-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1986e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1986e-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1986e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1986e-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1986e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

