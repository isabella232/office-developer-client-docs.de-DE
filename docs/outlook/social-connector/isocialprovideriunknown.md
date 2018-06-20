---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Stellt eine Instanz eines Anbieters Outlook Social Connector (OSC).
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796102"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="0df0d-103">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0df0d-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="0df0d-104">Stellt eine Instanz eines Anbieters Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="0df0d-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="0df0d-105">Members</span><span class="sxs-lookup"><span data-stu-id="0df0d-105">Members</span></span>

<span data-ttu-id="0df0d-106">In der folgenden Tabelle werden die Member, die für die **ISocialProvider** -Schnittstelle verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="0df0d-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="0df0d-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="0df0d-107">**Name**</span></span>|<span data-ttu-id="0df0d-108">**Typ des Elements**</span><span class="sxs-lookup"><span data-stu-id="0df0d-108">**Member type**</span></span>|<span data-ttu-id="0df0d-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0df0d-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0df0d-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="0df0d-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="0df0d-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0df0d-111">Property</span></span>  <br/> |<span data-ttu-id="0df0d-112">Gibt ein Array von Zeichenfolgen, die Website-URLs für den OSC-Anbieter angeben.</span><span class="sxs-lookup"><span data-stu-id="0df0d-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="0df0d-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="0df0d-114">Methode</span><span class="sxs-lookup"><span data-stu-id="0df0d-114">Method</span></span>  <br/> |<span data-ttu-id="0df0d-115">Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0df0d-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="0df0d-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="0df0d-117">Methode</span><span class="sxs-lookup"><span data-stu-id="0df0d-117">Method</span></span>  <br/> |<span data-ttu-id="0df0d-118">Ruft eine Zeichenfolge, die vom Anbieterfunktionen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0df0d-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="0df0d-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="0df0d-120">Methode</span><span class="sxs-lookup"><span data-stu-id="0df0d-120">Method</span></span>  <br/> |<span data-ttu-id="0df0d-121">Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0df0d-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="0df0d-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="0df0d-123">Methode</span><span class="sxs-lookup"><span data-stu-id="0df0d-123">Method</span></span>  <br/> |<span data-ttu-id="0df0d-124">Diese Methode wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0df0d-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-125">Load</span><span class="sxs-lookup"><span data-stu-id="0df0d-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="0df0d-126">Methode</span><span class="sxs-lookup"><span data-stu-id="0df0d-126">Method</span></span>  <br/> |<span data-ttu-id="0df0d-127">Initialisiert den OSC-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="0df0d-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="0df0d-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="0df0d-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0df0d-129">Property</span></span>  <br/> |<span data-ttu-id="0df0d-130">Gibt eine GUID, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="0df0d-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="0df0d-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="0df0d-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0df0d-132">Property</span></span>  <br/> |<span data-ttu-id="0df0d-133">Gibt ein Array von Bytes, die das Symbol für das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="0df0d-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="0df0d-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="0df0d-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0df0d-135">Property</span></span>  <br/> |<span data-ttu-id="0df0d-136">Gibt eine Zeichenfolge, die den Namen für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="0df0d-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="0df0d-137">Version</span><span class="sxs-lookup"><span data-stu-id="0df0d-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="0df0d-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0df0d-138">Property</span></span>  <br/> |<span data-ttu-id="0df0d-139">Gibt eine Zeichenfolge, die die Versionsnummer des Anbieters für diese für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="0df0d-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0df0d-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0df0d-140">Remarks</span></span>

<span data-ttu-id="0df0d-141">Ein OSC-Anbieter muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.</span><span class="sxs-lookup"><span data-stu-id="0df0d-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0df0d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0df0d-142">See also</span></span>

- [<span data-ttu-id="0df0d-143">Outlook Connector für soziale Netzwerke Provider-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0df0d-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

