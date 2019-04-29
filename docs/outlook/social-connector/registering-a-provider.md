---
title: Registrieren eines Providers
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: In diesem Thema werden die Windows-Registrierungsspeicherorte beschrieben, die bei der Installation eines Outlook Social Connector-Anbieters (OSC) verwendet werden.
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421760"
---
# <a name="registering-a-provider"></a><span data-ttu-id="113eb-103">Registrieren eines Providers</span><span class="sxs-lookup"><span data-stu-id="113eb-103">Registering a provider</span></span>

<span data-ttu-id="113eb-104">In diesem Thema werden die Windows-Registrierungsspeicherorte beschrieben, die bei der Installation eines Outlook Social Connector-Anbieters (OSC) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="113eb-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="113eb-105">COM-Registrierung</span><span class="sxs-lookup"><span data-stu-id="113eb-105">COM registration</span></span>

<span data-ttu-id="113eb-106">Sie müssen die OSC-Anbieter-DLL so konfigurieren, dass Sie die COM-Self-Registration oder regsvr32 während der Installation registriert.</span><span class="sxs-lookup"><span data-stu-id="113eb-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="113eb-107">Die COM-Registrierung der Anbieter-DLL registriert den OSC- `HKEY_CLASSES_ROOT` Anbieter unter der Registrierungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="113eb-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="113eb-108">Ein in verwaltetem Code entwickelter OSC-Anbieter verfügt über eine COM-sichtbare Anbieter Assembly.</span><span class="sxs-lookup"><span data-stu-id="113eb-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="113eb-109">Sie sollten eine separate Anwendungsdomäne für die Anbieterkomponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="113eb-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="113eb-110">Andernfalls verwendet der OSC-Anbieter die standardmäßige freigegebene Anwendungsdomäne, die von anderen Komponenten verwendet wird, und der Anbieter funktioniert möglicherweise nicht wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="113eb-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="113eb-111">Registrieren der Anbieter-ProgID</span><span class="sxs-lookup"><span data-stu-id="113eb-111">Registering provider ProgID</span></span>

<span data-ttu-id="113eb-112">Jeder OSC-Anbieter muss einen programmgesteuerten Bezeichner (`ProgID`) registrieren.</span><span class="sxs-lookup"><span data-stu-id="113eb-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="113eb-113">Das Installationsprogramm des Anbieters kann einen der folgenden Speicherorte auswählen `ProgID`:</span><span class="sxs-lookup"><span data-stu-id="113eb-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="113eb-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Ihr Anbieter Installationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter nur für den derzeit angemeldeten Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="113eb-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="113eb-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Ihr Anbieter Installationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter für alle Benutzer auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="113eb-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="113eb-116">Der OSC sucht in den oben `ProgID` genannten Speicherorten nach dem Anbieter, es sei denn, der Clientcomputer hat 32-Bit Outlook auf einem 64-Bit-Windows-Betriebssystem ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="113eb-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="113eb-117">In diesem Fall sollte das Installationsprogramm des Anbieters eine der folgenden Speicherorte in der `HKEY_CURRENT_USER` oder `HKEY_LOCAL_MACHINE` -Struktur auswählen:</span><span class="sxs-lookup"><span data-stu-id="113eb-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="113eb-118">Bei einer Klick-und-Los-Version von Office sollte das Installationsprogramm eines der folgenden Speicherorte in der Struktur HKEY_CURRENT_USER oder HKEY_LOCAL_MACHINE wählen:</span><span class="sxs-lookup"><span data-stu-id="113eb-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="113eb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="113eb-119">See also</span></span>

- [<span data-ttu-id="113eb-120">PrüfListe für die Installation</span><span class="sxs-lookup"><span data-stu-id="113eb-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="113eb-121">Schnelle Schritte für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="113eb-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="113eb-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="113eb-122">Deploying a Provider</span></span>](deploying-a-provider.md)

