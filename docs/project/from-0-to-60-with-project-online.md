---
title: Von 0 auf 100 mit Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Anwendungsentwickler kann eine Project Online Site (SharePoint gehostet) mithilfe von eigenständigen Applications und/oder Projekt-add-ins anpassen. Eine Vielzahl von Clientanwendungen ist möglich, die im Bereich von Adressierung Beteiligten in einem Projekt auf PMO Support-Funktionen, beispielsweise eine der folgenden Anforderungen:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392585"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="c1ca2-103">Von 0 auf 100 mit Project Online</span><span class="sxs-lookup"><span data-stu-id="c1ca2-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="c1ca2-104">Anwendungsentwickler kann eine Project Online Site (SharePoint gehostet) mithilfe von eigenständigen Applications und/oder Projekt-add-ins anpassen. Eine Vielzahl von Clientanwendungen ist möglich, die im Bereich von Adressierung Beteiligten in einem Projekt auf PMO Support-Funktionen, beispielsweise eine der folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="c1ca2-105">Optimierte Zeitkarte Dateneingabe für Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="c1ca2-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="c1ca2-106">Effiziente Zeitkarte Genehmigung für Vorgesetzte</span><span class="sxs-lookup"><span data-stu-id="c1ca2-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="c1ca2-107">Aufsicht über ermöglicht (Beschaffung und Status) für ein Projekt erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="c1ca2-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="c1ca2-108">Status/Überprüfung des aktiven Projekte</span><span class="sxs-lookup"><span data-stu-id="c1ca2-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="c1ca2-109">Problembericht</span><span class="sxs-lookup"><span data-stu-id="c1ca2-109">Issues report</span></span>
- <span data-ttu-id="c1ca2-110">Ändern von Management Statusbericht</span><span class="sxs-lookup"><span data-stu-id="c1ca2-110">Change Management Status report</span></span>
    
<span data-ttu-id="c1ca2-111">Project Online enthält die API-Unterstützung, um die folgenden Szenarien zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="c1ca2-112">Für ein Projekt (SharePoint) gehostet add-in:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="c1ca2-113">Code (JavaScript, HTML, CSS), die in SharePoint Online gehostet wird</span><span class="sxs-lookup"><span data-stu-id="c1ca2-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="c1ca2-114">Anlagen, die in den Browser heruntergeladen und in SharePoint Online ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="c1ca2-115">Geschäftslogik in JavaScript</span><span class="sxs-lookup"><span data-stu-id="c1ca2-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="c1ca2-116">Zugreifen auf Daten, die in/gespeichert in Project Online oder SharePoint wie (aber nicht beschränkt auf):</span><span class="sxs-lookup"><span data-stu-id="c1ca2-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="c1ca2-117">Benutzerdefinierte Felder</span><span class="sxs-lookup"><span data-stu-id="c1ca2-117">Custom fields</span></span>  
  - <span data-ttu-id="c1ca2-118">Listen</span><span class="sxs-lookup"><span data-stu-id="c1ca2-118">Lists</span></span>
    
