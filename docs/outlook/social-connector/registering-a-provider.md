---
title: Registrieren eines Providers
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: In diesem Thema werden die Speicherorte der Windows-Registrierung, die verwendet werden, wenn Sie einen Anbieter für Outlook Social Connector (OSC) installieren.
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796075"
---
# <a name="registering-a-provider"></a><span data-ttu-id="556ba-103">Registrieren eines Providers</span><span class="sxs-lookup"><span data-stu-id="556ba-103">Registering a provider</span></span>

<span data-ttu-id="556ba-104">In diesem Thema werden die Speicherorte der Windows-Registrierung, die verwendet werden, wenn Sie einen Anbieter für Outlook Social Connector (OSC) installieren.</span><span class="sxs-lookup"><span data-stu-id="556ba-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="556ba-105">COM-Registrierung</span><span class="sxs-lookup"><span data-stu-id="556ba-105">COM registration</span></span>

<span data-ttu-id="556ba-106">Sie müssen den OSC-Anbieter-DLL zum Registrieren von COM-Self-Registrierung oder regsvr32 während der Installation konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="556ba-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="556ba-107">COM-Registrierung der Provider-DLL registriert den OSC-Anbieter unter der `HKEY_CLASSES_ROOT` Registrierungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="556ba-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="556ba-108">Ein OSC-Anbieter in verwaltetem Code entwickelt hat eine COM-sichtbare Anbieterassembly.</span><span class="sxs-lookup"><span data-stu-id="556ba-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="556ba-109">Sie sollten eine separate Anwendungsdomäne für die Providerkomponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="556ba-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="556ba-110">Sie andernfalls der OSC-Anbieter verwendet die Standarddomäne für den freigegebenen Anwendung, die von anderen Komponenten verwendet wird, und der Anbieter funktionieren möglicherweise nicht wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="556ba-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="556ba-111">Provider-ProgID registrieren</span><span class="sxs-lookup"><span data-stu-id="556ba-111">Registering provider ProgID</span></span>

<span data-ttu-id="556ba-112">Jeder OSC-Anbieter muss einen programmgesteuerten Bezeichner registrieren (`ProgID`).</span><span class="sxs-lookup"><span data-stu-id="556ba-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="556ba-113">Das Installationsprogramm Anbieter kann wählen Sie eine der folgenden Speicherorte zum Hinzufügen oder Entfernen der `ProgID`:</span><span class="sxs-lookup"><span data-stu-id="556ba-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="556ba-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Das Installationsprogramm der Anbieter sollte diesen Speicherort verwenden, wenn der Anbieter nur für den aktuell angemeldeten Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="556ba-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="556ba-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Das Installationsprogramm der Anbieter sollte diesen Speicherort verwenden, wenn der Anbieter für alle Benutzer auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="556ba-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="556ba-116">Die OSC sucht für den Anbieter `ProgID` an die oben genannten Speicherorten, wenn es sich bei dem Clientcomputer 32-Bit-Outlook auf einem 64-Bit-Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="556ba-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="556ba-117">In diesem Fall sollte das Installationsprogramm der Anbieter auswählen eine der folgenden Speicherorten in der `HKEY_CURRENT_USER` oder `HKEY_LOCAL_MACHINE` Struktur:</span><span class="sxs-lookup"><span data-stu-id="556ba-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="556ba-118">Eine Klick-und-Los-Version von Office sollte das Installationsprogramm der Anbieter eine der folgenden Speicherorte in der Struktur HKEY_CURRENT_USER oder HKEY_LOCAL_MACHINE auswählen:</span><span class="sxs-lookup"><span data-stu-id="556ba-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="556ba-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="556ba-119">See also</span></span>

- [<span data-ttu-id="556ba-120">Checkliste für Installation</span><span class="sxs-lookup"><span data-stu-id="556ba-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="556ba-121">QuickSteps für Informationen zum Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="556ba-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="556ba-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="556ba-122">Deploying a Provider</span></span>](deploying-a-provider.md)

