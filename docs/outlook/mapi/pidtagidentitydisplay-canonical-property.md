---
title: Kanonische Pidtagidentitydisplay (-Eigenschaft
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
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327951"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="27d93-103">Kanonische Pidtagidentitydisplay (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="27d93-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="27d93-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27d93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27d93-105">Enthält den Anzeigenamen für die Identität eines Dienstanbieters gemäß der Definition in einem Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="27d93-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27d93-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="27d93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27d93-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="27d93-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="27d93-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="27d93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27d93-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="27d93-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="27d93-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="27d93-110">Data type:</span></span>  <br/> |<span data-ttu-id="27d93-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="27d93-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="27d93-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="27d93-112">Area:</span></span>  <br/> |<span data-ttu-id="27d93-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="27d93-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27d93-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27d93-114">Remarks</span></span>

<span data-ttu-id="27d93-115">Diese Eigenschaften werden nicht als Eigenschaften für ein Objekt, sondern nur als Spalte in einer Statustabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27d93-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="27d93-116">Sie ist Teil der Identität des Dienstanbieters, der die Zeile der Statustabelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="27d93-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="27d93-117">Die Identität des Anbieters bezieht sich in der Regel auf sein Konto auf dem Server, kann jedoch auf eine beliebige Darstellung verweisen, die der Anbieter innerhalb des Messagingsystems definiert.</span><span class="sxs-lookup"><span data-stu-id="27d93-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="27d93-118">Ein Dienstanbieter, der eine beliebige Identitätseigenschaft bereit liefert, sollte alle Bereitstellung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="27d93-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="27d93-119">Anbieter, die zum gleichen Nachrichtendienst gehören, sollten dieselben Werte für die Identitätseigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="27d93-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="27d93-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="27d93-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="27d93-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="27d93-121">Header files</span></span>

<span data-ttu-id="27d93-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="27d93-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="27d93-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="27d93-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="27d93-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="27d93-124">Mapitags.h</span></span>
  
> <span data-ttu-id="27d93-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="27d93-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27d93-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27d93-126">See also</span></span>



[<span data-ttu-id="27d93-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="27d93-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="27d93-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27d93-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27d93-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27d93-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27d93-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="27d93-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27d93-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="27d93-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