- <span data-ttu-id="c1ca2-119">Für ein Projekt (SharePoint) vom Anbieter gehosteten add-in:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="c1ca2-120">Code, der auf einer Website, die außerhalb der Project Online-Website vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="c1ca2-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="c1ca2-121">Eine externe Website, die werden kann (jedoch nicht auf beschränkt ist):</span><span class="sxs-lookup"><span data-stu-id="c1ca2-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="c1ca2-122">Anderen SharePoint-Website</span><span class="sxs-lookup"><span data-stu-id="c1ca2-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="c1ca2-123">App/Webdienst integriert auf einer beliebigen Plattform</span><span class="sxs-lookup"><span data-stu-id="c1ca2-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="c1ca2-124">Die externe Website enthält die Geschäftslogik</span><span class="sxs-lookup"><span data-stu-id="c1ca2-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="c1ca2-125">Der Browser wird von Project Online an externe Website mit Zugriffstoken mit Project Online umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="c1ca2-126">Die externe Website kann Anrufe auf SharePoint und Project Online tätigen.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="c1ca2-127">Für eine externe/Standalone-add-in:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="c1ca2-128">Benutzer führt eine Anwendung auf ihrem Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-128">User executes an application on their device</span></span>
  - <span data-ttu-id="c1ca2-129">Anwendung authentifiziert und Project Online-APIs direkt anrufen</span><span class="sxs-lookup"><span data-stu-id="c1ca2-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="c1ca2-130">Art der Anwendung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-130">Type of application</span></span>|<span data-ttu-id="c1ca2-131">API-Implementierung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-131">API implementation</span></span>|<span data-ttu-id="c1ca2-132">Zielumgebung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-132">Target environment</span></span>|<span data-ttu-id="c1ca2-133">Beispiele für die Anwendung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c1ca2-134">Projekt gehostet</span><span class="sxs-lookup"><span data-stu-id="c1ca2-134">Project hosted</span></span>  <br/> |<span data-ttu-id="c1ca2-135">JSOM (Java Script-Objektmodell)</span><span class="sxs-lookup"><span data-stu-id="c1ca2-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="c1ca2-136">REST</span><span class="sxs-lookup"><span data-stu-id="c1ca2-136">REST</span></span>  <br/> |<span data-ttu-id="c1ca2-137">Browser</span><span class="sxs-lookup"><span data-stu-id="c1ca2-137">Browser</span></span>  <br/> |<span data-ttu-id="c1ca2-138">Zeitkarteneintrag</span><span class="sxs-lookup"><span data-stu-id="c1ca2-138">Timecard entry</span></span>  <br/> <span data-ttu-id="c1ca2-139">Zeitkarte Genehmigung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-139">Timecard approval</span></span>  <br/> <span data-ttu-id="c1ca2-140">Projektstatus</span><span class="sxs-lookup"><span data-stu-id="c1ca2-140">Project Status</span></span>  <br/> <span data-ttu-id="c1ca2-141">Problembericht</span><span class="sxs-lookup"><span data-stu-id="c1ca2-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="c1ca2-142">Project-Anbieter gehostet</span><span class="sxs-lookup"><span data-stu-id="c1ca2-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="c1ca2-143">CSOM-Clientbibliothek</span><span class="sxs-lookup"><span data-stu-id="c1ca2-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="c1ca2-144">Azure-Website-App</span><span class="sxs-lookup"><span data-stu-id="c1ca2-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="c1ca2-145">Nicht-Windows-Umgebung (LAMP usw.)</span><span class="sxs-lookup"><span data-stu-id="c1ca2-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="c1ca2-146">Externe Arbeitszeittabelle validator</span><span class="sxs-lookup"><span data-stu-id="c1ca2-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="c1ca2-147">Projekt zu verwendenden Importprogramms</span><span class="sxs-lookup"><span data-stu-id="c1ca2-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="c1ca2-148">Extern/eigenständige</span><span class="sxs-lookup"><span data-stu-id="c1ca2-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="c1ca2-149">REST</span><span class="sxs-lookup"><span data-stu-id="c1ca2-149">REST</span></span>  <br/> <span data-ttu-id="c1ca2-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="c1ca2-150">CSOM</span></span>  <br/> |<span data-ttu-id="c1ca2-151">REST - jeder Plattform</span><span class="sxs-lookup"><span data-stu-id="c1ca2-151">REST - any platform</span></span>  <br/> <span data-ttu-id="c1ca2-152">CSOM - jeder .NET unterstützten Plattform</span><span class="sxs-lookup"><span data-stu-id="c1ca2-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="c1ca2-153">Zeitkarteneintrag</span><span class="sxs-lookup"><span data-stu-id="c1ca2-153">Timecard entry</span></span>  <br/> <span data-ttu-id="c1ca2-154">Migration von Projekten zu einem neuen Standort</span><span class="sxs-lookup"><span data-stu-id="c1ca2-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="c1ca2-155">Ändern Sie Verwaltungsstatus.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="c1ca2-156">Was dauert es der Entwicklung von Anwendungen für Project Online beginnen?</span><span class="sxs-lookup"><span data-stu-id="c1ca2-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="c1ca2-157">Die gemeinsame Elemente für das Entwickeln von Project Online-Applikationen erforderlich sind ein Konto mit Project Online und Testdaten – Projekte und projektbezogenen Informationen, die Zuordnungen, Aufgaben, Ressourcen und benutzerdefinierte Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="c1ca2-158">Eine Entwicklungsumgebung ist auch erforderlich, aber Einzelheiten der Development Environment hängt vom Typ der Anwendung und der API-Schnittstelle für die Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="c1ca2-159">Die nächsten Abschnitten werden die Entwicklung von Anforderungen für die drei API-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="c1ca2-160">Referenzdokumentation für die beschreibt das Objektmodell, die für alle drei Schnittstellen als auch eine Entität-Zuordnung, die Beziehungen zwischen den Komponenten der Objekt-Modell anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="c1ca2-161">Projekt-add-in-Entwicklungsumgebung gehostet</span><span class="sxs-lookup"><span data-stu-id="c1ca2-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="c1ca2-162">Eine gehostete-Add-in ist ein Add-in, die auf dem Server befindet und an einen Browser für die Ausführung zur Laufzeit heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="c1ca2-163">Gehostete-add-ins können die JSOM oder REST-Schnittstelle und in JavaScript geschrieben.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="c1ca2-164">Project Online enthält Verweise auf die JSOM-Bibliothek für die Ausführung zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="c1ca2-165">Wird vorausgesetzt Entwicklung befindet sich in einer Windows-Plattform, die benötigten Ressourcen gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="c1ca2-166">Visual Studio 2015 (empfohlen) oder Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c1ca2-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="c1ca2-167">Office-Entwicklungstools für Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c1ca2-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="c1ca2-168">JavaScript-Sprache</span><span class="sxs-lookup"><span data-stu-id="c1ca2-168">JavaScript language</span></span>
    
