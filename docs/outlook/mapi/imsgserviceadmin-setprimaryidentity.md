---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792615"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="6face-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="6face-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="6face-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6face-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6face-105">Legt eine Message Service hat der Hersteller der primäre Identität für das Profil sein.</span><span class="sxs-lookup"><span data-stu-id="6face-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="6face-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6face-106">Parameters</span></span>

 <span data-ttu-id="6face-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="6face-107">_lpUID_</span></span>
  
> <span data-ttu-id="6face-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Dienst angeben die primäre Identität enthält, oder NULL, gibt an, dass die aktuelle Identität **SetPrimaryIdentity** gelöscht werden sollte.</span><span class="sxs-lookup"><span data-stu-id="6face-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="6face-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6face-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6face-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="6face-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6face-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6face-111">Return value</span></span>

<span data-ttu-id="6face-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="6face-112">S_OK</span></span> 
  
> <span data-ttu-id="6face-113">Der Nachrichtendienst wurde erfolgreich hat den Hersteller der primären Identität zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6face-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="6face-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6face-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6face-115">**SetPrimaryIdentity** wurde versucht, eine Message Service angeben, die das SERVICE_NO_PRIMARY_IDENTITY-Flag, das in der **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="6face-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6face-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6face-116">Remarks</span></span>

<span data-ttu-id="6face-117">Die Methode **IMsgServiceAdmin::SetPrimaryIdentity** richtet einen Nachrichtendienst zur als hat der Hersteller der primäre Identität für das Profil.</span><span class="sxs-lookup"><span data-stu-id="6face-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="6face-118">Die primäre Identität ist in der Regel der Benutzer, die den Dienst angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="6face-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="6face-119">Es wird durch drei Eigenschaften dargestellt:</span><span class="sxs-lookup"><span data-stu-id="6face-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="6face-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6face-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="6face-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6face-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="6face-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6face-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="6face-123">Jeder Dienstanbieter in der festgelegten Messagingdiensts wird diese drei Eigenschaften auf die Anzeigenamen sowie die Eintrags-ID und Suche Schlüssel des Benutzers messaging, das die primäre Identität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6face-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="6face-124">Clients können die primäre Identität Eintrags-ID abrufen, durch die [IMAPISession::QueryIdentity](imapisession-queryidentity.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6face-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="6face-125">Die **PR_RESOURCE_FLAGS** -Eigenschaft wird festgelegt, um STATUS_PRIMARY_IDENTITY für die einzelnen Anbieter, die den Dienst gehört, das die primäre Identität bereitstellt und SERVICE_PRIMARY_IDENTITY für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="6face-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="6face-126">Bei ein Dienstanbieter die primäre Identität für die Message-Dienst angegeben werden kann, wird es auf STATUS_NO_PRIMARY_IDENTITY **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="6face-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="6face-127">**SetPrimaryIdentity** wird die **PR_RESOURCE_FLAGS** -Eigenschaft der einzelnen Nachricht-Dienste, die nicht der primäre Identitätswert SERVICE_NO_PRIMARY_IDENTITY bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6face-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="6face-128">Jeder Nachricht-Dienstanbieter, die MAPI Informationen zu verfügt kann beim Anmelden eines Clients mit dem Dienst auf eine Identität für jeden Benutzer einrichten.</span><span class="sxs-lookup"><span data-stu-id="6face-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="6face-129">Da MAPI-Verbindungen mit mehreren Dienstanbieter für jede MAPI-Sitzung unterstützt, ist es jedoch keine feste Definition der Identität eines bestimmten Benutzers für die MAPI-Sitzung als Ganzes. Identität des Benutzers, hängt davon ab, welcher Dienst beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="6face-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="6face-130">Clients können **SetPrimaryIdentity** zum Bestimmen von einer der vielen Identitäten eingerichtet für einen Benutzer von den Diensten für die Nachricht als primäre Identität für diesen Benutzer aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6face-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6face-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6face-131">See also</span></span>



[<span data-ttu-id="6face-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="6face-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="6face-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6face-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="6face-134">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6face-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

