---
title: Kanonische Pidtagidentityentryid (-Eigenschaft
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
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423335"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="1fd16-103">Kanonische Pidtagidentityentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1fd16-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1fd16-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fd16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fd16-105">Enthält die Eintrags-ID für die Identität eines Dienstanbieters gemäß der Definition in einem Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="1fd16-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fd16-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1fd16-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fd16-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1fd16-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1fd16-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1fd16-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1fd16-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="1fd16-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="1fd16-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1fd16-110">Data type:</span></span>  <br/> |<span data-ttu-id="1fd16-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1fd16-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1fd16-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1fd16-112">Area:</span></span>  <br/> |<span data-ttu-id="1fd16-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="1fd16-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fd16-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fd16-114">Remarks</span></span>

<span data-ttu-id="1fd16-115">Diese Eigenschaft wird nicht als Eigenschaft für ein Objekt, sondern nur als Spalte in einer Statustabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1fd16-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="1fd16-116">Sie ist Teil der Identität des Dienstanbieters, der die Zeile der Statustabelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="1fd16-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="1fd16-117">Die Identität des Anbieters bezieht sich in der Regel auf sein Konto auf dem Server, kann jedoch auf eine beliebige Darstellung verweisen, die der Anbieter innerhalb des Messagingsystems definiert.</span><span class="sxs-lookup"><span data-stu-id="1fd16-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="1fd16-118">Diese Eigenschaft wird häufig auf die entsprechende Adressbucheintrags-ID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1fd16-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="1fd16-119">Ein Dienstanbieter, der eine beliebige Identitätseigenschaft bereit liefert, sollte alle Bereitstellung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1fd16-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="1fd16-120">Anbieter, die zum gleichen Nachrichtendienst gehören, sollten dieselben Werte für die Identitätseigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="1fd16-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1fd16-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1fd16-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1fd16-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="1fd16-122">Header files</span></span>

<span data-ttu-id="1fd16-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1fd16-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fd16-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="1fd16-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1fd16-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1fd16-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1fd16-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1fd16-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1fd16-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fd16-127">See also</span></span>



[<span data-ttu-id="1fd16-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="1fd16-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="1fd16-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fd16-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fd16-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fd16-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fd16-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1fd16-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fd16-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1fd16-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