<span data-ttu-id="c1ca2-169">Besuchen Sie https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages für eine beispielanwendung.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="c1ca2-170">Sie können herunterladen und Ausführen des Beispiels in ein paar einfachen Schritten:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="c1ca2-171">Herunterladen Sie und öffnen Sie die beispielanwendung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="c1ca2-172">Aktualisieren Sie das SiteURL im Fenster Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1ca2-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="c1ca2-173">Project Online untersucht sowohl die Anwendungsbereich des Add-Ins und die Berechtigungen eines Benutzers mit Zugriff auf Informationen auf dem Project Online-Host gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="c1ca2-174">Wenn in einer oder beide Einstellungen explizit Zugriff verweigert wird, verweigert Project Online Zugriff auf Informationen.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="c1ca2-175">Andernfalls wird der Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="c1ca2-176">[Sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="c1ca2-177">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-177">Build the project.</span></span>
    
5. <span data-ttu-id="c1ca2-178">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="c1ca2-179">Projekt-add-in Entwicklung vom Anbieter gehostete Umgebung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="c1ca2-180">Vom Anbieter gehosteten-add-ins sind Applications geschrieben und auf allen Plattformen Web darstellen.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="c1ca2-181">Sie können eine Verbindung herstellen und Datenvorgänge mithilfe der REST (oder CSOM für Microsoft-Plattformen) API.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="c1ca2-182">Jede Sprache und die Umgebung, die die REST-Schnittstelle unterstützt können für die Entwicklung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="c1ca2-183">Ein Beispiel für die Windows-Entwicklungsumgebung für diese Art Anwendung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="c1ca2-184">Visual Studio 2015 (empfohlen) oder Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c1ca2-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="c1ca2-185">Microsoft Office-Entwicklungstools für Visual Studio (im Lieferumfang von Visual Studio 2015 Professional- und Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="c1ca2-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="c1ca2-186">.NET Framework 4.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c1ca2-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="c1ca2-187">[SharePoint Online-CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe)</span><span class="sxs-lookup"><span data-stu-id="c1ca2-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="c1ca2-188">Eine Programmiersprache wie c#</span><span class="sxs-lookup"><span data-stu-id="c1ca2-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="c1ca2-189">Besuchen Sie https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations für Beispielskripts arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="c1ca2-190">Sie können das Beispiel in wenigen Schritten ausführen:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="c1ca2-191">Herunterladen Sie und öffnen Sie die beispielanwendung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="c1ca2-192">Aktualisieren Sie das SiteURL im Fenster Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1ca2-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="c1ca2-193">Project Online untersucht sowohl die Anwendungsbereich des Add-Ins und die Berechtigungen eines Benutzers mit Zugriff auf Informationen auf dem Project Online-Host gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="c1ca2-194">Wenn in einer oder beide Einstellungen explizit Zugriff verweigert wird, verweigert Project Online Zugriff auf Informationen.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="c1ca2-195">Andernfalls wird der Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="c1ca2-196">[Sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="c1ca2-197">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-197">Build the project.</span></span>
    
5. <span data-ttu-id="c1ca2-198">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="c1ca2-199">Extern/eigenständige Anwendung-Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="c1ca2-199">External/standalone application development environment</span></span>

<span data-ttu-id="c1ca2-200">Eine eigenständige Anwendung kann rufen Sie Project Online mit dem Client Side-Objekt Objektmodell (CSOM) oder REST kommunizieren mit Project Online erstellen, abrufen, aktualisieren und Löschen von Informationen, die sich auf dem Server befinden.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="c1ca2-201">Dies ist eine eigenständige-Clientanwendung, die Zugriff auf Benutzerebene ausgeführt abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="c1ca2-202">Ein Beispiel für die Windows-Entwicklungsumgebung für diese Art Anwendung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="c1ca2-203">Visual Studio 2015 (empfohlen) oder Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c1ca2-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="c1ca2-204">Microsoft Office-Entwicklungstools für Visual Studio (im Lieferumfang von Visual Studio 2015 Professional- und Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="c1ca2-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="c1ca2-205">.NET Framework 4.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c1ca2-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="c1ca2-206">[SharePoint Online-CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe)</span><span class="sxs-lookup"><span data-stu-id="c1ca2-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="c1ca2-207">Eine Programmiersprache wie c#</span><span class="sxs-lookup"><span data-stu-id="c1ca2-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="c1ca2-208">Besuchen Sie https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields für eine beispielanwendung.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="c1ca2-209">Sie können das Beispiel in wenigen Schritten ausführen:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="c1ca2-210">Laden Sie die beispielanwendung aus</span><span class="sxs-lookup"><span data-stu-id="c1ca2-210">Download the sample application</span></span>
    
2. <span data-ttu-id="c1ca2-211">Stellen Sie eine Reihe von Änderungen an Ihrer Project Online-Website zugreifen – den Namen des Standorts, Benutzerkonto und Kennwort.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="c1ca2-212">Stellen Sie sicher, dass der Benutzer Zugriff auf alle Projekte.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="c1ca2-213">Project Online verwendet Benutzerberechtigungen zum Zugriff auf Informationen im Datenspeicher steuern.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="c1ca2-214">Fügen Sie die Verweise mit der Nuget Package Manager-Konsole zur Verfügung, indem Sie Folgendes in der Konsole Nuget eingeben im Menü Extras die SharePoint-Assembly hinzu:</span><span class="sxs-lookup"><span data-stu-id="c1ca2-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="c1ca2-215">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-215">Build the project.</span></span>
    
5. <span data-ttu-id="c1ca2-216">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="c1ca2-217">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c1ca2-217">Next steps</span></span>

<span data-ttu-id="c1ca2-218">Jede beispielanwendung verfügt über einen Artikel erläutern die wichtigsten arbeiten mit der einzelnen Project-API.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="c1ca2-219">Die Artikel in der folgenden Liste zusammen mit ein paar Artikeln, die entitätsbeziehungen Informationen zu den Abfragesystem und den Zugriff auf benutzerdefinierte Felder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c1ca2-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="c1ca2-220">Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell</span><span class="sxs-lookup"><span data-stu-id="c1ca2-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="c1ca2-221">Entwickeln eines Project Online add-Ins mithilfe der JavaScript-Objektmodell (JSOM)</span><span class="sxs-lookup"><span data-stu-id="c1ca2-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="c1ca2-222">Zugriff auf benutzerdefinierte Project Online-Unternehmensfelder</span><span class="sxs-lookup"><span data-stu-id="c1ca2-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="c1ca2-223">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1ca2-223">See also</span></span>

<span data-ttu-id="c1ca2-224">Dokumentation und Beispiele im Zusammenhang mit Project Online und die Anwendungsentwicklung mithilfe von CSOM finden Sie im [Projekt Development Portal](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="c1ca2-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

