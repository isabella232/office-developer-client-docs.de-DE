---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437532"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="fd84d-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd84d-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="fd84d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd84d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd84d-105">Funktioniert mit Dienstanbietern in einem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="fd84d-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd84d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fd84d-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd84d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd84d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fd84d-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="fd84d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="fd84d-109">Anbieterverwaltungsobjekte</span><span class="sxs-lookup"><span data-stu-id="fd84d-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="fd84d-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="fd84d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="fd84d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="fd84d-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="fd84d-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fd84d-112">Called by:</span></span>  <br/> |<span data-ttu-id="fd84d-113">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fd84d-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="fd84d-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="fd84d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fd84d-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="fd84d-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="fd84d-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="fd84d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="fd84d-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="fd84d-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fd84d-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="fd84d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="fd84d-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="fd84d-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="fd84d-120">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Anbieterverwaltungsobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fd84d-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="fd84d-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="fd84d-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="fd84d-122">Bietet Zugriff auf die Anbietertabelle des Nachrichtendiensts, eine Liste der Dienstanbieter im Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="fd84d-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="fd84d-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="fd84d-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="fd84d-124">Fügt dem Nachrichtendienst einen Dienstanbieter hinzu.</span><span class="sxs-lookup"><span data-stu-id="fd84d-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="fd84d-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="fd84d-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="fd84d-126">Löscht einen Dienstanbieter aus dem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="fd84d-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="fd84d-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="fd84d-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="fd84d-128">Öffnet einen Profilabschnitt aus dem aktuellen Profil und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="fd84d-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd84d-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd84d-129">Remarks</span></span>

<span data-ttu-id="fd84d-130">Clients können einen Zeiger auf eine **IProviderAdmin-Schnittstelle** durch Aufrufen der [IMsgServiceAdmin::AdminProviders-Methode](imsgserviceadmin-adminproviders.md) erhalten. Dienstanbietern wird ein **IProviderAdmin-Zeiger** übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fd84d-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd84d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd84d-131">See also</span></span>



[<span data-ttu-id="fd84d-132">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fd84d-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

