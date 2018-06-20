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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792776"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="54ebc-103">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="54ebc-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="54ebc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54ebc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54ebc-105">Funktioniert mit-Dienstanbieter in einem Message-Dienst.</span><span class="sxs-lookup"><span data-stu-id="54ebc-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54ebc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="54ebc-106">Header file:</span></span>  <br/> |<span data-ttu-id="54ebc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54ebc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="54ebc-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="54ebc-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="54ebc-109">Verwaltungsobjekte Anbieter</span><span class="sxs-lookup"><span data-stu-id="54ebc-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="54ebc-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="54ebc-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="54ebc-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="54ebc-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="54ebc-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="54ebc-112">Called by:</span></span>  <br/> |<span data-ttu-id="54ebc-113">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="54ebc-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="54ebc-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="54ebc-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="54ebc-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="54ebc-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="54ebc-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="54ebc-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="54ebc-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="54ebc-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="54ebc-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="54ebc-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="54ebc-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="54ebc-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="54ebc-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält, die für den Anbieter Verwaltungsobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="54ebc-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="54ebc-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="54ebc-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="54ebc-122">Bietet Zugriff auf den Dienst Anbieter Tabelle, eine Liste der Dienstanbieter in der Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="54ebc-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="54ebc-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="54ebc-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="54ebc-124">Fügt einen Dienstanbieter an den Dienst.</span><span class="sxs-lookup"><span data-stu-id="54ebc-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="54ebc-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="54ebc-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="54ebc-126">Löscht einen Dienstanbieter aus der Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="54ebc-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="54ebc-127">"OpenProfileSection"</span><span class="sxs-lookup"><span data-stu-id="54ebc-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="54ebc-128">Öffnet einen Profilabschnitt aus dem aktuellen Profil, und gibt einen [IProfSect](iprofsectimapiprop.md) Zeiger für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="54ebc-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54ebc-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54ebc-129">Remarks</span></span>

<span data-ttu-id="54ebc-130">Clients können einen Zeiger auf eine **IProviderAdmin** -Schnittstelle abrufen, indem Sie die [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) -Methode aufrufen; Dienstanbieter sind ein **IProviderAdmin** -Zeiger übergeben, wenn ihre Messagingdiensts Entry Point-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54ebc-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54ebc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54ebc-131">See also</span></span>



[<span data-ttu-id="54ebc-132">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="54ebc-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

