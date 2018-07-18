---
title: PidTagIdentityEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e724cc727292158fab26495e5d627b42dfe00daa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794450"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="b6f98-103">PidTagIdentityEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b6f98-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b6f98-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6f98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6f98-105">Enthält die Eintrags-ID für einen Dienstanbieter Identität in einem messaging-System angegeben.</span><span class="sxs-lookup"><span data-stu-id="b6f98-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6f98-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b6f98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6f98-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b6f98-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="b6f98-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="b6f98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6f98-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="b6f98-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="b6f98-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b6f98-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6f98-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b6f98-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b6f98-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b6f98-112">Area:</span></span>  <br/> |<span data-ttu-id="b6f98-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="b6f98-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6f98-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6f98-114">Remarks</span></span>

<span data-ttu-id="b6f98-115">Diese Eigenschaft wird nicht als eine Eigenschaft für jedes Objekt, sondern nur als eine Spalte in einer Statustabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6f98-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="b6f98-116">Es ist Teil der Identität des Dienstanbieters die Tabellenzeile Status verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="b6f98-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="b6f98-117">Identität des Anbieters in der Regel zu ihrer Firma auf dem Server verweist, doch verweisen auf eine beliebige Darstellung, die der Anbieter innerhalb der messaging-System definiert.</span><span class="sxs-lookup"><span data-stu-id="b6f98-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="b6f98-118">Diese Eigenschaft gibt wird häufig auf die entsprechende Adresse Adressbuch Eintrags-ID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b6f98-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="b6f98-119">Ein Dienstanbieter, die die Eigenschaften Identity Einrichtung sollte alle diese sind.</span><span class="sxs-lookup"><span data-stu-id="b6f98-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="b6f98-120">Anbieter, die den Dienst angehören, sollte die gleichen Werte für die Identitätseigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="b6f98-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b6f98-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b6f98-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b6f98-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b6f98-122">Header files</span></span>

<span data-ttu-id="b6f98-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6f98-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6f98-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b6f98-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6f98-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6f98-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b6f98-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b6f98-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6f98-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6f98-127">See also</span></span>



[<span data-ttu-id="b6f98-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="b6f98-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="b6f98-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6f98-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6f98-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6f98-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6f98-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b6f98-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6f98-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b6f98-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

