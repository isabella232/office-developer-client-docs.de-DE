---
title: Von 0 auf 100 mit Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Ein Anwendungsentwickler kann eine Project Online-Website (in SharePoint gehostet) mithilfe eigenständiger Anwendungen und/oder Projekt-Add-Ins anpassen. Es gibt eine Vielzahl von Anwendungen, die von den Anforderungen der Beteiligten an einem Projekt bis hin zu PMO-Supportfunktionen reichen, wie beispielsweise einem der folgenden:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344408"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="3f9bd-103">Von 0 auf 100 mit Project Online</span><span class="sxs-lookup"><span data-stu-id="3f9bd-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="3f9bd-104">Ein Anwendungsentwickler kann eine Project Online-Website (in SharePoint gehostet) mithilfe eigenständiger Anwendungen und/oder Projekt-Add-Ins anpassen. Es gibt eine Vielzahl von Anwendungen, die von den Anforderungen der Beteiligten an einem Projekt bis hin zu PMO-Supportfunktionen reichen, wie beispielsweise einem der folgenden:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="3f9bd-105">Optimierter Zeitkarten Dateneintrag für Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="3f9bd-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="3f9bd-106">Effiziente Zeitkarten Genehmigung für Vorgesetzte</span><span class="sxs-lookup"><span data-stu-id="3f9bd-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="3f9bd-107">Aufsicht über Genehmigungen (Beschaffung und Status), die für ein Projekt erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="3f9bd-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="3f9bd-108">Status/Integritätsprüfung aktiver Projekte</span><span class="sxs-lookup"><span data-stu-id="3f9bd-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="3f9bd-109">Problembericht</span><span class="sxs-lookup"><span data-stu-id="3f9bd-109">Issues report</span></span>
- <span data-ttu-id="3f9bd-110">Change Management-Status Bericht</span><span class="sxs-lookup"><span data-stu-id="3f9bd-110">Change Management Status report</span></span>
    
