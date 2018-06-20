---
title: Kanonische PidTagStoreProvider-Eigenschaft
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
ms.openlocfilehash: b634f815d2aedecc716227c6525b846db38ca869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795216"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="f3346-103">Kanonische PidTagStoreProvider-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f3346-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="f3346-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3346-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3346-105">Enthält eine vom Anbieter definiertes [MAPIUID](mapiuid.md) -Struktur, die den Typ des Nachrichtenspeichers angibt.</span><span class="sxs-lookup"><span data-stu-id="f3346-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3346-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f3346-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3346-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="f3346-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="f3346-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="f3346-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3346-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="f3346-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="f3346-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f3346-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3346-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f3346-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f3346-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f3346-112">Area:</span></span>  <br/> |<span data-ttu-id="f3346-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3346-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3346-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3346-114">Remarks</span></span>

<span data-ttu-id="f3346-115">Die Struktur [MAPIUID](mapiuid.md) identifiziert den Typ des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="f3346-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="f3346-116">Der Wert ist Zeichenfolgeneigenschaften Nachricht auf Message Store Objekte berechnet und für jeden Anbieter eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="f3346-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="f3346-117">Es wird normalerweise zum Durchsuchen der Nachricht Store-Tabelle verwendet, um einen Speicher mit den gewünschten Typ, wie Öffentliche Ordner zu finden.</span><span class="sxs-lookup"><span data-stu-id="f3346-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="f3346-118">Diese Eigenschaft entspricht der **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md))-Eigenschaft für Adressbücher.</span><span class="sxs-lookup"><span data-stu-id="f3346-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f3346-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f3346-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f3346-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f3346-120">Header files</span></span>

<span data-ttu-id="f3346-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3346-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3346-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f3346-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3346-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3346-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f3346-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f3346-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3346-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3346-125">See also</span></span>



[<span data-ttu-id="f3346-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3346-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3346-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3346-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3346-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f3346-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3346-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f3346-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

