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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317360"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="778ac-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="778ac-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="778ac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="778ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="778ac-105">Legt fest, dass ein Nachrichtendienst der Lieferant der primären Identität für das Profil ist.</span><span class="sxs-lookup"><span data-stu-id="778ac-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="778ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="778ac-106">Parameters</span></span>

 <span data-ttu-id="778ac-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="778ac-107">_lpUID_</span></span>
  
> <span data-ttu-id="778ac-108">in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Nachrichtendienst enthält, um die primäre Identität anzugeben, oder NULL, die angibt, dass **SetPrimaryIdentity** die aktuelle Identität löschen soll.</span><span class="sxs-lookup"><span data-stu-id="778ac-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="778ac-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="778ac-109">_ulFlags_</span></span>
  
> <span data-ttu-id="778ac-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="778ac-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="778ac-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="778ac-111">Return value</span></span>

<span data-ttu-id="778ac-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="778ac-112">S_OK</span></span> 
  
> <span data-ttu-id="778ac-113">Dem Nachrichtendienst wurde der Lieferant mit der primären Identität erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="778ac-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="778ac-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="778ac-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="778ac-115">**SetPrimaryIdentity** hat versucht, einen Nachrichtendienst mit dem SERVICE_NO_PRIMARY_IDENTITY-Flag in seiner **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="778ac-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="778ac-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="778ac-116">Remarks</span></span>

<span data-ttu-id="778ac-117">Die **IMsgServiceAdmin:: SetPrimaryIdentity** -Methode richtet einen Nachrichtendienst als Anbieter der primären Identität für das Profil ein.</span><span class="sxs-lookup"><span data-stu-id="778ac-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="778ac-118">Die primäre Identität ist in der Regel der Benutzer, der beim Nachrichtendienst angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="778ac-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="778ac-119">Es wird durch drei Eigenschaften dargestellt:</span><span class="sxs-lookup"><span data-stu-id="778ac-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="778ac-120">**PR_IDENTITY_DISPLAY** ([Pidtagidentitydisplay (](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="778ac-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="778ac-121">**PR_IDENTITY_ENTRYID** ([Pidtagidentityentryid (](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="778ac-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="778ac-122">**PR_IDENTITY_SEARCH_KEY** ([Pidtagidentitysearchkey (](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="778ac-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="778ac-123">Jeder Dienstanbieter im angegebenen Nachrichtendienst legt diese drei Eigenschaften auf den Anzeigenamen, die Eintrags-ID und den Suchschlüssel des Messaging Benutzers fest, der die primäre Identität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="778ac-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="778ac-124">Clients können die Eintrags-ID der primären Identität abrufen, indem Sie die [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="778ac-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="778ac-125">Die **PR_RESOURCE_FLAGS** -Eigenschaft wird für jeden Anbieter, der ein Mitglied des Nachrichtendiensts ist, der die primäre Identität bereitstellt, und SERVICE_PRIMARY_IDENTITY für den Nachrichtendienst auf STATUS_PRIMARY_IDENTITY festgelegt.</span><span class="sxs-lookup"><span data-stu-id="778ac-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="778ac-126">Wenn ein Dienstanbieter die primäre Identität für seinen Nachrichtendienst nicht angeben kann, wird **PR_RESOURCE_FLAGS** auf STATUS_NO_PRIMARY_IDENTITY festgelegt.</span><span class="sxs-lookup"><span data-stu-id="778ac-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="778ac-127">**SetPrimaryIdentity** legt die **PR_RESOURCE_FLAGS** -Eigenschaft der einzelnen Nachrichtendienste fest, die nicht die primäre Identität für SERVICE_NO_PRIMARY_IDENTITY bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="778ac-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="778ac-128">Jeder Nachrichtendienst Anbieter, über den MAPI Informationen enthält, kann für jeden seiner Benutzer eine Identität festlegen, wenn sich ein Client beim Dienst anmeldet.</span><span class="sxs-lookup"><span data-stu-id="778ac-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="778ac-129">Da MAPI jedoch Verbindungen mit mehreren Dienstanbietern für jede MAPI-Sitzung unterstützt, gibt es keine feste Definition der Identität eines bestimmten Benutzers für die MAPI-Sitzung als Ganzes; die Identität eines Benutzers hängt davon ab, welcher Dienst beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="778ac-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="778ac-130">Clients können **SetPrimaryIdentity** aufrufen, um eine der vielen Identitäten festzulegen, die von Nachrichtendiensten für einen Benutzer als primäre Identität für diesen Benutzer erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="778ac-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="778ac-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="778ac-131">See also</span></span>



[<span data-ttu-id="778ac-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="778ac-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="778ac-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="778ac-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="778ac-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="778ac-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

