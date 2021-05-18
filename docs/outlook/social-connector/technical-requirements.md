---
title: Technische Anforderungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: In diesem Thema werden die unterstützten Programmiersprachen, die Anforderungen für die COM-Sichtbarkeit und die Rückgabetypanforderungen der Methode sowie Details der Outlook Social Connector (OSC)-Anbieter-Erweiterbarkeits-DLL beschrieben.
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329155"
---
# <a name="technical-requirements"></a><span data-ttu-id="e6d10-103">Technische Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6d10-103">Technical requirements</span></span>

<span data-ttu-id="e6d10-104">In diesem Thema werden die unterstützten Programmiersprachen, die Anforderungen für die COM-Sichtbarkeit und die Rückgabetypanforderungen der Methode sowie Details der Outlook Social Connector (OSC)-Anbieter-Erweiterbarkeits-DLL beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e6d10-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="e6d10-105">Programmiersprachen- und COM-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6d10-105">Programming language and COM requirements</span></span>

<span data-ttu-id="e6d10-106">Sie können einen #A0 mithilfe verwalteter Sprachen wie Visual C# oder Visual Basic oder nicht verwalteten Sprachen wie Visual C++ erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6d10-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="e6d10-107">Sie können jedes Tool verwenden, das eine COM-sichtbare DLL-Komponente erstellen kann, um einen OSC-Anbieter zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="e6d10-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="e6d10-108">Die Entscheidung, eine verwaltete oder nicht verwaltete Sprache zum Entwickeln eines Anbieters zu verwenden, sollte die Downloadgröße und Abhängigkeiten des Anbieterinstallationspakets berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="e6d10-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="e6d10-109">Ein OSC-Anbieter muss com-visible sein, wie durch folgendes definiert:</span><span class="sxs-lookup"><span data-stu-id="e6d10-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="e6d10-110">Nach der Installation muss ein OSC-Anbieter mithilfe der COM-Selbstregistrierung oder regsvr32 registriert werden.</span><span class="sxs-lookup"><span data-stu-id="e6d10-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="e6d10-111">Die COM-Registrierung einer OSC-Anbieter-DLL registriert den Anbieter unter HKCU oder HKLM.</span><span class="sxs-lookup"><span data-stu-id="e6d10-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="e6d10-112">Die ProgID eines Anbieters ist unter  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` registriert.</span><span class="sxs-lookup"><span data-stu-id="e6d10-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="e6d10-113">Ein in einer verwalteten Sprache entwickelter OSC-Anbieter ist COM-visible.</span><span class="sxs-lookup"><span data-stu-id="e6d10-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="e6d10-114">Ein OSC-Anbieter sollte der Windows-Registrierung Werte hinzufügen, die angeben, dass die Anbieter-DLL sowohl Single-Threaded Apartment (STA) als auch Multithreaded Apartment (MTA)-Threadingmodelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e6d10-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="e6d10-115">Weitere Informationen zu COM-Threadingmodellen finden Sie unter [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="e6d10-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="e6d10-116">Methoden in der Erweiterbarkeit des OSC-Anbieters müssen primitive Typen wie **zeichenfolge** oder **bool zurückgeben.**</span><span class="sxs-lookup"><span data-stu-id="e6d10-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="e6d10-117">Bestimmte  Zeichenfolgenrücklaufwerte müssen der Schemadefinition für die Erweiterbarkeit des OSC-Anbieters entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e6d10-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="e6d10-118">Nur XML wird als Rückgabewert unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e6d10-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="e6d10-119">Details zur ERWEITERUNGS-DLL des OSC-Anbieters</span><span class="sxs-lookup"><span data-stu-id="e6d10-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="e6d10-120">Die Komponente, die die Erweiterbarkeit des OSC-Anbieters unterstützt, ist die ERWEITERUNGS-DLL des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="e6d10-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="e6d10-121">Drittanbieterentwickler können MITHILFE dieser Erweiterbarkeitsschnittstellen DLLs des OSC-Anbieters erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6d10-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="e6d10-122">In der folgenden Liste sind die Details der ERWEITERUNGs-DLL des OSC-Anbieters aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="e6d10-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="e6d10-123">Erweiterungs-DLL-Dateiname: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="e6d10-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="e6d10-124">Erweiterungs-DLL-Anzeigename: Microsoft Outlook Erweiterbarkeit für soziale Anbieter</span><span class="sxs-lookup"><span data-stu-id="e6d10-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="e6d10-125">Erweiterungs-DLL-Hauptversion: 15.0</span><span class="sxs-lookup"><span data-stu-id="e6d10-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="e6d10-126">Extensibiilty DLL TypeLib Version: 1.1</span><span class="sxs-lookup"><span data-stu-id="e6d10-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="e6d10-127">Verschiedene technische Informationen</span><span class="sxs-lookup"><span data-stu-id="e6d10-127">Miscellaneous technical information</span></span>

<span data-ttu-id="e6d10-128">JavaScript Object Notation (JSON) wird im Erweiterbarkeitsmodell des OSC-Anbieters nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e6d10-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="e6d10-129">Es gibt keine Abhängigkeiten von einem XML-Parser.</span><span class="sxs-lookup"><span data-stu-id="e6d10-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="e6d10-130">Der OSC-Anbieter kann einen xml-Parser verwenden, der in Office enthalten ist, z. B. Microsoft XML Core Services (MSXML), die in Microsoft .NET Framework integrierten XML-Analysefunktionen oder einen DRITTANBIETER-XML-Parser verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6d10-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6d10-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6d10-131">See also</span></span>

- [<span data-ttu-id="e6d10-132">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="e6d10-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="e6d10-133">Schnelle Schritte zum Entwickeln eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="e6d10-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="e6d10-134">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="e6d10-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="e6d10-135">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="e6d10-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