<span data-ttu-id="3f9bd-111">Project Online umfasst API-Unterstützung für die folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="3f9bd-112">Für ein gehostetes Projekt (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="3f9bd-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="3f9bd-113">Code (JavaScript, HTML, CSS), der in SharePoint Online gehostet wird</span><span class="sxs-lookup"><span data-stu-id="3f9bd-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="3f9bd-114">Objekte, die in den Browser heruntergeladen und für SharePoint Online ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="3f9bd-115">Geschäftslogik in JavaScript</span><span class="sxs-lookup"><span data-stu-id="3f9bd-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="3f9bd-116">Zugreifen auf Daten, die in Project Online oder SharePoint wie (aber nicht beschränkt auf) in gespeichert sind:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="3f9bd-117">Custom fields (benutzerdefinierte Felder)</span><span class="sxs-lookup"><span data-stu-id="3f9bd-117">Custom fields</span></span>  
  - <span data-ttu-id="3f9bd-118">Listen</span><span class="sxs-lookup"><span data-stu-id="3f9bd-118">Lists</span></span>
    
- <span data-ttu-id="3f9bd-119">Für ein von einem Projekt (SharePoint) vom Anbieter gehostetes Add-in:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="3f9bd-120">Code, der auf einer Website außerhalb der Project Online-Website vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="3f9bd-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="3f9bd-121">Eine externe Website, die (aber nicht beschränkt auf) sein kann:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="3f9bd-122">Eine andere SharePoint-Website</span><span class="sxs-lookup"><span data-stu-id="3f9bd-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="3f9bd-123">Web-App/Dienst auf einer beliebigen Plattform</span><span class="sxs-lookup"><span data-stu-id="3f9bd-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="3f9bd-124">Die externe Website enthält Geschäftslogik</span><span class="sxs-lookup"><span data-stu-id="3f9bd-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="3f9bd-125">Der Browser wird von Project online zu externer Website mit Zugriffstoken zu Project Online umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="3f9bd-126">Die externe Website kann Aufrufe an SharePoint und Project online tätigen</span><span class="sxs-lookup"><span data-stu-id="3f9bd-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="3f9bd-127">Für ein externes/eigenständiges Add-in:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="3f9bd-128">Der Benutzer führt eine Anwendung auf dem Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-128">User executes an application on their device</span></span>
  - <span data-ttu-id="3f9bd-129">Anwendung authentifiziert und ruft Project Online-APIs direkt auf</span><span class="sxs-lookup"><span data-stu-id="3f9bd-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="3f9bd-130">Art der Anwendung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-130">Type of application</span></span>|<span data-ttu-id="3f9bd-131">API-Implementierung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-131">API implementation</span></span>|<span data-ttu-id="3f9bd-132">Zielumgebung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-132">Target environment</span></span>|<span data-ttu-id="3f9bd-133">Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="3f9bd-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3f9bd-134">Projekt gehostet</span><span class="sxs-lookup"><span data-stu-id="3f9bd-134">Project hosted</span></span>  <br/> |<span data-ttu-id="3f9bd-135">JSOM (Java Script Object Model)</span><span class="sxs-lookup"><span data-stu-id="3f9bd-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="3f9bd-136">REST</span><span class="sxs-lookup"><span data-stu-id="3f9bd-136">REST</span></span>  <br/> |<span data-ttu-id="3f9bd-137">Browser</span><span class="sxs-lookup"><span data-stu-id="3f9bd-137">Browser</span></span>  <br/> |<span data-ttu-id="3f9bd-138">Zeitkarten Eintrag</span><span class="sxs-lookup"><span data-stu-id="3f9bd-138">Timecard entry</span></span>  <br/> <span data-ttu-id="3f9bd-139">Zeitkarten Genehmigung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-139">Timecard approval</span></span>  <br/> <span data-ttu-id="3f9bd-140">Projekt Status</span><span class="sxs-lookup"><span data-stu-id="3f9bd-140">Project Status</span></span>  <br/> <span data-ttu-id="3f9bd-141">Problembericht</span><span class="sxs-lookup"><span data-stu-id="3f9bd-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="3f9bd-142">Gehosteter Projektanbieter</span><span class="sxs-lookup"><span data-stu-id="3f9bd-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="3f9bd-143">CSOM-Clientbibliothek</span><span class="sxs-lookup"><span data-stu-id="3f9bd-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="3f9bd-144">Azure-Website/-App</span><span class="sxs-lookup"><span data-stu-id="3f9bd-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="3f9bd-145">Nicht-Windows-Umgebung (Lampe usw.)</span><span class="sxs-lookup"><span data-stu-id="3f9bd-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="3f9bd-146">Externe Validierung in der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="3f9bd-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="3f9bd-147">Projekt-Importierer</span><span class="sxs-lookup"><span data-stu-id="3f9bd-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="3f9bd-148">Extern/eigenständig</span><span class="sxs-lookup"><span data-stu-id="3f9bd-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="3f9bd-149">REST</span><span class="sxs-lookup"><span data-stu-id="3f9bd-149">REST</span></span>  <br/> <span data-ttu-id="3f9bd-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="3f9bd-150">CSOM</span></span>  <br/> |<span data-ttu-id="3f9bd-151">REST – beliebige Plattform</span><span class="sxs-lookup"><span data-stu-id="3f9bd-151">REST - any platform</span></span>  <br/> <span data-ttu-id="3f9bd-152">CSOM-beliebige von .NET unterstützte Plattform</span><span class="sxs-lookup"><span data-stu-id="3f9bd-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="3f9bd-153">Zeitkarten Eintrag</span><span class="sxs-lookup"><span data-stu-id="3f9bd-153">Timecard entry</span></span>  <br/> <span data-ttu-id="3f9bd-154">Migration von Projekten zu einer neuen Website</span><span class="sxs-lookup"><span data-stu-id="3f9bd-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="3f9bd-155">Change Management Status.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="3f9bd-156">Was wird benötigt, um die Entwicklung von Anwendungen für Project online zu beginnen?</span><span class="sxs-lookup"><span data-stu-id="3f9bd-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="3f9bd-157">Die allgemeinen Elemente, die für die Entwicklung von Project Online-Anwendungen erforderlich sind, sind Project Online-Konto und Testdaten--Projekte und projektbezogene Informationen, die Zuordnungen, Aufgaben, Ressourcen und benutzerdefinierte Felder einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="3f9bd-158">Eine Entwicklungsumgebung ist ebenfalls erforderlich, aber die Spezifik der Entwicklungsumgebung hängt vom Typ der Anwendung und der API-Schnittstelle ab, die für die Anwendung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="3f9bd-159">In den nächsten Abschnitten werden die Entwicklungsanforderungen für die drei API-Schnittstellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="3f9bd-160">In der Referenzdokumentation wird das für alle drei Schnittstellen gängige Objektmodell sowie eine Entitätszuordnung beschrieben, in der die Beziehungen zwischen den Objektmodell Komponenten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="3f9bd-161">Projekt gehostete Add-in-Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="3f9bd-162">Ein gehostetes Add-in ist ein Add-in, das sich auf dem Server befindet und zur Laufzeitausführung in einen Browser heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="3f9bd-163">Gehostete Add-Ins können die JSOM-oder REST-Schnittstellen verwenden und in JavaScript geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="3f9bd-164">Project Online stellt Verweise auf die JSOM-Bibliothek für die Laufzeitausführung bereit.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="3f9bd-165">Unter der Voraussetzung, dass die Entwicklung auf einer Windows-Plattform erfolgt, folgen die erforderlichen Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="3f9bd-166">Visual Studio 2015 (bevorzugt) oder Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="3f9bd-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="3f9bd-167">Office-Entwicklungstools für Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f9bd-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="3f9bd-168">JavaScript-Sprache</span><span class="sxs-lookup"><span data-stu-id="3f9bd-168">JavaScript language</span></span>
    
<span data-ttu-id="3f9bd-169">Besuchen https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages Sie für eine Beispielanwendung.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="3f9bd-170">Sie können das Beispiel in wenigen einfachen Schritten herunterladen und ausführen:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="3f9bd-171">Herunterladen und Öffnen der Beispielanwendung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="3f9bd-172">Aktualisieren des SiteURL im Eigenschaftenfenster</span><span class="sxs-lookup"><span data-stu-id="3f9bd-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="3f9bd-173">Project Online untersucht sowohl den Anwendungsbereich des Add-Ins als auch die Benutzerberechtigungen für den Zugriff auf Informationen auf dem Project Online-Host.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="3f9bd-174">Wenn der Zugriff explizit in einer oder beiden Einstellungen verweigert wird, verweigert Project Online den Zugriff auf die Informationen.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="3f9bd-175">Andernfalls wird der Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="3f9bd-176">Aktivieren Sie [querladen](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="3f9bd-177">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-177">Build the project.</span></span>
    
5. <span data-ttu-id="3f9bd-178">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="3f9bd-179">Projektanbieter-gehostete Add-in-Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="3f9bd-180">Vom Anbieter gehostete Add-Ins sind Anwendungen, die auf einer beliebigen Webplattform geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="3f9bd-181">Sie können mithilfe der REST-API (oder CSOM für Microsoft-Plattformen) eine Verbindung herstellen und Datenvorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="3f9bd-182">Jede Sprache und Umgebung, die die REST-Schnittstelle unterstützt, kann für die Entwicklung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="3f9bd-183">Ein Beispiel für die Windows-Entwicklungsumgebung für diesen Anwendungstyp umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="3f9bd-184">Visual Studio 2015 (bevorzugt) oder Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="3f9bd-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="3f9bd-185">Microsoft Office-Entwicklungs Tools für Visual Studio (im Lieferumfang von Visual Studio 2015 Professional und Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="3f9bd-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="3f9bd-186">.NET Framework 4,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3f9bd-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="3f9bd-187">[SHAREPOINTONLINE CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe)</span><span class="sxs-lookup"><span data-stu-id="3f9bd-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="3f9bd-188">Eine Programmiersprache wie C#</span><span class="sxs-lookup"><span data-stu-id="3f9bd-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="3f9bd-189">Besuchen https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations Sie für funktionsfähige Beispielskripts.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="3f9bd-190">Sie können das Beispiel in wenigen Schritten ausführen:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="3f9bd-191">Herunterladen und Öffnen der Beispielanwendung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="3f9bd-192">Aktualisieren des SiteURL im Eigenschaftenfenster</span><span class="sxs-lookup"><span data-stu-id="3f9bd-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="3f9bd-193">Project Online untersucht sowohl den Anwendungsbereich des Add-Ins als auch die Benutzerberechtigungen für den Zugriff auf Informationen auf dem Project Online-Host.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="3f9bd-194">Wenn der Zugriff explizit in einer oder beiden Einstellungen verweigert wird, verweigert Project Online den Zugriff auf die Informationen.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="3f9bd-195">Andernfalls wird der Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="3f9bd-196">Aktivieren Sie [querladen](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="3f9bd-197">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-197">Build the project.</span></span>
    
5. <span data-ttu-id="3f9bd-198">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="3f9bd-199">Entwicklungsumgebung für externe/eigenständige Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3f9bd-199">External/standalone application development environment</span></span>

<span data-ttu-id="3f9bd-200">Eine eigenständige Anwendung kann Project Online mithilfe des Client seitigen Objektmodells (CSOM) oder REST für die Kommunikation mit Project Online aufrufen, um Informationen auf dem Server zu erstellen, abzurufen, zu aktualisieren und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="3f9bd-201">Hierbei handelt es sich um eine eigenständige Clientanwendung, die von der Benutzerzugriffsebene abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="3f9bd-202">Ein Beispiel für die Windows-Entwicklungsumgebung für diesen Anwendungstyp umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="3f9bd-203">Visual Studio 2015 (bevorzugt) oder Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="3f9bd-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="3f9bd-204">Microsoft Office-Entwicklungs Tools für Visual Studio (im Lieferumfang von Visual Studio 2015 Professional und Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="3f9bd-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="3f9bd-205">.NET Framework 4,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3f9bd-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="3f9bd-206">[SHAREPOINTONLINE CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe)</span><span class="sxs-lookup"><span data-stu-id="3f9bd-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="3f9bd-207">Eine Programmiersprache wie C#</span><span class="sxs-lookup"><span data-stu-id="3f9bd-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="3f9bd-208">Besuchen https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields Sie für eine Beispielanwendung.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="3f9bd-209">Sie können das Beispiel in wenigen Schritten ausführen:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="3f9bd-210">Herunterladen der Beispielanwendung</span><span class="sxs-lookup"><span data-stu-id="3f9bd-210">Download the sample application</span></span>
    
2. <span data-ttu-id="3f9bd-211">Führen Sie einige Änderungen aus, um auf Ihre Project Online-Website zuzugreifen: den Websitenamen, das Benutzerkonto und das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="3f9bd-212">Stellen Sie sicher, dass der Benutzer Zugriff auf alle Projekte hat.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="3f9bd-213">Project Online verwendet Benutzerberechtigungen, um den Zugriff auf Informationen im Datenspeicher zu steuern.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="3f9bd-214">Fügen Sie die SharePoint-Assembly den verweisen mithilfe der Nuget-Paket-Manager-Konsole hinzu, die im Menü Extras verfügbar ist, indem Sie Folgendes in der Nuget-Konsole eingeben:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="3f9bd-215">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-215">Build the project.</span></span>
    
5. <span data-ttu-id="3f9bd-216">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="3f9bd-217">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="3f9bd-217">Next steps</span></span>

<span data-ttu-id="3f9bd-218">Jede Beispielanwendung enthält einen Artikel, in dem die Highlights der Arbeit mit der einzelnen Projekt-API erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="3f9bd-219">Die Artikel werden in der folgenden Liste zusammen mit einigen Artikeln angezeigt, in denen die Entitätsbeziehungen, Informationen zum Abfragesystem und der Zugriff auf benutzerdefinierte Felder beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="3f9bd-220">Entwickeln einer Project Online-Anwendung mithilfe des Client seitigen Objektmodells</span><span class="sxs-lookup"><span data-stu-id="3f9bd-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="3f9bd-221">Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)</span><span class="sxs-lookup"><span data-stu-id="3f9bd-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="3f9bd-222">Zugriff auf benutzerdefinierte Project Online-Unternehmensfelder</span><span class="sxs-lookup"><span data-stu-id="3f9bd-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="3f9bd-223">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f9bd-223">See also</span></span>

<span data-ttu-id="3f9bd-224">Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="3f9bd-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

