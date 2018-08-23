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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8810b6c39b909ebaa612496824150499cd15165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584842"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="e7662-103">PidTagIdentityEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7662-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e7662-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7662-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7662-105">Enthält die Eintrags-ID für einen Dienstanbieter Identität in einem messaging-System angegeben.</span><span class="sxs-lookup"><span data-stu-id="e7662-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7662-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e7662-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7662-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e7662-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e7662-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e7662-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7662-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="e7662-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="e7662-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e7662-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7662-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e7662-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e7662-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e7662-112">Area:</span></span>  <br/> |<span data-ttu-id="e7662-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="e7662-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7662-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e7662-114">Remarks</span></span>

<span data-ttu-id="e7662-115">Diese Eigenschaft wird nicht als eine Eigenschaft für jedes Objekt, sondern nur als eine Spalte in einer Statustabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7662-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="e7662-116">Es ist Teil der Identität des Dienstanbieters die Tabellenzeile Status verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e7662-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="e7662-117">Identität des Anbieters in der Regel zu ihrer Firma auf dem Server verweist, doch verweisen auf eine beliebige Darstellung, die der Anbieter innerhalb der messaging-System definiert.</span><span class="sxs-lookup"><span data-stu-id="e7662-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="e7662-118">Diese Eigenschaft gibt wird häufig auf die entsprechende Adresse Adressbuch Eintrags-ID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e7662-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="e7662-119">Ein Dienstanbieter, die die Eigenschaften Identity Einrichtung sollte alle diese sind.</span><span class="sxs-lookup"><span data-stu-id="e7662-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="e7662-120">Anbieter, die den Dienst angehören, sollte die gleichen Werte für die Identitätseigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e7662-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e7662-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7662-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e7662-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e7662-122">Header files</span></span>

<span data-ttu-id="e7662-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7662-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7662-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e7662-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7662-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7662-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e7662-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e7662-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7662-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7662-127">See also</span></span>



[<span data-ttu-id="e7662-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="e7662-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="e7662-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7662-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7662-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7662-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7662-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e7662-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7662-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e7662-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

