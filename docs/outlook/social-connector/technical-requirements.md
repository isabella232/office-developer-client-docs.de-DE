---
title: Technische Anforderungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: In diesem Thema werden die unterstützten Programmiersprachen, COM-Sichtbarkeits-und Methodenrückgabe Typen und Details zur Erweiterbarkeits-DLL für Outlook Social Connector (OSC) beschrieben.
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329155"
---
# <a name="technical-requirements"></a><span data-ttu-id="f5a46-103">Technische Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5a46-103">Technical requirements</span></span>

<span data-ttu-id="f5a46-104">In diesem Thema werden die unterstützten Programmiersprachen, COM-Sichtbarkeits-und Methodenrückgabe Typen und Details zur Erweiterbarkeits-DLL für Outlook Social Connector (OSC) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f5a46-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="f5a46-105">Programmiersprachen-und COM-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5a46-105">Programming language and COM requirements</span></span>

<span data-ttu-id="f5a46-106">Sie können einen OSC-Anbieter erstellen, indem Sie verwaltete Sprachen wie Visual C# oder Visual Basic oder nicht verwaltete Sprachen wie Visual C++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5a46-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="f5a46-107">Sie können ein beliebiges Tool verwenden, mit dem eine COM-sichtbare DLL-Komponente erstellt werden kann, um einen OSC-Anbieter zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="f5a46-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="f5a46-108">Die Entscheidung, eine verwaltete oder nicht verwaltete Sprache für die Entwicklung eines Anbieters zu verwenden, sollte die Downloadgröße und die Abhängigkeiten des Anbieter Installationspakets berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="f5a46-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="f5a46-109">Ein OSC-Anbieter muss gemäß der folgenden Definition COM-sichtbar sein:</span><span class="sxs-lookup"><span data-stu-id="f5a46-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="f5a46-110">Nach der Installation muss ein OSC-Anbieter mithilfe von COM Self-Registration oder regsvr32 registriert werden.</span><span class="sxs-lookup"><span data-stu-id="f5a46-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="f5a46-111">Die COM-Registrierung einer OSC-Anbieter-DLL registriert den Anbieter unter HKCU oder HKLM.</span><span class="sxs-lookup"><span data-stu-id="f5a46-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="f5a46-112">Die ProgID eines Anbieters ist unter `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`registriert.</span><span class="sxs-lookup"><span data-stu-id="f5a46-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="f5a46-113">Ein OSC-Anbieter, der in einer verwalteten Sprache entwickelt wurde, ist COM-sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f5a46-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="f5a46-114">Ein OSC-Anbieter sollte der Windows-Registrierung Werte hinzufügen, die darauf hinweisen, dass die Anbieter-DLL sowohl ein STA-als auch ein Multithread-Apartment (MTA)-Threading-Modelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5a46-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="f5a46-115">Weitere Informationen zu COM-Threadingmodellen finden Sie unter [Beschreibungen und Funktionsweise von OLE](https://support.microsoft.com/kb/150777)-threadIng-Modellen.</span><span class="sxs-lookup"><span data-stu-id="f5a46-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="f5a46-116">Methoden in der OSC-Anbieter Erweiterbarkeit müssen primitive Typen wie **String** oder **bool**zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f5a46-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="f5a46-117">Bestimmte **Zeichenfolgen** Rückgabewerte müssen der Schema Definition für osc-Anbieter Erweiterbarkeit entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f5a46-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="f5a46-118">Nur XML wird als Rückgabewert unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5a46-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="f5a46-119">Details zur OSC-Anbieter Erweiterbarkeits-DLL</span><span class="sxs-lookup"><span data-stu-id="f5a46-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="f5a46-120">Die Komponente, die OSC-Anbieter Erweiterbarkeit unterstützt, ist die OSC-Erweiterungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="f5a46-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="f5a46-121">Drittanbieter-Entwickler können OSC-Anbieter-DLLs mithilfe dieser Erweiterbarkeitsschnittstellen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5a46-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="f5a46-122">In der folgenden Liste sind die Details der OSC-Anbieter Erweiterungs-DLL aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="f5a46-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="f5a46-123">Erweiterungs-DLL-Dateiname: socialprovider. dll</span><span class="sxs-lookup"><span data-stu-id="f5a46-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="f5a46-124">Erweiterbarkeit der DLL-Datei: Microsoft Outlook-Erweiterbarkeit für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f5a46-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="f5a46-125">Erweiterungs-DLL-Hauptversion: 15,0</span><span class="sxs-lookup"><span data-stu-id="f5a46-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="f5a46-126">Extensibiilty-DLL-Bibliotheksversion: 1,1</span><span class="sxs-lookup"><span data-stu-id="f5a46-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="f5a46-127">Sonstige technische Informationen</span><span class="sxs-lookup"><span data-stu-id="f5a46-127">Miscellaneous technical information</span></span>

<span data-ttu-id="f5a46-128">JSON (JavaScript Object Notation) wird im Erweiterbarkeitsmodell des OSC-Anbieters nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5a46-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="f5a46-129">Es gibt keine Abhängigkeiten von einem XML-Parser.</span><span class="sxs-lookup"><span data-stu-id="f5a46-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="f5a46-130">Der OSC-Anbieter kann einen in Office enthaltenen XML-Parser wie Microsoft XML Core Services (MSXML) verwenden, die in Microsoft .NET Framework integrierten XML-Analysefunktionen verwenden oder einen Drittanbieter-XML-Parser verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5a46-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f5a46-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5a46-131">See also</span></span>

- [<span data-ttu-id="f5a46-132">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="f5a46-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="f5a46-133">Schnelle Schritte für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="f5a46-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="f5a46-134">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="f5a46-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="f5a46-135">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f5a46-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

