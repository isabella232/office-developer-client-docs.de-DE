---
title: Technische Anforderungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: In diesem Thema werden die unterstützten Programmiersprachen, Typ Anforderungen und Details zu den Outlook Social Connector (OSC)-Erweiterbarkeit des Providers DLL COM-Sichtbarkeit und -Methode zurück.
ms.openlocfilehash: 94b57e20957f3d8d779c4d3324ecbb8ccd37f60a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796083"
---
# <a name="technical-requirements"></a><span data-ttu-id="4afee-103">Technische Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4afee-103">Technical requirements</span></span>

<span data-ttu-id="4afee-104">In diesem Thema werden die unterstützten Programmiersprachen, Typ Anforderungen und Details zu den Outlook Social Connector (OSC)-Erweiterbarkeit des Providers DLL COM-Sichtbarkeit und -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="4afee-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="4afee-105">Programmiersprachen und COM-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4afee-105">Programming language and COM requirements</span></span>

<span data-ttu-id="4afee-106">Sie können einen OSC-Anbieter mit verwalteten Sprachen wie Visual c# oder Visual Basic oder nicht verwaltete Sprachen wie Visual C++ erstellen.</span><span class="sxs-lookup"><span data-stu-id="4afee-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="4afee-107">Sie können eine beliebige Tool verwenden, die eine COM-sichtbare DLL-Komponente Informationen zum Entwickeln von eines OSC-Anbieters erstellen können.</span><span class="sxs-lookup"><span data-stu-id="4afee-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="4afee-108">Die Entscheidung für eine verwaltete oder nicht verwaltete Sprache zum Entwickeln eines Providers sollte Konto die Download-Größe und Abhängigkeiten des Installationspakets Anbieter berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="4afee-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="4afee-109">Ein OSC-Anbieter muss COM-sichtbar sein, wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="4afee-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="4afee-110">Nach der Installation muss ein OSC-Anbieters mithilfe von COM-Self-Registrierung oder regsvr32 registriert werden.</span><span class="sxs-lookup"><span data-stu-id="4afee-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="4afee-111">COM-Registrierung eines OSC-Anbieters DLL registriert den Anbieter unter HKCU oder HKLM.</span><span class="sxs-lookup"><span data-stu-id="4afee-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="4afee-112">ProgID des Providers registriert ist, klicken Sie unter `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="4afee-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="4afee-113">Ein in einer verwalteten Sprache entwickelt OSC-Anbieter ist COM-sichtbar.</span><span class="sxs-lookup"><span data-stu-id="4afee-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="4afee-114">Ein OSC-Anbieter sollten Werte hinzufügen, der Windows-Registrierung, die angeben, dass der Provider-DLL des Apartmentthreading Single-Threading (Station) und multithreaded Apartmentthreading (MTA) Modelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4afee-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="4afee-115">Weitere Informationen zu COM Threadmodelle finden Sie unter [Beschreibung und Funktionsweise von OLE Threading-Modelle](http://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="4afee-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](http://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="4afee-116">Methoden bei der Erweiterbarkeit der OSC-Anbieter müssen Grundtypen wie **Zeichenfolge** oder **Bool**zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4afee-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="4afee-117">Bestimmte **Zeichenfolge** zurück, dass die Werte der Schemadefinition für die Erweiterbarkeit des OSC-Providers einhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="4afee-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="4afee-118">Nur XML-Zeichenfolge wird als Rückgabewert unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4afee-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="4afee-119">Details der die OSC-anbietererweiterung DLL</span><span class="sxs-lookup"><span data-stu-id="4afee-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="4afee-120">Die Komponente, die Erweiterbarkeit des OSC-Providers unterstützt ist die OSC-anbietererweiterung DLL.</span><span class="sxs-lookup"><span data-stu-id="4afee-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="4afee-121">Drittanbieter-Entwickler können mit dieser Erweiterungsschnittstellen OSC-Anbieter-DLLs erstellen.</span><span class="sxs-lookup"><span data-stu-id="4afee-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="4afee-122">Die folgende Liste enthält die Details der OSC-anbietererweiterung DLL:</span><span class="sxs-lookup"><span data-stu-id="4afee-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="4afee-123">Erweiterbarkeit der DLL-Dateiname: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="4afee-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="4afee-124">Erweiterbarkeit der DLL-Anzeigename: Microsoft Outlook für soziale Netzwerke Erweiterbarkeit des Providers</span><span class="sxs-lookup"><span data-stu-id="4afee-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="4afee-125">Erweiterbarkeit der DLL-Hauptversion: 15.0</span><span class="sxs-lookup"><span data-stu-id="4afee-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="4afee-126">Der Typbibliothek Extensibiilty-DLL-Version: 1.1</span><span class="sxs-lookup"><span data-stu-id="4afee-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="4afee-127">Sonstige technische Informationen</span><span class="sxs-lookup"><span data-stu-id="4afee-127">Miscellaneous technical information</span></span>

<span data-ttu-id="4afee-128">JavaScript Object Notation (JSON) wird im Modell Erweiterbarkeit OSC-Anbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4afee-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="4afee-129">Es gibt keine Abhängigkeiten auf einen XML-Parser.</span><span class="sxs-lookup"><span data-stu-id="4afee-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="4afee-130">OSC-Anbieter kann verwenden einen XML-Parser, der mit Office, wie beispielsweise Microsoft XML Core Services (MSXML) enthalten ist, verwenden Sie die XML-Parser Funktionen in Microsoft .NET Framework integriert, oder einen Drittanbieter-XML-Parser.</span><span class="sxs-lookup"><span data-stu-id="4afee-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4afee-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4afee-131">See also</span></span>

- [<span data-ttu-id="4afee-132">Bewährte Methoden für das Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="4afee-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="4afee-133">QuickSteps für Informationen zum Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="4afee-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="4afee-134">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="4afee-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="4afee-135">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="4afee-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

