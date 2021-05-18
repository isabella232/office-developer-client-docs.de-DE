---
title: Informationen zur InfoPath XML-Interop-Assembly
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml interop [infopath 2007],InfoPath 2007, PRIMÄRE XML-Interop-Assembly,InfoPath XML-Interop-Assembly
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: Die InfoPath XML-Interop-Assembly wird bereitgestellt, um unterstützung für die Interoperabilität zwischen verwalteten Code und dem COM-Server zu ermöglichen, der von Microsoft XML Core Services (MSXML) von externen Anwendungen verfügbar gemacht wird, die InfoPath automatisieren.
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303780"
---
# <a name="about-the-infopath-xml-interop-assembly"></a><span data-ttu-id="f8dcf-104">Informationen zur InfoPath XML-Interop-Assembly</span><span class="sxs-lookup"><span data-stu-id="f8dcf-104">About the InfoPath XML interop assembly</span></span>

<span data-ttu-id="f8dcf-105">Die InfoPath XML-Interop-Assembly wird bereitgestellt, um unterstützung für die Interoperabilität zwischen verwalteten Code und dem COM-Server zu ermöglichen, der von Microsoft XML Core Services (MSXML) von externen Anwendungen verfügbar gemacht wird, die InfoPath automatisieren.</span><span class="sxs-lookup"><span data-stu-id="f8dcf-105">The InfoPath XML interop assembly is provided to allow support for interoperability between managed code and the COM server exposed by Microsoft XML Core Services (MSXML) from external applications that automate InfoPath.</span></span>

<span data-ttu-id="f8dcf-106">Die **Option .NET Programmability Support** im InfoPath-Setupprogramm installiert drei Interopassemblys.</span><span class="sxs-lookup"><span data-stu-id="f8dcf-106">The **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="f8dcf-107">Interop-Assemblys sind .NET-Assemblys, die als Verbindung zwischen verwaltetem und nicht verwaltetem Code dienen, indem sie COM-Objektmember entsprechenden verwalteten .NET-Membern zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f8dcf-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> <span data-ttu-id="f8dcf-108">Eine dieser Assemblys, Microsoft.Office.Interop.InfoPath.Xml.dll, stellt die Mitglieder [](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) desMicrosoft.Office.Interop.InfoPath.Xml-Namespaces zur Verfügung, der für die Arbeit mit Mitgliedern verwendet wird, die vom COM-Server für Microsoft XML Core Services (MSXML) aus externen Anwendungen verfügbar gemacht werden, die InfoPath mithilfe von verwalteten Code automatisieren.</span><span class="sxs-lookup"><span data-stu-id="f8dcf-108">One of those assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, provides the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) namespace, which is used to work with members exposed by the COM server for Microsoft XML Core Services (MSXML) from external applications that automate InfoPath using managed code.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f8dcf-109">Die Verweise auf die Microsoft.Office.Interop.InfoPath.dll und Microsoft.Office.Interop.InfoPath.Xml.dll, die für externe InfoPath-Automatisierungsprojekte erforderlich sind, müssen manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f8dcf-109">The references to the Microsoft.Office.Interop.InfoPath.dll and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies that are required for InfoPath external automation projects must be established manually.</span></span> <span data-ttu-id="f8dcf-110">Weitere Informationen zur externen Automatisierung finden Sie unter [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span><span class="sxs-lookup"><span data-stu-id="f8dcf-110">For more information on external automation, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f8dcf-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8dcf-111">See also</span></span>

- [<span data-ttu-id="f8dcf-112">Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="f8dcf-112">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

