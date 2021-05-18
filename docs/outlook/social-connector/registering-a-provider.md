---
title: Registrieren eines Providers
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: In diesem Thema werden Windows Registrierungsstandorte beschrieben, die bei der Installation eines Outlook Social Connector (OSC) verwendet werden.
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421760"
---
# <a name="registering-a-provider"></a><span data-ttu-id="be5bf-103">Registrieren eines Providers</span><span class="sxs-lookup"><span data-stu-id="be5bf-103">Registering a provider</span></span>

<span data-ttu-id="be5bf-104">In diesem Thema werden Windows Registrierungsstandorte beschrieben, die bei der Installation eines Outlook Social Connector (OSC) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be5bf-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="be5bf-105">COM-Registrierung</span><span class="sxs-lookup"><span data-stu-id="be5bf-105">COM registration</span></span>

<span data-ttu-id="be5bf-106">Sie müssen die OSC-Anbieter-DLL so konfigurieren, dass sie sich während der Installation mithilfe der COM-Selbstregistrierung oder regsvr32 registriert.</span><span class="sxs-lookup"><span data-stu-id="be5bf-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="be5bf-107">Die COM-Registrierung der Anbieter-DLL registriert den OSC-Anbieter unter der `HKEY_CLASSES_ROOT` Registrierungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="be5bf-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="be5bf-108">Ein in verwalteter Code entwickelter OSC-Anbieter verfügt über eine COM-sichtbare Anbieter-Assembly.</span><span class="sxs-lookup"><span data-stu-id="be5bf-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="be5bf-109">Sie sollten eine separate Anwendungsdomäne für die Anbieterkomponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="be5bf-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="be5bf-110">Andernfalls verwendet der OSC-Anbieter die standardmäßige freigegebene Anwendungsdomäne, die von anderen Komponenten verwendet wird, und der Anbieter funktioniert möglicherweise nicht wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="be5bf-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="be5bf-111">Registrieren des Anbieters ProgID</span><span class="sxs-lookup"><span data-stu-id="be5bf-111">Registering provider ProgID</span></span>

<span data-ttu-id="be5bf-112">Jeder OSC-Anbieter muss einen programmgesteuerten Bezeichner ( `ProgID` ) registrieren.</span><span class="sxs-lookup"><span data-stu-id="be5bf-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="be5bf-113">Das Installationsprogramm des Anbieters kann einen der folgenden Speicherorte auswählen, um folgendes hinzuzufügen oder zu `ProgID` entfernen:</span><span class="sxs-lookup"><span data-stu-id="be5bf-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="be5bf-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`Ihr Anbieterinstallationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter nur für den aktuell &ndash; angemeldeten Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="be5bf-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="be5bf-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;Ihr Anbieterinstallationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter für alle Benutzer auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="be5bf-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="be5bf-116">Das Betriebssystem sucht an den oben genannten Speicherorten nach dem Anbieter, es sei denn, der Clientcomputer verfügt über `ProgID` 32-Bit-Outlook auf einem 64-Bit-Betriebssystem Windows betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="be5bf-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="be5bf-117">In einem solchen Fall sollte Ihr Anbieterinstallationsprogramm einen der folgenden Speicherorte im oder im  `HKEY_CURRENT_USER`  `HKEY_LOCAL_MACHINE` Hive auswählen:</span><span class="sxs-lookup"><span data-stu-id="be5bf-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="be5bf-118">Für eine Klick-und-Aus-Version von Office sollte Ihr Anbieterinstaller einen der folgenden Speicherorte im HKEY_CURRENT_USER oder HKEY_LOCAL_MACHINE auswählen:</span><span class="sxs-lookup"><span data-stu-id="be5bf-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="be5bf-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be5bf-119">See also</span></span>

- [<span data-ttu-id="be5bf-120">Prüfliste für die Installation</span><span class="sxs-lookup"><span data-stu-id="be5bf-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="be5bf-121">Schnelle Schritte zum Entwickeln eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="be5bf-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="be5bf-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="be5bf-122">Deploying a Provider</span></span>](deploying-a-provider.md)

