---
title: Kanonische PidTagIdentityDisplay-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b88fc54f1db26277d8a8d5e54fcff0ae164b0eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794469"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="ba2ff-103">Kanonische PidTagIdentityDisplay-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ba2ff-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="ba2ff-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba2ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba2ff-105">Enthält den Anzeigenamen für einen Dienstanbieter Identität in einem messaging-System angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba2ff-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ba2ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba2ff-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="ba2ff-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="ba2ff-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ba2ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba2ff-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="ba2ff-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="ba2ff-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ba2ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba2ff-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ba2ff-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ba2ff-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ba2ff-112">Area:</span></span>  <br/> |<span data-ttu-id="ba2ff-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="ba2ff-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba2ff-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ba2ff-114">Remarks</span></span>

<span data-ttu-id="ba2ff-115">Diese Eigenschaften werden nicht als Eigenschaften für jedes Objekt, sondern nur als eine Spalte in einer Statustabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="ba2ff-116">Es ist Teil der Identität des Dienstanbieters die Tabellenzeile Status verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="ba2ff-117">Identität des Anbieters in der Regel zu ihrer Firma auf dem Server verweist, doch verweisen auf eine beliebige Darstellung, die der Anbieter innerhalb der messaging-System definiert.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="ba2ff-118">Ein Dienstanbieter, die die Eigenschaften Identity Einrichtung sollte alle diese sind.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="ba2ff-119">Anbieter, die den Dienst angehören, sollte die gleichen Werte für die Identitätseigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ba2ff-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba2ff-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ba2ff-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ba2ff-121">Header files</span></span>

<span data-ttu-id="ba2ff-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba2ff-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba2ff-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba2ff-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ba2ff-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ba2ff-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba2ff-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba2ff-126">See also</span></span>



[<span data-ttu-id="ba2ff-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="ba2ff-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="ba2ff-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba2ff-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba2ff-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba2ff-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba2ff-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ba2ff-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba2ff-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ba2ff-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

