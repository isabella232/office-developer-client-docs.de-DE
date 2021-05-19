---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Stellt eine Instanz eines Outlook Social Connector (OSC)-Anbieters dar.
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409958"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="70b93-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="70b93-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="70b93-104">Stellt eine Instanz eines Outlook Social Connector (OSC)-Anbieters dar.</span><span class="sxs-lookup"><span data-stu-id="70b93-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="70b93-105">Elemente</span><span class="sxs-lookup"><span data-stu-id="70b93-105">Members</span></span>

<span data-ttu-id="70b93-106">In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialProvider-Schnittstelle verfügbar** sind.</span><span class="sxs-lookup"><span data-stu-id="70b93-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="70b93-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="70b93-107">**Name**</span></span>|<span data-ttu-id="70b93-108">**Membertyp**</span><span class="sxs-lookup"><span data-stu-id="70b93-108">**Member type**</span></span>|<span data-ttu-id="70b93-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70b93-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70b93-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="70b93-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="70b93-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="70b93-111">Property</span></span>  <br/> |<span data-ttu-id="70b93-112">Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den OSC-Anbieter angeben.</span><span class="sxs-lookup"><span data-stu-id="70b93-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="70b93-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="70b93-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="70b93-114">Methode</span><span class="sxs-lookup"><span data-stu-id="70b93-114">Method</span></span>  <br/> |<span data-ttu-id="70b93-115">Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md)-Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="70b93-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="70b93-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="70b93-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="70b93-117">Methode</span><span class="sxs-lookup"><span data-stu-id="70b93-117">Method</span></span>  <br/> |<span data-ttu-id="70b93-118">Ruft eine Zeichenfolge ab, die Anbieterfunktionen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="70b93-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="70b93-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="70b93-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="70b93-120">Methode</span><span class="sxs-lookup"><span data-stu-id="70b93-120">Method</span></span>  <br/> |<span data-ttu-id="70b93-121">Ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab.</span><span class="sxs-lookup"><span data-stu-id="70b93-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="70b93-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="70b93-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="70b93-123">Methode</span><span class="sxs-lookup"><span data-stu-id="70b93-123">Method</span></span>  <br/> |<span data-ttu-id="70b93-124">Diese Methode wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="70b93-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="70b93-125">Load</span><span class="sxs-lookup"><span data-stu-id="70b93-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="70b93-126">Methode</span><span class="sxs-lookup"><span data-stu-id="70b93-126">Method</span></span>  <br/> |<span data-ttu-id="70b93-127">Initialisiert den OSC-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="70b93-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="70b93-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="70b93-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="70b93-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="70b93-129">Property</span></span>  <br/> |<span data-ttu-id="70b93-130">Gibt eine GUID zurück, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="70b93-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="70b93-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="70b93-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="70b93-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="70b93-132">Property</span></span>  <br/> |<span data-ttu-id="70b93-133">Gibt ein Array von Bytes zurück, das das Symbol für das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="70b93-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="70b93-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="70b93-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="70b93-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="70b93-135">Property</span></span>  <br/> |<span data-ttu-id="70b93-136">Gibt eine Zeichenfolge zurück, die den Namen des sozialen Netzwerks darstellt.</span><span class="sxs-lookup"><span data-stu-id="70b93-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="70b93-137">Version</span><span class="sxs-lookup"><span data-stu-id="70b93-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="70b93-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="70b93-138">Property</span></span>  <br/> |<span data-ttu-id="70b93-139">Gibt eine Zeichenfolge zurück, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="70b93-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70b93-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70b93-140">Remarks</span></span>

<span data-ttu-id="70b93-141">Ein OSC-Anbieter muss diese Schnittstelle implementieren, um mit dem OSC zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="70b93-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="70b93-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70b93-142">See also</span></span>

- [<span data-ttu-id="70b93-143">Outlook Social Connector Provider Interfaces</span><span class="sxs-lookup"><span data-stu-id="70b93-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

