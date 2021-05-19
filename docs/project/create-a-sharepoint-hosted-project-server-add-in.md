---
title: Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Von den drei Arten von Apps, die Sie für Project Online erstellen können (automatisch gehostet, vom Anbieter gehostet und SharePoint gehostet), ist die von SharePoint gehostete App die einfachste, die sie erstellen und bereitstellen kann.
ms.openlocfilehash: 9b3b41eda40a8419ad72f11bb474acf7acaf81e9
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773757"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a><span data-ttu-id="69ef7-103">Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="69ef7-103">Create a SharePoint-hosted Project Server add-in</span></span>

<span data-ttu-id="69ef7-104">Von den drei Arten von Apps, die Sie für Project Online erstellen können (automatisch gehostet, vom Anbieter gehostet und SharePoint gehostet), ist die von SharePoint gehostete App die einfachste, die sie erstellen und bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="69ef7-104">Of the three types of apps that you can create for Project Online (autohosted, provider-hosted, and SharePoint-hosted), the SharePoint-hosted app is the simplest to create and deploy.</span></span> <span data-ttu-id="69ef7-105">Eine SharePoint-gehostete App erfordert keine OAuth-Authentifizierung und verwendet weder Azure noch eine lokale Website für die vom Anbieter gehosteten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-105">A SharePoint-hosted app does not require OAuth authentication, and does not use Azure or require maintenance of a local site for the provider-hosted resources.</span></span> <span data-ttu-id="69ef7-106">Die **App für SharePoint 2013-Vorlage** in Visual Studio ist ein praktisches Framework für die Entwicklung von Apps, die im Office Store veröffentlicht und verkauft oder in einem privaten App-Katalog auf SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69ef7-106">The **App for SharePoint 2013** template in Visual Studio is a convenient framework for developing apps that can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> 
  
<span data-ttu-id="69ef7-107">In Project ist statusing ein Prozess, bei dem ein Teammitglied die Seite Aufgaben in Project Web App verwenden kann, um den Status eines zugewiesenen Vorgangs zu übermitteln, z. B. die Anzahl der Arbeitsstunden, die an jedem Tag einer Woche für die Arbeit an der Aufgabe gearbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-107">In Project, statusing is a process where a team member can use the Tasks page in Project Web App to submit the status of an assigned task, such as the number of hours worked each day of a week spent working on the task.</span></span> <span data-ttu-id="69ef7-108">Der Zuweisungsbesitzer (in der Regel der Projektmanager) kann den Status genehmigen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-108">The assignment owner (usually the project manager) can approve or reject the status.</span></span> <span data-ttu-id="69ef7-109">Wenn der Status genehmigt wird, Project Den Zeitplan neu berechnen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-109">When the status is approved, Project recalculates the schedule.</span></span> <span data-ttu-id="69ef7-110">Die **QuickStatus-App** zeigt zugewiesene Aufgaben an, bei denen der Benutzer den Abgeschlossenen Prozentstand schnell aktualisieren und den Status der ausgewählten Zuordnungen zur Genehmigung übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="69ef7-110">The **QuickStatus** app displays assigned tasks, where the user can quickly update percent complete and submit status of the selected assignments for approval.</span></span> <span data-ttu-id="69ef7-111">Obwohl die Seite Aufgaben in Project Web App wesentlich mehr Funktionalität bietet, ist die **QuickStatus-App** ein Beispiel, das eine vereinfachte Benutzeroberfläche bietet.</span><span class="sxs-lookup"><span data-stu-id="69ef7-111">Although the Tasks page in Project Web App has much more functionality, the **QuickStatus** app is an example that provides a simplified interface.</span></span> 
  
<span data-ttu-id="69ef7-112">Die **QuickStatus-App** ist ein Beispiel für Entwickler. Es ist nicht für die Verwendung in einer Produktionsumgebung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-112">The **QuickStatus** app is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="69ef7-113">Der hauptzweck ist es, ein Beispiel für die App-Entwicklung für Project Online zu zeigen, nicht um eine voll funktionsfähige Status-App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-113">The primary purpose is to show an example of app development for Project Online, not to create a fully functional statusing app.</span></span> <span data-ttu-id="69ef7-114">Einen besseren Ansatz für die Statusanzeige finden Sie in der Empfehlung unter [Nächste Schritte](#pj15_StatusingApp_NextSteps).</span><span class="sxs-lookup"><span data-stu-id="69ef7-114">For a better approach to statusing, see the recommendation in [Next steps](#pj15_StatusingApp_NextSteps).</span></span>
  
<span data-ttu-id="69ef7-115">Allgemeine Informationen zum Status finden Sie unter [Vorgangsfortschritt](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span><span class="sxs-lookup"><span data-stu-id="69ef7-115">For general information about statusing, see [Task progress](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span></span> <span data-ttu-id="69ef7-116">Weitere Informationen zum Entwickeln von Add-Ins für SharePoint und Project Server finden Sie unter [SharePoint Add-Ins](https://msdn.microsoft.com/library/jj163230.aspx).</span><span class="sxs-lookup"><span data-stu-id="69ef7-116">For more information about developing add-ins for SharePoint and Project Server, see [SharePoint Add-ins](https://msdn.microsoft.com/library/jj163230.aspx).</span></span>

<span data-ttu-id="69ef7-117"><a name="pj15_StatusingApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-117"><a name="pj15_StatusingApp_Prerequisites"> </a></span></span>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a><span data-ttu-id="69ef7-118">Voraussetzungen für das Erstellen einer App für Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="69ef7-118">Prerequisites for creating an app for Project Server 2013</span></span>

<span data-ttu-id="69ef7-119">Um relativ einfache Apps zu entwickeln, die auf Project Online oder in einer lokalen Installation von Project Server 2013 bereitgestellt werden können, können Sie die Napa verwenden, die eine Onlineentwicklungsumgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-119">To develop relatively simple apps that can be deployed to Project Online or to an on-premises installation of Project Server 2013, you can use the Napa, which provide an online development environment.</span></span> <span data-ttu-id="69ef7-120">Für komplexere Apps, das Ändern des Project Web App-Menübands und ein einfacheres Debuggen während der Entwicklung können Sie Visual Studio 2012 oder Visual Studio 2013.</span><span class="sxs-lookup"><span data-stu-id="69ef7-120">For more complex apps, modifying the Project Web App ribbon, and easier debugging during development, you can use Visual Studio 2012 or Visual Studio 2013.</span></span> <span data-ttu-id="69ef7-121">Bei einer lokalen Installation können Sie z. B. die Drafts-Datentabellen manuell auf Änderungen in der Project überprüfen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-121">For example, with an on-premises installation, you can manually check the Drafts datatables for changes in the Project Server database.</span></span> <span data-ttu-id="69ef7-122">In diesem Artikel wird gezeigt, wie Sie die App-Entwicklung mit Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="69ef7-122">This article shows how to do app development with Visual Studio.</span></span>
  
<span data-ttu-id="69ef7-123">Die Entwicklung Project Server-Apps mit Visual Studio erfordert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="69ef7-123">Development of Project Server apps with Visual Studio requires the following:</span></span>
  
- <span data-ttu-id="69ef7-p106">Stellen Sie sicher, dass Sie die neuesten Service Packs und Windows-Updates auf dem lokalen Entwicklungscomputer installiert haben. Als Betriebssystem kann Windows 7, Windows 8, Windows Server 2008 oder Windows Server 2012 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-p106">Ensure that you have installed the most recent service packs and Windows updates on your local development computer. The operating system can be Windows 7, Windows 8, Windows Server 2008, or Windows Server 2012.</span></span>
    
- <span data-ttu-id="69ef7-126">Sie müssen einen Computer mit SharePoint Server 2013 und Project Server 2013 installiert haben, auf dem der Computer für die App-Isolation und das Querladen von Apps konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-126">You must have a computer that has SharePoint Server 2013 and Project Server 2013 installed, where the computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="69ef7-127">Das Querladen ermöglicht Visual Studio, die App vorübergehend zum Debuggen zu installieren.</span><span class="sxs-lookup"><span data-stu-id="69ef7-127">Sideloading enables Visual Studio to temporarily install the app for debugging.</span></span> <span data-ttu-id="69ef7-128">Sie können eine lokale Installation von SharePoint server Project verwenden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-128">You can use an on-premises installation of SharePoint and Project Server.</span></span> <span data-ttu-id="69ef7-129">Weitere Informationen finden Sie unter Einrichten einer lokalen Entwicklungsumgebung [für Apps für SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="69ef7-129">For more information, see [Set up an on-premises development environment for apps for SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="69ef7-130">Konfigurieren Sie für eine lokale Installation eine isolierte App-Domäne,  *bevor*  Sie einen Unternehmens-App-Katalog erstellen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-130">For an on-premises installation, configure an isolated app domain  *before*  you create a corporate app catalog.</span></span> 
  
- <span data-ttu-id="69ef7-131">Der Entwicklungscomputer kann ein Remotecomputer sein, auf dem Office Entwicklertools für Visual Studio 2012 installiert sind.</span><span class="sxs-lookup"><span data-stu-id="69ef7-131">The development computer can be a remote computer that has Office Developer Tools for Visual Studio 2012 installed.</span></span> <span data-ttu-id="69ef7-132">Stellen Sie sicher, dass Sie die neueste Version installiert haben. weitere Informationen *finden* Sie im Abschnitt [Extras](https://msdn.microsoft.com/office/apps/fp123627.aspx)der Apps für Office und SharePoint Downloads .</span><span class="sxs-lookup"><span data-stu-id="69ef7-132">Ensure that you have installed the most recent version; see the  *Tools*  section of the [Apps for Office and SharePoint downloads](https://msdn.microsoft.com/office/apps/fp123627.aspx).</span></span>
    
- <span data-ttu-id="69ef7-133">Stellen Sie sicher, Project Web App-Instanz, die Sie für die Entwicklung und tests verwenden, im Browser verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-133">Verify that the Project Web App instance you will be using for development and testing is accessible in the browser.</span></span>
    
<span data-ttu-id="69ef7-134">Informationen zur Verwendung der Onlinetools finden Sie unter Einrichten einer Umgebung für die Entwicklung von Apps [für SharePoint auf Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span><span class="sxs-lookup"><span data-stu-id="69ef7-134">For information about using the online tools, see [Set up an environment for developing apps for SharePoint on Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span></span> <span data-ttu-id="69ef7-135">Eine exemplarische Vorgehensweise zum Erstellen einer einfachen App für Project Server, die die Onlinetools verwendet, finden Sie in der EPMSource-Blogreihe Erstellen Ihrer ersten Project [Server-App.](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/)</span><span class="sxs-lookup"><span data-stu-id="69ef7-135">For a walkthrough of building a simple app for Project Server that uses the online tools, see the EPMSource blog series, [Building your first Project Server app](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).</span></span>

<span data-ttu-id="69ef7-136"><a name="pj15_StatusingApp_UsingVisualStudio"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-136"><a name="pj15_StatusingApp_UsingVisualStudio"> </a></span></span>

## <a name="using-visual-studio-to-create-a-project-server-app"></a><span data-ttu-id="69ef7-137">Verwenden Visual Studio zum Erstellen einer Project Server-App</span><span class="sxs-lookup"><span data-stu-id="69ef7-137">Using Visual Studio to create a Project Server app</span></span>

<span data-ttu-id="69ef7-138">Office Developer Tools for Visual Studio 2012 enthält eine Vorlage für SharePoint Apps, die mit Project Server 2013 verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="69ef7-138">Office Developer Tools for Visual Studio 2012 includes a template for SharePoint apps that can be used with Project Server 2013.</span></span> <span data-ttu-id="69ef7-139">Wenn Sie eine App-Lösung erstellen, enthält die Lösung die folgenden Dateien für Ihren benutzerdefinierten Code:</span><span class="sxs-lookup"><span data-stu-id="69ef7-139">When you create an app solution, the solution includes the following files for your custom code:</span></span>
  
- <span data-ttu-id="69ef7-140">**AppManifest.xml** enthält Einstellungen für den App-Titel, den Berechtigungsanforderungsbereich und andere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69ef7-140">**AppManifest.xml** includes settings for the app title, permission request scope, and other properties.</span></span> <span data-ttu-id="69ef7-141">Prozedur 1 enthält Schritte zum Festlegen der Eigenschaften mithilfe des Manifest-Designers.</span><span class="sxs-lookup"><span data-stu-id="69ef7-141">Procedure 1 includes steps to set the properties by using the Manifest Designer.</span></span> 
    
- <span data-ttu-id="69ef7-142">**Default.aspx** im Ordner Seiten ist die Hauptseite der App.</span><span class="sxs-lookup"><span data-stu-id="69ef7-142">**Default.aspx** in the Pages folder is the main page of the app.</span></span> <span data-ttu-id="69ef7-143">In Prozedur 2 wird gezeigt, wie Sie HTML5-Inhalte für die **QuickStatus-App** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-143">Procedure 2 shows how to add HTML5 content for the **QuickStatus** app.</span></span> 
    
- <span data-ttu-id="69ef7-144">**App.js** im Ordner Skripts ist die primäre Datei für den benutzerdefinierten JavaScript-Code.</span><span class="sxs-lookup"><span data-stu-id="69ef7-144">**App.js** in the Scripts folder is the primary file for the custom JavaScript code.</span></span> <span data-ttu-id="69ef7-145">In Prozedur 3 wird der JavaScript-Code für die **QuickStatus-App** erläutert.</span><span class="sxs-lookup"><span data-stu-id="69ef7-145">Procedure 3 explains the JavaScript code for the **QuickStatus** app.</span></span> 
    
   <span data-ttu-id="69ef7-146">Wenn Sie kommerzielle Steuerelemente wie ein jQuery-basiertes Raster oder eine Datumsauswahl hinzufügen, können Sie Verweise auf zusätzliche JavaScript-Dateien in der Datei Default.aspx hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-146">If you add commercial controls such as a jQuery-based grid or date picker, you can add references to additional JavaScript files in the Default.aspx file.</span></span>
    
- <span data-ttu-id="69ef7-147">**App.css** im Ordner Inhalt ist die primäre Datei für benutzerdefinierte CSS3-Formatvorlagen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-147">**App.css** in the Content folder is the primary file for custom CSS3 styles.</span></span> <span data-ttu-id="69ef7-148">Prozedur 2 und Prozedur 3 enthalten Informationen zu Cascading Stylesheets (CSS)-Formatvorlagen für die **QuickStatus-App.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-148">Procedure 2 and Procedure 3 include information about cascading style sheets (CSS) styles for the **QuickStatus** app.</span></span> <span data-ttu-id="69ef7-149">Sie können Verweise auf zusätzliche CSS-Dateien in der Datei "Default.aspx" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-149">You can add references to additional CSS files in the Default.aspx file.</span></span> 
    
- <span data-ttu-id="69ef7-150">**AppIcon.png** im Ordner Bilder ist das 96 x 96-Symbol, das die App im Office Store oder im App-Katalog anzeigt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-150">**AppIcon.png** in the Images folder is the 96 x 96 icon that the app displays in the Office Store or the app catalog.</span></span> 
    
<span data-ttu-id="69ef7-151">Zum Ändern des Project Web App-Menübands können Sie eine benutzerdefinierte Menübandaktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-151">To modify the Project Web App ribbon, you can add a ribbon custom action.</span></span> <span data-ttu-id="69ef7-152">Der Beispielcode für den [Abschnitt QuickStatus-App](#pj15_StatusingApp_Example) enthält den vollständigen Code für die geänderten Dateien Default.aspx, App.js, App.css, Elements.xml und AppManifest.xml Dateien.</span><span class="sxs-lookup"><span data-stu-id="69ef7-152">The [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section includes the complete code for the modified Default.aspx, App.js, App.css, Elements.xml, and AppManifest.xml files.</span></span> 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a><span data-ttu-id="69ef7-153">Vorgehensweise 1:</span><span class="sxs-lookup"><span data-stu-id="69ef7-153">Procedure 1.</span></span> <span data-ttu-id="69ef7-154">So erstellen Sie ein App-Projekt in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="69ef7-154">To create an app project in Visual Studio</span></span>

1. <span data-ttu-id="69ef7-155">Führen Visual Studio 2012 als Administrator aus, und wählen Sie dann auf der Startseite **Project** Neue Option aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-155">Run Visual Studio 2012 as an administrator, and then select **New Project** on the Start page.</span></span> 
    
2. <span data-ttu-id="69ef7-156">Erweitern Sie **im Dialogfeld Project** die Knoten **Vorlagen**, **Visual C#** und **Office/SharePoint,** und wählen Sie **dann Apps aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-156">In the **New Project** dialog box, expand the **Templates**, **Visual C#**, and **Office/SharePoint** nodes, and then select **Apps**.</span></span> <span data-ttu-id="69ef7-157">Verwenden Sie die **Standardeinstellung .NET Framework 4.5** in der Dropdownliste Zielframework am oberen Rand des Mittelbereichs, und wählen Sie dann **App für SharePoint 2013** aus (siehe Abbildung 1).</span><span class="sxs-lookup"><span data-stu-id="69ef7-157">Use the default **.NET Framework 4.5** in the target framework drop-down list at the top of the center pane, and then select **App for SharePoint 2013** (see Figure 1).</span></span> 
    
3. <span data-ttu-id="69ef7-158">Geben Sie **im Feld Name** QuickStatus ein, navigieren Sie zu dem Speicherort, an dem Sie die App speichern möchten, und wählen Sie dann OK **aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-158">In the **Name** field, type QuickStatus, browse to the location where you want to save the app, and then choose **OK**.</span></span>
    
   <span data-ttu-id="69ef7-159">**Abbildung 1. Erstellen einer Project Server-App in Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="69ef7-159">**Figure 1. Creating a Project Server app in Visual Studio**</span></span>

   <span data-ttu-id="69ef7-160">![Erstellen einer Project Server-App in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Erstellen einer Project Server-App in Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="69ef7-160">![Creating a Project Server app in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Creating a Project Server app in Visual Studio")</span></span>
  
4. <span data-ttu-id="69ef7-161">Füllen Sie **im Dialogfeld Neue App für SharePoint** die folgenden drei Felder aus:</span><span class="sxs-lookup"><span data-stu-id="69ef7-161">In the **New app for SharePoint** dialog box, fill in the following three fields:</span></span> 
    
   - <span data-ttu-id="69ef7-162">Geben Sie im oberen Textfeld den Namen ein, den die App in der Project anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="69ef7-162">In the top text box, type the name that you want the app to display in Project Web App.</span></span> <span data-ttu-id="69ef7-163">Geben Sie beispielsweise Quick Status Update ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-163">For example, type Quick Status Update.</span></span>
    
   - <span data-ttu-id="69ef7-164">Geben Sie für die Website, die zum Debuggen verwendet werden soll, die URL der Project Web App-Instanz ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-164">For the site to use for debugging, type the URL of the Project Web App instance.</span></span> <span data-ttu-id="69ef7-165">Geben Sie beispielsweise `https://ServerName/ProjectServerName` ein (ersetzen _Sie ServerName_ und _ProjectServerName_ durch Eigene Werte), und wählen Sie dann **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-165">For example, type  `https://ServerName/ProjectServerName` (replacing  _ServerName_ and  _ProjectServerName_ with your own values), and then choose **Validate**.</span></span> <span data-ttu-id="69ef7-166">Wenn alles gut geht, zeigt Visual Studio **Verbindung erfolgreich an.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-166">If all goes well, Visual Studio shows **Connection successful**.</span></span> <span data-ttu-id="69ef7-167">Wenn Sie eine Fehlermeldung erhalten, stellen Sie sicher, dass die Project Web App-URL korrekt ist und dass der Project Server-Computer für die App-Isolation und das Querladen von Apps konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-167">If you get an error message, ensure that the Project Web App URL is correct and that the Project Server computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="69ef7-168">Weitere Informationen finden Sie im Abschnitt Voraussetzungen für das Erstellen einer [App für Project Server 2013.](#pj15_StatusingApp_Prerequisites)</span><span class="sxs-lookup"><span data-stu-id="69ef7-168">For more information, see the [Prerequisites for creating an app for Project Server 2013](#pj15_StatusingApp_Prerequisites) section.</span></span> 
    
   - <span data-ttu-id="69ef7-169">Wählen Sie **in der Dropdownliste** How do you want to host your app for SharePoint die Option SharePoint gehostet **aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-169">In the **How do you want to host your app for SharePoint** drop-down list, choose **SharePoint-hosted**.</span></span>
    
   > [!CAUTION]
   > <span data-ttu-id="69ef7-170">Wenn Sie den standardmäßigen vom Anbieter gehosteten Projekttyp aus Versehen auswählen, erstellt Visual Studio zwei Projekte in der Projektmappe: ein **QuickStatus-Projekt** und ein **QuickStatusWeb-Projekt.** </span><span class="sxs-lookup"><span data-stu-id="69ef7-170">If you choose the default **Provider-hosted** project type by mistake, Visual Studio creates two projects in the solution: a **QuickStatus** project and a **QuickStatusWeb** project.</span></span> <span data-ttu-id="69ef7-171">Wenn zwei Projekte zu sehen sind, löschen Sie diese Lösung, und starten Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="69ef7-171">If you see two projects, delete that solution and start again.</span></span> 
  
5. <span data-ttu-id="69ef7-172">Wählen **Sie OK** aus, um die **QuickStatus-Lösung,** **das QuickStatus-Projekt** und die Standarddateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-172">Choose **OK** to create the **QuickStatus** solution, **QuickStatus** project, and default files.</span></span> 
    
6. <span data-ttu-id="69ef7-173">Öffnen Sie die Manifest-Designer-Ansicht (doppelklicken Sie z. B. auf die AppManifest.xml Datei).</span><span class="sxs-lookup"><span data-stu-id="69ef7-173">Open the Manifest Designer view (for example, double-click the AppManifest.xml file).</span></span> <span data-ttu-id="69ef7-174">Auf der **Registerkarte Allgemein** sollte im Textfeld **Titel** der App-Name angezeigt werden, den Sie in Schritt 4 eingeben.</span><span class="sxs-lookup"><span data-stu-id="69ef7-174">On the **General** tab, the **Title** text box should show the app name that you typed in step 4.</span></span> <span data-ttu-id="69ef7-175">Wählen Sie **die Registerkarte** Berechtigungen aus, um die folgenden Berechtigungsanforderungen für die App hinzuzufügen (siehe Abbildung 2):</span><span class="sxs-lookup"><span data-stu-id="69ef7-175">Choose the **Permissions** tab to add the following permission requests for the app (see Figure 2):</span></span> 
    
   - <span data-ttu-id="69ef7-176">Wählen Sie in der ersten Zeile der **Liste Berechtigungsanforderungen** in der Spalte **Bereich** in der Dropdownliste **Statusing** aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-176">In the first row of the **Permission requests** list, in the **Scope** column, choose **Statusing** in the drop-down list.</span></span> <span data-ttu-id="69ef7-177">Wählen Sie **in der Spalte** Berechtigung die Option **SubmitStatus aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-177">In the **Permission** column, choose **SubmitStatus**.</span></span>
    
   - <span data-ttu-id="69ef7-178">Fügen Sie eine Zeile hinzu, in der **Scope** mehrere **Projekte** und die **Berechtigung Read** **ist.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-178">Add a row where the **Scope** is **Multiple Projects** and the **Permission** is **Read**.</span></span>
    
   <span data-ttu-id="69ef7-179">**Abbildung 2. Festlegen des Berechtigungsbereichs für eine Status-App**</span><span class="sxs-lookup"><span data-stu-id="69ef7-179">**Figure 2. Setting the permission scope for a statusing app**</span></span>

   <span data-ttu-id="69ef7-180">![Festlegen des Berechtigungsumfangs für eine Statuserfassungs-App](media/pj15_CreateStatusingApp_PermissionScope.gif "Festlegen des Berechtigungsumfangs für eine Statuserfassungs-App")</span><span class="sxs-lookup"><span data-stu-id="69ef7-180">![Setting the permission scope for a statusing app](media/pj15_CreateStatusingApp_PermissionScope.gif "Setting the permission scope for a statusing app")</span></span>
  
<span data-ttu-id="69ef7-181">Die **QuickStatus-App** ermöglicht es einem Project Web App-Benutzer, Zuordnungen für den Benutzer aus mehreren Projekten zu lesen, den abgeschlossenen Zuordnungsprozentl zu ändern und das Update zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="69ef7-181">The **QuickStatus** app enables a Project Web App user to read assignments for that user from multiple projects, change the assignment percent complete, and submit the update.</span></span> <span data-ttu-id="69ef7-182">Die anderen Berechtigungsanforderungsbereiche, die in der Dropdownliste in Abbildung 2 angezeigt werden, sind für diese App nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69ef7-182">The other permission request scopes shown in the drop-down list in Figure 2 are not required for this app.</span></span> <span data-ttu-id="69ef7-183">Die Berechtigungsanforderungsbereiche sind die Berechtigungen, die die App im Auftrag des Benutzers anfordert.</span><span class="sxs-lookup"><span data-stu-id="69ef7-183">The permission request scopes are the permissions that the app requests on behalf of the user.</span></span> <span data-ttu-id="69ef7-184">Wenn der Benutzer nicht über diese Berechtigungen in Project Web App verfügt, wird die App nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-184">If the user does not have those permissions in Project Web App, the app does not run.</span></span> <span data-ttu-id="69ef7-185">Eine App kann über mehrere Berechtigungsanforderungsbereiche verfügen, einschließlich derer für andere SharePoint Berechtigungen, sollte jedoch nur über das für die App-Funktionalität erforderliche Minimum verfügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-185">An app can have multiple permission request scopes, including those for other SharePoint permissions, but should have only the minimum necessary for the app functionality.</span></span> <span data-ttu-id="69ef7-186">Im Folgenden finden Sie die Berechtigungsanforderungsbereiche, die sich auf Project Server bezogen haben:</span><span class="sxs-lookup"><span data-stu-id="69ef7-186">Following are the permission request scopes that are related to Project Server:</span></span> 

- <span data-ttu-id="69ef7-187">**Enterprise Ressourcen**: Ressourcen-Manager-Berechtigungen zum Lesen oder Schreiben von Informationen zu anderen Project Web App-Benutzern.</span><span class="sxs-lookup"><span data-stu-id="69ef7-187">**Enterprise Resources**: Resource manager permissions, to read or write information about other Project Web App users.</span></span>
    
- <span data-ttu-id="69ef7-188">**Mehrere Projekte**: Lese- oder Schreibzugriff auf mehrere Projekte, bei denen der Benutzer über die angeforderten Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-188">**Multiple Projects**: Read or write to more than one project, where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="69ef7-189">**Project Server**: Erfordert, dass der App-Benutzer über Administratorberechtigungen für Project Web App verfügt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-189">**Project Server**: Requires the app user to have administrator permissions for Project Web App.</span></span>
    
- <span data-ttu-id="69ef7-190">**Reporting**: Read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App).</span><span class="sxs-lookup"><span data-stu-id="69ef7-190">**Reporting**: Read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App).</span></span> 
    
- <span data-ttu-id="69ef7-191">**Single Project**: Lese- oder Schreibzugriff auf ein Projekt, in dem der Benutzer über die angeforderten Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-191">**Single Project**: Read or write to a project where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="69ef7-192">**Statusing**: Übermitteln von Aktualisierungen für den Status von Zuordnungen, z. B. Arbeitsstunden, Prozent abgeschlossene und neue Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-192">**Statusing**: Submit updates for status of assignments, such as times worked, percent complete, and new assignments.</span></span>
    
- <span data-ttu-id="69ef7-193">**Workflow**: Wenn der Benutzer über die Berechtigung zum Ausführen Project Serverworkflows verfügt, wird die App mit erhöhten Berechtigungen für den Workflow ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-193">**Workflow**: If the user has permission to run Project Server workflows, the app then runs with elevated permissions for the workflow.</span></span>
    
<span data-ttu-id="69ef7-194">Weitere Informationen zu Berechtigungsanforderungsbereich für Project Server 2013 finden Sie im Abschnitt *Project-Apps* unter [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md) und [App permissions in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span><span class="sxs-lookup"><span data-stu-id="69ef7-194">For more information about permission request scopes for Project Server 2013, see the  *Project apps*  section in [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md) and [App permissions in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span></span>


<span data-ttu-id="69ef7-195"><a name="pj15_StatusingApp_HTML"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-195"><a name="pj15_StatusingApp_HTML"> </a></span></span>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a><span data-ttu-id="69ef7-196">Erstellen des HTML-Inhalts für die QuickStatus-App</span><span class="sxs-lookup"><span data-stu-id="69ef7-196">Creating the HTML content for the QuickStatus app</span></span>

<span data-ttu-id="69ef7-197">Bevor Sie mit dem Codieren der HTML-Inhalte beginnen, entwerfen Sie die Benutzeroberfläche und die Benutzeroberfläche für die QuickStatus-App (Abbildung 3 zeigt ein Beispiel für die abgeschlossene Seite).</span><span class="sxs-lookup"><span data-stu-id="69ef7-197">Before you start coding the HTML content, design the user interface and user experience for the QuickStatus app (Figure 3 shows an example of the completed page).</span></span> <span data-ttu-id="69ef7-198">Ein Entwurf kann auch eine Gliederung der JavaScript-Funktionen enthalten, die mit dem HTML-Code interagieren.</span><span class="sxs-lookup"><span data-stu-id="69ef7-198">A design can also include an outline of the JavaScript functions that interact with the HTML code.</span></span> <span data-ttu-id="69ef7-199">Allgemeine Informationen finden Sie unter [UX design for apps in SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span><span class="sxs-lookup"><span data-stu-id="69ef7-199">For general information, see [UX design for apps in SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span></span>
  
<span data-ttu-id="69ef7-200">**Abbildung 3. Design der QuickStatus-App-Seite**</span><span class="sxs-lookup"><span data-stu-id="69ef7-200">**Figure 3. Design of the QuickStatus app page**</span></span>

<span data-ttu-id="69ef7-201">![Design der QuickStatus-App-Seite](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design der QuickStatus-App-Seite")</span><span class="sxs-lookup"><span data-stu-id="69ef7-201">![Design of the QuickStatus app page](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design of the QuickStatus app page")</span></span>
  
<span data-ttu-id="69ef7-202">Die App zeigt den Anzeigenamen oben an, der der Wert des **Title-Elements** in AppManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="69ef7-202">The app shows the display name at the top, which is the value of the **Title** element in AppManifest.xml.</span></span> 
  
<span data-ttu-id="69ef7-203">Standardmäßig verwendet die Seite HTML5.</span><span class="sxs-lookup"><span data-stu-id="69ef7-203">By default, the page uses HTML5.</span></span> <span data-ttu-id="69ef7-204">Nachfolgend finden Sie die Standard-HTML-Elemente für die hauptbenutzeroberflächenobjekte, die die **QuickStatus-App** im Textkörper der Seite enthält:</span><span class="sxs-lookup"><span data-stu-id="69ef7-204">Following are the standard HTML elements for the main UI objects that the **QuickStatus** app contains in the body of the page:</span></span> 
  
- <span data-ttu-id="69ef7-205">Ein **Formularelement** enthält alle anderen Benutzeroberflächenelemente.</span><span class="sxs-lookup"><span data-stu-id="69ef7-205">A **form** element contains all of the other UI elements.</span></span> 
    
- <span data-ttu-id="69ef7-206">Ein **Fieldset-Element** erstellt einen Container und einen Rahmen für die Zuordnungstabelle. Das untergeordnete **Legendenelement** enthält eine Bezeichnung für den Container.</span><span class="sxs-lookup"><span data-stu-id="69ef7-206">A **fieldset** element creates a container and border for the table of assignments; the child **legend** element provides a label for the container.</span></span> 
    
- <span data-ttu-id="69ef7-207">Ein **Tabellenelement** enthält eine Beschriftung und nur eine Tabellenkopfzeile.</span><span class="sxs-lookup"><span data-stu-id="69ef7-207">A **table** element includes a caption and only a table header.</span></span> <span data-ttu-id="69ef7-208">JavaScript-Funktionen ändern die Tabellenbeschriftung und fügen Zeilen für die Zuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-208">JavaScript functions change the table caption and add rows for the assignments.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="69ef7-209">Zum einfachen Hinzufügen von Auslagerungen und Sortierungen würde eine Produktions-App wahrscheinlich ein kommerzielles jQuery-basiertes Rastersteuerelement anstelle einer Tabelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-209">To easily add paging and sorting, a production app would probably use a commercial jQuery-based grid control instead of a table.</span></span> 
  
   <span data-ttu-id="69ef7-210">Die Tabelle enthält Spalten für den Projektnamen, den Vorgangsnamen mit einem Kontrollkästchen, die aktuelle Arbeit, den Abgeschlossenen Prozentbetrag, die verbleibende Arbeit und den Zuordnungsendtermin.</span><span class="sxs-lookup"><span data-stu-id="69ef7-210">The table includes columns for the project name, task name with a check box, actual work, percent complete, remaining work, and the assignment finish date.</span></span> <span data-ttu-id="69ef7-211">JavaScript-Funktionen erstellen das Kontrollkästchen und das Texteingabefeld für den Prozentbereich, der für jeden Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-211">JavaScript functions create the check box and the text input field for the percent complete of each task.</span></span>
    
- <span data-ttu-id="69ef7-212">Ein **Eingabeelement** für ein Textfeld legt für alle ausgewählten Zuordnungen den vollständigen Prozentbereich fest.</span><span class="sxs-lookup"><span data-stu-id="69ef7-212">An **input** element for a text box sets percent complete for all selected assignments.</span></span> 
    
- <span data-ttu-id="69ef7-213">Ein **Schaltflächenelement** übermittelt die Statusänderungen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-213">A **button** element submits the status changes.</span></span> 
    
- <span data-ttu-id="69ef7-214">Ein **Schaltflächenelement** aktualisiert die Seite.</span><span class="sxs-lookup"><span data-stu-id="69ef7-214">A **button** element refreshes the page.</span></span> 
    
- <span data-ttu-id="69ef7-215">Ein **Schaltflächenelement** beendet die App und kehrt zur Seite Aufgaben in Project Web App zurück.</span><span class="sxs-lookup"><span data-stu-id="69ef7-215">A **button** element exits the app and returns to the Tasks page in Project Web App.</span></span> 
    
<span data-ttu-id="69ef7-216">Das untere Textfeld und  die Schaltflächenelemente befinden sich innerhalb von div-Elementen, sodass CSS die Position und Darstellung der Benutzeroberflächenobjekte problemlos verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="69ef7-216">The bottom text box and button elements are within **div** elements, so that CSS can easily manage the position and appearance of the UI objects.</span></span> <span data-ttu-id="69ef7-217">Eine JavaScript-Funktion fügt am unteren Rand der Seite einen Absatz hinzu, der Ergebnisse für den Erfolg oder Fehler der Statusaktualisierung enthält.</span><span class="sxs-lookup"><span data-stu-id="69ef7-217">A JavaScript function adds a paragraph at the bottom of the page that contains results for success or failure of the status update.</span></span> 
  
### <a name="procedure-2-to-create-the-html-content"></a><span data-ttu-id="69ef7-218">Vorgehensweise 2:</span><span class="sxs-lookup"><span data-stu-id="69ef7-218">Procedure 2.</span></span> <span data-ttu-id="69ef7-219">So erstellen Sie den HTML-Inhalt</span><span class="sxs-lookup"><span data-stu-id="69ef7-219">To create the HTML content</span></span>

1. <span data-ttu-id="69ef7-220">Öffnen Visual Studio die Datei "Default.aspx".</span><span class="sxs-lookup"><span data-stu-id="69ef7-220">In Visual Studio, open the Default.aspx file.</span></span>
    
   <span data-ttu-id="69ef7-221">Die Datei enthält zwei **asp:Content-Elemente:** Das Element mit dem Attribut wird innerhalb der Seitenkopfzeile hinzugefügt, und das Element mit dem Attribut wird innerhalb des  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"`  `ContentPlaceHolderID="PlaceHolderMain"` **Seitentextelements** platziert.</span><span class="sxs-lookup"><span data-stu-id="69ef7-221">The file includes two **asp:Content** elements: The element with the  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` attribute is added within the page header, and the element with the  `ContentPlaceHolderID="PlaceHolderMain"` attribute is placed within the page **body** element.</span></span> 
    
2. <span data-ttu-id="69ef7-222">Fügen Sie im Steuerelement für die Seitenkopfzeile einen Verweis auf die PS.js auf dem `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` Servercomputer Project hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-222">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` control for the page header, add a reference to the PS.js file on the Project Server computer.</span></span> <span data-ttu-id="69ef7-223">Zum Testen und Debuggen können Sie PS.debug.js.</span><span class="sxs-lookup"><span data-stu-id="69ef7-223">For testing and debugging, you can use PS.debug.js.</span></span> 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   <span data-ttu-id="69ef7-224">Die App-Infrastruktur verwendet das `/_layouts/15/` virtuelle Verzeichnis für SharePoint in IIS.</span><span class="sxs-lookup"><span data-stu-id="69ef7-224">The app infrastructure uses the `/_layouts/15/` virtual directory for the SharePoint site in IIS.</span></span> <span data-ttu-id="69ef7-225">Die physische Datei ist  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js` .</span><span class="sxs-lookup"><span data-stu-id="69ef7-225">The physical file is  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="69ef7-226">Entfernen Sie vor der Bereitstellung der App für die Produktionsnutzung aus den  `.debug` Skriptverweisen, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="69ef7-226">Before you deploy the app for production use, remove  `.debug` from the script references to improve performance.</span></span> 
  
3. <span data-ttu-id="69ef7-227">Löschen Sie im Steuerelement für den Seitentext das generierte div-Element, und fügen Sie dann den `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` HTML-Code  für die Benutzeroberflächenobjekte hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-227">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` control for the page body, delete the generated **div** element, and then add the HTML code for the UI objects.</span></span> <span data-ttu-id="69ef7-228">Das **Tabellenelement** enthält nur eine Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="69ef7-228">The **table** element contains only a header row.</span></span> <span data-ttu-id="69ef7-229">Die **Spalte Vorgangsname** enthält ein Eingabesteuerelement des Kontrollkästchens.</span><span class="sxs-lookup"><span data-stu-id="69ef7-229">The **Task name** column includes a check box input control.</span></span> <span data-ttu-id="69ef7-230">Text für das **Caption-Element** wird durch den **onGetUserNameSuccess-Rückruf** für die **getUserInfo-Funktion** in der App.js ersetzt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-230">Text for the **caption** element is replaced by the **onGetUserNameSuccess** callback for the **getUserInfo** function in the App.js file.</span></span> 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. <span data-ttu-id="69ef7-231">Fügen Sie in der Datei App.css CSS-Code für die Position und Darstellung der Benutzeroberflächenelemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-231">In the App.css file, add CSS code for the position and appearance of the UI elements.</span></span> <span data-ttu-id="69ef7-232">Den vollständigen CSS-Code der **QuickStatus-App** finden Sie im Abschnitt [Beispielcode für die QuickStatus-App.](#pj15_StatusingApp_Example)</span><span class="sxs-lookup"><span data-stu-id="69ef7-232">For the complete CSS code of the **QuickStatus** app, see the [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section.</span></span> 
    
<span data-ttu-id="69ef7-233">Prozedur 3 fügt die JavaScript-Funktionen hinzu, um die Zuordnungen zu lesen und die Tabellenzeilen zu erstellen sowie den Abgeschlossenen Zuordnungsprozentsatz zu ändern und zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="69ef7-233">Procedure 3 adds the JavaScript functions to read the assignments and create the table rows, and to change and update the assignment percent complete.</span></span> <span data-ttu-id="69ef7-234">Die eigentlichen Schritte sind iterativer bei der Entwicklung einer App, in der Sie abwechselnd einen Teil des HTML-Codes erstellen, verwandte Formatvorlagen und JavaScript-Funktionen hinzufügen und testen, mehr HTML-Code ändern oder hinzufügen und dann den Prozess wiederholen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-234">The actual steps are more iterative in developing an app, where you alternately create some of the HTML code, add and test related styles and JavaScript functions, modify or add more HTML code, and then repeat the process.</span></span>

<span data-ttu-id="69ef7-235"><a name="pj15_StatusingApp_JavaScript"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-235"><a name="pj15_StatusingApp_JavaScript"> </a></span></span>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a><span data-ttu-id="69ef7-236">Erstellen der JavaScript-Funktionen für die QuickStatus-App</span><span class="sxs-lookup"><span data-stu-id="69ef7-236">Creating the JavaScript functions for the QuickStatus app</span></span>

<span data-ttu-id="69ef7-237">Die Visual Studio-Vorlage für eine SharePoint-App enthält die App.js-Datei, die den Standard initialisierungscode enthält, der den SharePoint-Clientkontext abgibt und grundlegende Get- und Set-Aktionen für die App-Seite veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="69ef7-237">The Visual Studio template for a SharePoint app includes the App.js file, which contains default initialization code that gets the SharePoint client context and demonstrates basic get and set actions for the app page.</span></span> <span data-ttu-id="69ef7-238">Der JavaScript-Namespace für SharePoint clientseitige SP.js ist **SP**.</span><span class="sxs-lookup"><span data-stu-id="69ef7-238">The JavaScript namespace for the SharePoint client-side SP.js library is **SP**.</span></span> <span data-ttu-id="69ef7-239">Da eine Project Server-App die PS.js verwendet, verwendet  die App den PS-Namespace, um den Clientkontext zu erhalten und auf das JSOM für Project Server zugreift.</span><span class="sxs-lookup"><span data-stu-id="69ef7-239">Because a Project Server app uses the PS.js library, the app uses the **PS** namespace to get the client context and access the JSOM for Project Server.</span></span> 
  
<span data-ttu-id="69ef7-240">JavaScript-Funktionen in der **QuickStatus-App** umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="69ef7-240">JavaScript functions in the **QuickStatus** app include the following:</span></span> 
  
- <span data-ttu-id="69ef7-241">Der **dokumentbereite** Ereignishandler wird ausgeführt, wenn das Dokumentobjektmodell (DOCUMENT Object Model, DOM) instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="69ef7-241">The document **ready** event handler runs when the document object model (DOM) is instantiated.</span></span> <span data-ttu-id="69ef7-242">Der  ready-Ereignishandler führt die folgenden vier Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="69ef7-242">The **ready** event handler does the following four steps:</span></span> 
    
    1. <span data-ttu-id="69ef7-243">Initialisiert die **globale ProjContext-Variable** mit dem Clientkontext für Project Server JSOM und **die globale pwaWeb-Variable.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-243">Initializes the **projContext** global variable with the client context for the Project Server JSOM and the **pwaWeb** global variable.</span></span> 
        
    2. <span data-ttu-id="69ef7-244">Ruft die **getUserInfo-Funktion** auf, um die **globale ProjUser-Variable** zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="69ef7-244">Calls the **getUserInfo** function to initialize the **projUser** global variable.</span></span> 
        
    3. <span data-ttu-id="69ef7-245">Ruft die **getAssignments-Funktion** auf, die angegebene Zuweisungsdaten für den Benutzer ab ruft.</span><span class="sxs-lookup"><span data-stu-id="69ef7-245">Calls the **getAssignments** function, which gets specified assignment data for the user.</span></span> 
        
    4. <span data-ttu-id="69ef7-246">Binds click event handlers to the table header check box, and to the check boxes in each row of the table.</span><span class="sxs-lookup"><span data-stu-id="69ef7-246">Binds click event handlers to the table header check box, and to the check boxes in each row of the table.</span></span> <span data-ttu-id="69ef7-247">Die Click-Ereignishandler verwalten das aktivierte **Attribut** der Kontrollkästchen, wenn der Benutzer ein Kontrollkästchen in der Tabelle auswählt oder auswählt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-247">The click event handlers manage the **checked** attribute of the check boxes when the user selects or clears any check box in the table.</span></span> 
    
- <span data-ttu-id="69ef7-248">Wenn die **getAssignments-Funktion** erfolgreich ist, ruft sie die **onGetAssignmentsSuccess-Funktion** auf.</span><span class="sxs-lookup"><span data-stu-id="69ef7-248">If the **getAssignments** function is successful, it calls the **onGetAssignmentsSuccess** function.</span></span> <span data-ttu-id="69ef7-249">Diese Funktion fügt für jede Zuordnung eine Zeile in die Tabelle ein, initialisiert die HTML-Steuerelemente in jeder Zeile und initialisiert dann die Eigenschaften der unteren Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="69ef7-249">That function inserts a row in the table for each assignment, initializes the HTML controls in each row, and then initializes the bottom button properties.</span></span> 
    
- <span data-ttu-id="69ef7-250">Der **onClick-Ereignishandler** für die **Schaltfläche Update** ruft die **updateAssignments-Funktion** auf.</span><span class="sxs-lookup"><span data-stu-id="69ef7-250">The **onClick** event handler for the **Update** button calls the **updateAssignments** function.</span></span> <span data-ttu-id="69ef7-251">Diese Funktion ruft den vollständigen Prozentwert ab, der auf jede ausgewählte Zuordnung angewendet wird. oder wenn das vollständige Textfeld Prozent leer ist, ruft die Funktion den Prozent abgeschlossen jeder ausgewählten Zuordnung in der Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="69ef7-251">That function gets the percent complete value that is applied to each selected assignment; or if the percent complete text box is empty, the function gets the percent complete of each selected assignment in the table.</span></span> <span data-ttu-id="69ef7-252">Die **updateAssignments-Funktion** speichert und übermittelt dann die Statusupdates und schreibt eine Meldung über die Ergebnisse an den unteren Rand der Seite.</span><span class="sxs-lookup"><span data-stu-id="69ef7-252">The **updateAssignments** function then saves and submits the status updates and writes a message about the results to the bottom of the page.</span></span> 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a><span data-ttu-id="69ef7-253">Verfahren 3.</span><span class="sxs-lookup"><span data-stu-id="69ef7-253">Procedure 3.</span></span> <span data-ttu-id="69ef7-254">So erstellen Sie die JavaScript-Funktionen</span><span class="sxs-lookup"><span data-stu-id="69ef7-254">To create the JavaScript functions</span></span>

1. <span data-ttu-id="69ef7-255">Öffnen Visual Studio die Datei App.js, und löschen Sie dann alle Inhalte in der Datei.</span><span class="sxs-lookup"><span data-stu-id="69ef7-255">In Visual Studio, open the App.js file, and then delete all the content in the file.</span></span>
    
2. <span data-ttu-id="69ef7-256">Fügen Sie die globalen Variablen und den **dokumentbereiten Ereignishandler** hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-256">Add the global variables and the document **ready** event handler.</span></span> <span data-ttu-id="69ef7-257">Auf **das Dokumentobjekt** wird mithilfe einer jQuery-Funktion zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-257">The **document** object is accessed by using a jQuery function.</span></span> 
    
   <span data-ttu-id="69ef7-258">Das Kontrollkästchen Click-Ereignishandler für die Tabellenkopfzeile legt den aktivierten Status der Zeilenkontrollkästchen fest.</span><span class="sxs-lookup"><span data-stu-id="69ef7-258">The click event handler for the table header check box sets the checked state of the row check boxes.</span></span> <span data-ttu-id="69ef7-259">Wenn alle Zeilenkontrollkästchen aktiviert sind oder alle aktiviert sind, wird der aktivierte Status des Kopfzeilenkontrollkästchens durch den Click-Ereignishandler für die Zeilen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="69ef7-259">If all of the row check boxes are selected or all are clear, the click event handler for the row check boxes sets the checked state of the header check box.</span></span> <span data-ttu-id="69ef7-260">Die Click-Ereignishandler legen auch die Ergebnismeldung am unteren Rand der Seite auf eine leere Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="69ef7-260">The click event handlers also set the results message at the bottom of the page to an empty string.</span></span>
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. <span data-ttu-id="69ef7-261">Fügen Sie **die getUserInfo-Funktion** hinzu, die **onGetUserNameSuccess** aufruft, wenn die Abfrage erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-261">Add the **getUserInfo** function, which calls **onGetUserNameSuccess** if the query is successful.</span></span> <span data-ttu-id="69ef7-262">Die **onGetUserNameSuccess-Funktion** ersetzt den  Inhalt des Beschriftungsab absatzes durch eine Tabellenbeschriftung, die den Benutzernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="69ef7-262">The **onGetUserNameSuccess** function replaces the contents of the **caption** paragraph with a table caption that includes the user name.</span></span> 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. <span data-ttu-id="69ef7-263">Fügen Sie **die getAssignments-Funktion** hinzu, die **onGetAssignmentsSuccess aufruft** (siehe Schritt 5), wenn die Zuweisungsabfrage erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-263">Add the **getAssignments** function, which calls **onGetAssignmentsSuccess** (see step 5) if the assignment query is successful.</span></span> <span data-ttu-id="69ef7-264">Die **Option Include** schränkt die Abfrage so ein, dass nur die angegebenen Felder zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-264">The **Include** option limits the query to return only the fields specified.</span></span> 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. <span data-ttu-id="69ef7-265">Fügen Sie **die onGetAssignmentsSuccess-Funktion** hinzu, die der Tabelle eine Zeile für jede Zuordnung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-265">Add the **onGetAssignmentsSuccess** function, which adds a row for each assignment to the table.</span></span> <span data-ttu-id="69ef7-266">Die **prevProjName-Variable** wird verwendet, um zu bestimmen, ob eine Zeile für ein anderes Projekt gilt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-266">The **prevProjName** variable is used to determine whether a row is for a different project.</span></span> <span data-ttu-id="69ef7-267">Wenn ja, wird der Projektname in fett formatierter Schriftart angezeigt. Andern falls nicht, wird der Projektname auf eine leere Zeichenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-267">If so, the project name is shown in a bold font; if not, the project name is set to an empty string.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="69ef7-268">Das JSOM enthält keine **TimeSpan-Eigenschaften,** die das CSOM enthält, z. B. **ActualWorkTimeSpan**.</span><span class="sxs-lookup"><span data-stu-id="69ef7-268">The JSOM does not include **TimeSpan** properties that the CSOM includes, such as **ActualWorkTimeSpan**.</span></span> <span data-ttu-id="69ef7-269">Stattdessen verwendet das JSOM Eigenschaften für die Anzahl von Millisekunden, z. [B. ps. StatusAssignment.actualWorkMilliseconds-Eigenschaft.](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69ef7-269">Instead, the JSOM uses properties for the number of milliseconds, such as the [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) property.</span></span> <span data-ttu-id="69ef7-270">Die Methode zum Erhalten dieser Eigenschaft **ist \_ actualWorkMilliseconds**, die einen ganzzahligen Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-270">The method to get that property is **get\_actualWorkMilliseconds**, which returns an integer value.</span></span> <span data-ttu-id="69ef7-271">> Die **get_actualWork-Methode** gibt eine Zeichenfolge wie "3h" zurück.</span><span class="sxs-lookup"><span data-stu-id="69ef7-271">> The **get_actualWork** method returns a string such as "3h".</span></span> <span data-ttu-id="69ef7-272">Sie können einen der Werte in der **QuickStatus-App** verwenden, ihn jedoch anders anzeigen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-272">You could use either value in the **QuickStatus** app, but display it differently.</span></span> <span data-ttu-id="69ef7-273">Die Zuordnungsabfrage enthält beide Eigenschaften, sodass Sie den Wert während des Debuggens testen können.</span><span class="sxs-lookup"><span data-stu-id="69ef7-273">The assignments query includes both properties, so you can test the value during debugging.</span></span> <span data-ttu-id="69ef7-274">Wenn Sie die **actualWork-Variable** entfernen, können Sie auch die **ActualWork-Eigenschaft** in der Zuweisungsabfrage entfernen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-274">If you remove the **actualWork** variable, you can also remove the **ActualWork** property in the assignments query.</span></span> 
  
   <span data-ttu-id="69ef7-275">Schließlich initialisiert **die onGetAssignmentsSuccess-Funktion** die Schaltfläche **Update** und die **Schaltfläche Aktualisieren** mit Click-Ereignishandlern.</span><span class="sxs-lookup"><span data-stu-id="69ef7-275">Finally, the **onGetAssignmentsSuccess** function initializes the **Update** button and the **Refresh** button with click event handlers.</span></span> <span data-ttu-id="69ef7-276">Der Textwert der Schaltfläche **Aktualisieren** kann auch im HTML-Code festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-276">The text value of the **Update** button could also be set in the HTML code.</span></span> 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. <span data-ttu-id="69ef7-277">Fügen Sie **den updateAssignments-Click-Ereignishandler** für die Schaltfläche **Aktualisieren** hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-277">Add the **updateAssignments** click event handler for the **Update** button.</span></span> <span data-ttu-id="69ef7-278">Wenn der Benutzer einen Wert für den abgeschlossenen Prozentwert eines Vorgangs ändert oder einen Wert im Textfeld **percentComplete** hinzufügt, kann der Wert in mehreren Formaten eingegeben werden, z. B. "60", "60 %" oder "60 %".</span><span class="sxs-lookup"><span data-stu-id="69ef7-278">When the user changes a value for percent complete of a task, or adds a value in the **percentComplete** text box, the value could be entered in several formats such as "60", "60%", or "60 %".</span></span> <span data-ttu-id="69ef7-279">Die **getNumericValue-Methode** gibt den numerischen Wert des Eingabetexts zurück.</span><span class="sxs-lookup"><span data-stu-id="69ef7-279">The **getNumericValue** method returns the numeric value of the input text.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="69ef7-280">In einer App, die für die Produktionsnutzung konzipiert ist, sollten Eingabewerte für numerische Informationen die Feldüberprüfung und zusätzliche Fehlerüberprüfung umfassen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-280">In an app that is designed for production use, input values for numeric information should include field validation and additional error checking.</span></span> 
  
   <span data-ttu-id="69ef7-281">Das **UpdateAssignments-Beispiel** enthält einige grundlegende Fehlerüberprüfungen  und zeigt Informationen im Nachrichtenab absatz am unteren Rand der Seite an– grün, wenn die Aktualisierungsabfrage erfolgreich ist, und rot, wenn ein Eingabefehler auftritt oder die Aktualisierungsabfrage nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-281">The **updateAssignments** example includes some basic error checking, and displays information in the **message** paragraph at the bottom of the page—green if the update query is successful and red if there is an input error or the update query is unsuccessful.</span></span> 
    
   <span data-ttu-id="69ef7-282">Vor der Verwendung der **submitAllStatusUpdates-Methode** muss die App die Updates auf dem Server mithilfe der **PS speichern. StatusAssignmentCollection.update-Methode.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-282">Before using the **submitAllStatusUpdates** method, the app must save the updates to the server by using the **PS.StatusAssignmentCollection.update** method.</span></span> 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. <span data-ttu-id="69ef7-283">Fügen Sie **die exitToPwa-Funktion** hinzu, die den **SPHostUrl-Abfragezeichenfolgenparameter** für die URL der Host-Project Web App-Website verwendet.</span><span class="sxs-lookup"><span data-stu-id="69ef7-283">Add the **exitToPwa** function, which uses the **SPHostUrl** query string parameter for the URL of the host Project Web App site.</span></span> <span data-ttu-id="69ef7-284">Um zur Seite Aufgaben zurück zu navigieren, fügen Sie  `"/Tasks.aspx"` die URL an.</span><span class="sxs-lookup"><span data-stu-id="69ef7-284">To navigate back to the Tasks page, append  `"/Tasks.aspx"` to the URL.</span></span> <span data-ttu-id="69ef7-285">Die variable **spHostUrl** wird beispielsweise auf  `https://ServerName/ProjectServerName/Tasks.aspx` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-285">For example, the **spHostUrl** variable would be set to  `https://ServerName/ProjectServerName/Tasks.aspx`.</span></span>
    
   <span data-ttu-id="69ef7-286">Die **getQueryStringParameter-Funktion** teilt die URL der **QuickStatus-Seite** auf, um den angegebenen Parameter in den URL-Optionen zu extrahieren und zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="69ef7-286">The **getQueryStringParameter** function splits the URL of the **QuickStatus** page to extract and return the specified parameter in the URL options.</span></span> <span data-ttu-id="69ef7-287">Im Folgenden finden Sie ein Beispiel für das **Dokument. URL-Wert** für das **QuickStatus-Dokument** (alle in einer Zeile):</span><span class="sxs-lookup"><span data-stu-id="69ef7-287">Following is an example of the **document.URL** value for the **QuickStatus** document (all on one line):</span></span> 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   <span data-ttu-id="69ef7-288">Für die vorherige URL gibt **die GetQueryStringParameter-Funktion** den **SPHostUrl-Abfragezeichenfolgenwert** zurück,  `https://ServerName/pwa` .</span><span class="sxs-lookup"><span data-stu-id="69ef7-288">For the previous URL, the **getQueryStringParameter** function returns the **SPHostUrl** query string value,  `https://ServerName/pwa`.</span></span> 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

<span data-ttu-id="69ef7-289">Wenn Sie die **QuickStatus-App** zu diesem Zeitpunkt veröffentlichen und Project Web App hinzufügen, kann die App auf der Seite Websiteinhalte ausgeführt werden, für Benutzer ist sie jedoch nicht einfach verfügbar.</span><span class="sxs-lookup"><span data-stu-id="69ef7-289">If you publish the **QuickStatus** app at this point and add it to Project Web App, the app can be run from the Site Contents page, but it is not easily available to users.</span></span> <span data-ttu-id="69ef7-290">Damit Benutzer die App finden und ausführen können, können Sie dem Menüband auf der Seite Aufgaben eine Schaltfläche hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-290">To help users find and run the app, you can add a button for it to the ribbon on the Tasks page.</span></span> <span data-ttu-id="69ef7-291">In Prozedur 4 wird gezeigt, wie Sie eine benutzerdefinierte Menübandaktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-291">Procedure 4 shows how to add a ribbon custom action.</span></span> 

<span data-ttu-id="69ef7-292"><a name="pj15_StatusingApp_ribbon"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-292"><a name="pj15_StatusingApp_ribbon"> </a></span></span>

### <a name="adding-a-ribbon-custom-action"></a><span data-ttu-id="69ef7-293">Hinzufügen einer benutzerdefinierten Menübandaktion</span><span class="sxs-lookup"><span data-stu-id="69ef7-293">Adding a ribbon custom action</span></span>

<span data-ttu-id="69ef7-294">Menübandregisterkarten, Gruppen und Steuerelemente für Project Web App werden in der pwaribbon.xml-Datei angegeben, die im Verzeichnis auf dem Computer installiert ist, auf dem `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` Project Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69ef7-294">Ribbon tabs, groups, and controls for Project Web App are specified in the pwaribbon.xml file, which is installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` directory on the computer running Project Server.</span></span> <span data-ttu-id="69ef7-295">Um benutzerdefinierte Aktionen für das Menüband Project Web App zu entwerfen, enthält der Project 2013 SDK-Download eine Kopie pwaribbon.xml.</span><span class="sxs-lookup"><span data-stu-id="69ef7-295">To help design custom actions for the Project Web App ribbon, the Project 2013 SDK download includes a copy of pwaribbon.xml.</span></span> 
  
<span data-ttu-id="69ef7-296">Project Web App verwendet unterschiedliche Menübanddefinitionen für die Seite Aufgaben, je nachdem, ob die Project Web App-Instanz den Modus für einmalige Eingaben verwendet, mit dem Benutzer Werte für die Arbeitszeittabelle und den Aufgabenstatus eingeben können.</span><span class="sxs-lookup"><span data-stu-id="69ef7-296">Project Web App uses different ribbon definitions for the Tasks page, depending on whether the Project Web App instance uses single entry mode that enables users to enter values for both the timesheet and task status.</span></span> <span data-ttu-id="69ef7-297">Wenn Sie über Administratorberechtigungen für Project Web App verfügen, wählen Sie zum Bestimmen des Eintragsmodus **PWA Einstellungen** im Dropdownmenü Einstellungen in der oberen rechten Ecke der Seite aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-297">If you have administrative permissions for Project Web App, to determine the entry mode, choose **PWA Settings** in the drop-down settings menu at the top-right corner of the page.</span></span> <span data-ttu-id="69ef7-298">Wählen Sie PWA Einstellungen Seite Arbeitszeittabelle Einstellungen und Standardwerte aus, und sehen  Sie sich dann das Kontrollkästchen Einzelner **Eintragsmodus** am unteren Rand der Seite an.</span><span class="sxs-lookup"><span data-stu-id="69ef7-298">On the PWA Settings page, choose **Timesheet Settings and Defaults**, and then look at the **Single Entry Mode** check box at the bottom of the page.</span></span> 
  
<span data-ttu-id="69ef7-299">Wenn der Einzeleingabemodus deaktiviert ist, wird das Menüband auf der Seite Aufgaben durch den Bereich Meine Arbeit in der pwaribbon.xml:</span><span class="sxs-lookup"><span data-stu-id="69ef7-299">When single entry mode is off, the ribbon on the Tasks page is defined by the My Work region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

<span data-ttu-id="69ef7-300">Wenn der Modus für einen einzelnen Eintrag aktiviert ist, wird das Seitenband Aufgaben durch den Bereich Gebundener Modus in der pwaribbon.xml:</span><span class="sxs-lookup"><span data-stu-id="69ef7-300">When single entry mode is on, the Tasks page ribbon is defined by the Tied Mode region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

<span data-ttu-id="69ef7-301">Obwohl die Gruppen und Steuerelemente in den einzelnen Regionen ähnlich aussehen, kann ein Steuerelement für den gebundenen Modus eine andere Funktion als das gleiche Steuerelement für den nicht gebundenen Modus aufrufen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-301">Although the groups and controls in each region look similar, a control for the tied mode can call a different function than the same control for the non-tied mode.</span></span> <span data-ttu-id="69ef7-302">In Prozedur 4 wird gezeigt, wie Sie ein Schaltflächensteuerelement für die **QuickStatus-App** hinzufügen, wenn der Modus für den einzelnen Eintrag deaktiviert ist (das Kontrollkästchen Einzelner **Eintragsmodus** ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="69ef7-302">Procedure 4 shows how to add a button control for the **QuickStatus** app when single entry mode is off (the **Single Entry Mode** check box is clear).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="69ef7-303">Allgemeine Informationen zum Hinzufügen benutzerdefinierter Aktionen zu einem Menüband oder zu einem Menü in einer SharePoint-Anwendung finden Sie unter [Create custom actions to deploy with apps for SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span><span class="sxs-lookup"><span data-stu-id="69ef7-303">For general information about adding custom actions to a ribbon or to a menu in a SharePoint application, see [Create custom actions to deploy with apps for SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span></span> 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a><span data-ttu-id="69ef7-304">Prozedur 4.</span><span class="sxs-lookup"><span data-stu-id="69ef7-304">Procedure 4.</span></span> <span data-ttu-id="69ef7-305">So fügen Sie der Seite Aufgaben eine benutzerdefinierte Menübandaktion hinzu</span><span class="sxs-lookup"><span data-stu-id="69ef7-305">To add a ribbon custom action to the Tasks page</span></span>

1. <span data-ttu-id="69ef7-306">Untersuchen Sie das Menüband auf der Seite Aufgaben in Project Web App.</span><span class="sxs-lookup"><span data-stu-id="69ef7-306">Examine the ribbon on the Tasks page in Project Web App.</span></span> <span data-ttu-id="69ef7-307">Wählen Sie auf **dem** Menüband die Registerkarte AUFGABEN aus, und planen Sie, wie sie geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="69ef7-307">Select the **TASKS** tab on the ribbon and plan how to modify it.</span></span> <span data-ttu-id="69ef7-308">Es gibt sieben Gruppen, z. **B. Submit**, **Tasks** und **Period**.</span><span class="sxs-lookup"><span data-stu-id="69ef7-308">There are seven groups, such as **Submit**, **Tasks**, and **Period**.</span></span> <span data-ttu-id="69ef7-309">Die **Gruppe** Übermitteln verfügt über zwei Steuerelemente, eine **Schaltfläche Speichern** und ein Dropdownmenü Status senden. </span><span class="sxs-lookup"><span data-stu-id="69ef7-309">The **Submit** group has two controls, a **Save** button and a **Send Status** drop-down menu.</span></span> <span data-ttu-id="69ef7-310">Sie können ein Steuerelement an einem beliebigen Ort in einer Gruppe hinzufügen, eine Gruppe mit einem neuen Steuerelement an einem beliebigen Speicherort auf der Registerkarte AUFGABEN hinzufügen oder eine weitere Menübandregisterkarte mit benutzerdefinierten Gruppen und Steuerelementen hinzufügen. </span><span class="sxs-lookup"><span data-stu-id="69ef7-310">You can add a control at any location in a group, add a group with a new control at any location in the **TASKS** tab, or add another ribbon tab that has custom groups and controls.</span></span> <span data-ttu-id="69ef7-311">In diesem Beispiel fügen wir der  Gruppe Übermitteln eine dritte Schaltfläche hinzu, in der die Schaltfläche die URL der **QuickStatus-App** aufruft.</span><span class="sxs-lookup"><span data-stu-id="69ef7-311">In this example, we add a third button to the **Submit** group, where the button invokes the URL of the **QuickStatus** app.</span></span> 
    
2. <span data-ttu-id="69ef7-312">Klicken Sie **im** Bereich Projektmappen-Explorer in Visual Studio mit der rechten Maustaste auf das **Projekt QuickStatus,** und fügen Sie dann ein neues Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-312">In the **Solution Explorer** pane in Visual Studio, right-click the **QuickStatus** project, and then add a new item.</span></span> <span data-ttu-id="69ef7-313">Wählen Sie im Dialogfeld **Neues Element** hinzufügen die Option **Benutzerdefinierte Menübandaktion** aus (siehe Abbildung 4).</span><span class="sxs-lookup"><span data-stu-id="69ef7-313">In the **Add New Item** dialog box, choose **Ribbon Custom Action** (see Figure 4).</span></span> <span data-ttu-id="69ef7-314">Nennen Sie beispielsweise die benutzerdefinierte Aktion RibbonQuickStatusAction, und wählen Sie dann **Hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-314">For example, name the custom action RibbonQuickStatusAction, and then choose **Add**.</span></span>
    
   <span data-ttu-id="69ef7-315">**Abbildung 4. Hinzufügen einer benutzerdefinierten Menübandaktion**</span><span class="sxs-lookup"><span data-stu-id="69ef7-315">**Figure 4. Adding a ribbon custom action**</span></span>

   <span data-ttu-id="69ef7-316">![Hinzufügen einer benutzerdefinierten Menübandaktion](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Hinzufügen einer benutzerdefinierten Menübandaktion")</span><span class="sxs-lookup"><span data-stu-id="69ef7-316">![Adding a ribbon custom action](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Adding a ribbon custom action")</span></span>
  
3. <span data-ttu-id="69ef7-317">Lassen Sie auf  der ersten Seite des Assistenten Benutzerdefinierte Aktion für Menüband erstellen die Option **Hostweb** ausgewählt, **wählen** Sie in der Dropdownliste keine für den benutzerdefinierten Aktionsbereich aus, und wählen Sie dann **Weiter** aus (siehe Abbildung 5).</span><span class="sxs-lookup"><span data-stu-id="69ef7-317">On the first page of the **Create Custom Action for Ribbon** wizard, leave the **Host Web** option selected, choose **None** in the drop-down list for the custom action scope, and then choose **Next** (see Figure 5).</span></span> <span data-ttu-id="69ef7-318">Die Elemente in den Dropdownlisten sind relevant für SharePoint, nicht für Project Server.</span><span class="sxs-lookup"><span data-stu-id="69ef7-318">The items in the drop-down lists are relevant to SharePoint, not to Project Server.</span></span> <span data-ttu-id="69ef7-319">Wir ersetzen den Großteil der generierten XML für die benutzerdefinierte Aktion, sodass sie auf Project angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="69ef7-319">We will replace most of the generated XML for the custom action so that it applies to Project Server.</span></span> 
    
   <span data-ttu-id="69ef7-320">**Abbildung 5. Angeben von Eigenschaften für die benutzerdefinierte Menübandaktion**</span><span class="sxs-lookup"><span data-stu-id="69ef7-320">**Figure 5. Specifying properties for the ribbon custom action**</span></span>

   <span data-ttu-id="69ef7-321">![Festlegen von Eigenschaften für die benutzerdefinierte Menübandaktion](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Festlegen von Eigenschaften für die benutzerdefinierte Menübandaktion")</span><span class="sxs-lookup"><span data-stu-id="69ef7-321">![Specifying properties for the ribbon custom action](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Specifying properties for the ribbon custom action")</span></span>
  
4. <span data-ttu-id="69ef7-322">Lassen Sie auf  der nächsten Seite des Assistenten Benutzerdefinierte Aktion für Menüband erstellen alle Standardwerte für die Einstellungen, und wählen Sie dann **Fertig** stellen aus (siehe Abbildung 6).</span><span class="sxs-lookup"><span data-stu-id="69ef7-322">On the next page of the **Create Custom Action for Ribbon** wizard, leave all the default values for the settings, and then choose **Finish** (see Figure 6).</span></span> <span data-ttu-id="69ef7-323">Visual Studio erstellt den **Ordner RibbonQuickStatusAction,** der eine Elements.xml enthält.</span><span class="sxs-lookup"><span data-stu-id="69ef7-323">Visual Studio creates the **RibbonQuickStatusAction** folder, which contains an Elements.xml file.</span></span> 
    
   <span data-ttu-id="69ef7-324">**Abbildung 6. Angeben der Einstellungen für ein Schaltflächensteuerelement**</span><span class="sxs-lookup"><span data-stu-id="69ef7-324">**Figure 6. Specifying the settings for a button control**</span></span>

   <span data-ttu-id="69ef7-325">![Festlegen der Einstellungen für ein Schaltflächensteuerelement](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Festlegen der Einstellungen für ein Schaltflächensteuerelement")</span><span class="sxs-lookup"><span data-stu-id="69ef7-325">![Specifying the settings for a button control](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Specifying the settings for a button control")</span></span>
  
5. <span data-ttu-id="69ef7-326">Ändern Sie den standardmäßig generierten Code in der Elements.xml für die benutzerdefinierte Menübandaktion.</span><span class="sxs-lookup"><span data-stu-id="69ef7-326">Modify the default generated code in the Elements.xml file for the ribbon custom action.</span></span> <span data-ttu-id="69ef7-327">Im Folgenden finden Sie den standardmäßigen XML-Code:</span><span class="sxs-lookup"><span data-stu-id="69ef7-327">Following is the default XML code:</span></span>
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. <span data-ttu-id="69ef7-328">Löschen Sie **im CustomAction-Element** das **Sequence-Attribut** und das **Title-Attribut.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-328">In the **CustomAction** element, delete the **Sequence** attribute and the **Title** attribute.</span></span> 
    
   2. <span data-ttu-id="69ef7-329">Um der Gruppe  Übermitteln ein Steuerelement hinzuzufügen, suchen Sie die erste Gruppe in der Auflistung in der pwaribbon.xml-Datei, die das Element ist, das `Ribbon.ContextualTabs.MyWork.Home.Groups` beginnt, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"` .</span><span class="sxs-lookup"><span data-stu-id="69ef7-329">To add a control to the **Submit** group, find the first group in the  `Ribbon.ContextualTabs.MyWork.Home.Groups` collection in the pwaribbon.xml file, which is the element that begins,  `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`.</span></span> <span data-ttu-id="69ef7-330">Um der Gruppe Übermitteln  ein untergeordnetes Steuerelement hinzuzufügen, zeigt der folgende Code das richtige **Location-Attribut** des **CommandUIDefinition-Elements** in Elements.xml Datei:</span><span class="sxs-lookup"><span data-stu-id="69ef7-330">To add a child control to the **Submit** group, the following code shows the correct **Location** attribute of the **CommandUIDefinition** element in the Elements.xml file:</span></span> 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. <span data-ttu-id="69ef7-331">Ändern Sie die Attributwerte des **untergeordneten Button-Elements** wie folgt:</span><span class="sxs-lookup"><span data-stu-id="69ef7-331">Change the attribute values of the child **Button** element as follows:</span></span> 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - <span data-ttu-id="69ef7-332">Damit die Schaltfläche zum dritten Steuerelement in der Gruppe wird, kann das **Sequence-Attribut** eine beliebige Zahl höher sein als der Wert des vorhandenen  `Sequence="20"` Send **Status-Steuerelements** (ein **FlyoutAnchor-Element** in pwaribbon.xml).</span><span class="sxs-lookup"><span data-stu-id="69ef7-332">To make the button the third control in the group, the **Sequence** attribute can be any number higher than the  `Sequence="20"` value of the existing **Send Status** control (which is a **FlyoutAnchor** element in pwaribbon.xml).</span></span> <span data-ttu-id="69ef7-333">Standardmäßig sind die Sequenznummern von Gruppen und Steuerelementen , wodurch  `10, 20, 30, …` Elemente in Zwischenpositionen eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="69ef7-333">By convention, the sequence numbers of groups and controls are  `10, 20, 30, …`, which enables elements to be inserted in intermediate positions.</span></span>
    
       - <span data-ttu-id="69ef7-334">Das **Command-Attribut** gibt den Befehl an, der im **CommandUIHandler-Element** ausgeführt werden soll (siehe den folgenden Schritt 5.d).</span><span class="sxs-lookup"><span data-stu-id="69ef7-334">The **Command** attribute specifies the command to run in the **CommandUIHandler** element (see the following step 5.d).</span></span> <span data-ttu-id="69ef7-335">Sie können den Befehlsnamen vereinfachen, um es dem nächsten Entwickler zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="69ef7-335">You can simplify the command name to make it easier for the next developer.</span></span> <span data-ttu-id="69ef7-336">Beispielsweise ist  `Command="Invoke_QuickStatus"` das Lesen einfacher als  `Command="Invoke_RibbonQuickStatusActionButtonRequest"` .</span><span class="sxs-lookup"><span data-stu-id="69ef7-336">For example  `Command="Invoke_QuickStatus"` is easier to read than  `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.</span></span>
    
       - <span data-ttu-id="69ef7-337">Die Bildattribute geben das 16 x 16-Pixel-Symbol und das 32 x 32-Pixel-Symbol für das Schaltflächensteuerelement an.</span><span class="sxs-lookup"><span data-stu-id="69ef7-337">The image attributes specify the 16 x 16-pixel icon and the 32 x 32-pixel icon for the button control.</span></span> <span data-ttu-id="69ef7-338">Gibt in der Elements.xml-Datei  `Image32by32="_layouts/15/images/placeholder32x32.png"` einen orangefarbenen Punkt an.</span><span class="sxs-lookup"><span data-stu-id="69ef7-338">In the default Elements.xml file,  `Image32by32="_layouts/15/images/placeholder32x32.png"` specifies an orange dot.</span></span> <span data-ttu-id="69ef7-339">Sie können Symbole aus den Bildzuordnungsdateien (ps16x16.png und ps32x32.png) extrahieren, die im Verzeichnis auf dem Computer installiert sind, auf dem `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Project Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69ef7-339">You can extract icons from the image map files (ps16x16.png and ps32x32.png) that are installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` directory on the computer running Project Server.</span></span> <span data-ttu-id="69ef7-340">Beispielsweise befindet sich das Symbol mit 32 x 32 Pixeln in der zweiten Spalte mit Symbolen von links und der zehnten Zeile unten am oberen Rand der ps32x32.png-Bildkarte (der obere Rand des Symbols liegt hinter dem Ende der neunten Zeile; 9 Zeilen x 32 Pixel/Zeile = 288 Pixel).</span><span class="sxs-lookup"><span data-stu-id="69ef7-340">For example, the 32 x 32-pixel icon is in the second column of icons from the left and the tenth row down from the top of the ps32x32.png image map (the top of the icon is after the end of the ninth row; 9 rows x 32 pixels/row = 288 pixels).</span></span> 
    
       - <span data-ttu-id="69ef7-341">Fügen Sie zum Anzeigen einer QuickInfo für das Schaltflächensteuerelement das **ToolTipTitle-Attribut** und das **ToolTipDescription-Attribut** hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-341">To show a tool tip for the button control, add the **ToolTipTitle** attribute and the **ToolTipDescription** attribute.</span></span> 
    
    4. <span data-ttu-id="69ef7-342">Ändern Sie die Attribute des **CommandUIHandler-Elements.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-342">Change the attributes of the **CommandUIHandler** element.</span></span> <span data-ttu-id="69ef7-343">Stellen Sie beispielsweise sicher, dass das **Command-Attribut** dem **Command-Attributwert** für das **Button-Element** entspricht.</span><span class="sxs-lookup"><span data-stu-id="69ef7-343">For example, ensure that the **Command** attribute matches the **Command** attribute value for the **Button** element.</span></span> <span data-ttu-id="69ef7-344">Für das **CommandAction-Attribut** `~appWebUrl` ist ein Platzhalter für die URL der **QuickStatus-Webseite.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-344">For the **CommandAction** attribute,  `~appWebUrl` is a placeholder for the URL of the **QuickStatus** webpage.</span></span> <span data-ttu-id="69ef7-345">Wenn die Menübandschaltfläche die **QuickStatus-App** aufruft, wird das **{StandardTokens}-Token** durch #A0 ersetzt, die **SPHostUrl,** **SPLanguage,** **SPClientTag,** **SPProductNumber** und **SPAppWebUrl enthalten.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-345">When the ribbon button invokes the **QuickStatus** app, the **{StandardTokens}** token is replaced by URL options that include **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**, and **SPAppWebUrl**.</span></span>
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. <span data-ttu-id="69ef7-346">Öffnen Sie im Projektmappen-Explorer den **Feature1.feature-Designer,** und  verschieben Sie das  **RibbonQuickStatusAction-Element** aus dem Bereich Elemente im Projektmappenbereich in die Elemente im **Featurebereich.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-346">In **Solution Explorer**, open the **Feature1.feature** designer, and move the **RibbonQuickStatusAction** item from the **Items in the Solution** pane to the **Items in the Feature** pane.</span></span> <span data-ttu-id="69ef7-347">Wenn Sie dann den **Package.package-Designer** öffnen, befindet sich das **RibbonQuickStatusAction-Element** im Bereich Elemente **im Bereich** Paket.</span><span class="sxs-lookup"><span data-stu-id="69ef7-347">If you then open the **Package.package** designer, the **RibbonQuickStatusAction** item will be in the **Items in the Package** pane.</span></span> 
    
<span data-ttu-id="69ef7-348">Während Sie die App entwickeln und eine Menübandschaltfläche hinzufügen, testen Sie normalerweise die App und legen haltepunkte im JavaScript-Code für das Debuggen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-348">As you develop the app and add a ribbon button, you normally test the app and set breakpoints in the JavaScript code for debugging.</span></span> <span data-ttu-id="69ef7-349">Wenn Sie **F5** drücken, um das Debuggen zu starten, kompiliert Visual Studio die App, stellt sie auf der Website zur Verfügung, die in der **Website-URL-Eigenschaft** des **QuickStatus-Projekts** angegeben ist, und zeigt eine Seite an, die fragt, ob Sie der App vertrauen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-349">When you press **F5** to start debugging, Visual Studio compiles the app, deploys it to the site that is specified in the **Site URL** property of the **QuickStatus** project, and displays a page that asks whether you trust the app.</span></span> <span data-ttu-id="69ef7-350">Wenn Sie fortfahren und die **QuickStatus-App** beenden, kehrt sie zur Seite Aufgaben in Project Web App zurück.</span><span class="sxs-lookup"><span data-stu-id="69ef7-350">When you proceed and then exit the **QuickStatus** app, it returns to the Tasks page in Project Web App.</span></span> 

> [!NOTE]
> <span data-ttu-id="69ef7-351">Abbildung 7 zeigt, dass die **Schaltfläche Schnellstatus** auf der Registerkarte **AUFGABEN** des Menübands deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-351">Figure 7 shows that the **Quick Status** button on the **TASKS** tab of the ribbon is disabled.</span></span> <span data-ttu-id="69ef7-352">Nach vielen Debugbereitstellungen mit Visual Studio können benutzerdefinierte Menübandsteuerelemente blockiert werden, wenn Sie die veröffentlichte App weiterhin auf demselben Testserver debuggen oder bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-352">After many debug deployments with Visual Studio, custom ribbon controls can be blocked when you continue to debug or deploy the published app on the same test server.</span></span> <span data-ttu-id="69ef7-353">Um die Schaltfläche zu aktivieren, löschen Sie das **RibbonQuickStatusAction-Element** in Visual Studio, und erstellen Sie dann eine neue Menübandaktion mit einem anderen Namen und einer anderen ID.</span><span class="sxs-lookup"><span data-stu-id="69ef7-353">To enable the button, delete the **RibbonQuickStatusAction** item in Visual Studio, and then create a new ribbon action that has a different name and ID.</span></span> <span data-ttu-id="69ef7-354">Wenn das Problem damit nicht gelöst wird, versuchen Sie, die App aus der Project Web App-Testinstanz zu entfernen, und erstellen Sie die App dann mit einer anderen App-ID neu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-354">If that doesn't solve the problem, try removing the app from the Project Web App test instance, and then recreate the app with a different app ID.</span></span> 
  
<span data-ttu-id="69ef7-355">**Abbildung 7. Anzeigen der QuickInfo der deaktivierten Schaltfläche "Schnellstatus"**</span><span class="sxs-lookup"><span data-stu-id="69ef7-355">**Figure 7. Viewing the tooltip of the disabled Quick Status button**</span></span>

<span data-ttu-id="69ef7-356">![Anzeigen der QuickInfo der deaktivierten Schaltfläche](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Anzeigen der QuickInfo der deaktivierten Schaltfläche")</span><span class="sxs-lookup"><span data-stu-id="69ef7-356">![Viewing the tooltip of the disabled button](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Viewing the tooltip of the disabled button")</span></span>
  
<span data-ttu-id="69ef7-357">In Verfahren 5 wird gezeigt, wie Sie die **QuickStatus-App** bereitstellen und installieren.</span><span class="sxs-lookup"><span data-stu-id="69ef7-357">Procedure 5 shows how to deploy and install the **QuickStatus** app.</span></span> <span data-ttu-id="69ef7-358">In Verfahren 6 werden einige zusätzliche Schritte zum Testen der App nach der Installation gezeigt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-358">Procedure 6 shows some additional steps in testing the app after you have installed it.</span></span> 

<span data-ttu-id="69ef7-359"><a name="pj15_StatusingApp_Deploying"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-359"><a name="pj15_StatusingApp_Deploying"> </a></span></span>

## <a name="deploying-the-quickstatus-app"></a><span data-ttu-id="69ef7-360">Bereitstellen der QuickStatus-App</span><span class="sxs-lookup"><span data-stu-id="69ef7-360">Deploying the QuickStatus app</span></span>

<span data-ttu-id="69ef7-361">Es gibt mehrere Möglichkeiten zum Bereitstellen einer App in SharePoint Webanwendung, z. B. Project Web App.</span><span class="sxs-lookup"><span data-stu-id="69ef7-361">There are several ways to deploy an app to a SharePoint web application such as Project Web App.</span></span> <span data-ttu-id="69ef7-362">Welche Bereitstellung Sie verwenden, hängt davon ab, ob Sie die App in einem privaten SharePoint-Katalog oder im öffentlichen Office Store veröffentlichen möchten und ob SharePoint lokal installiert ist oder ein Online-Mandanzunternehmen ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-362">Which deployment you use will depend on whether you want to publish the app to a private SharePoint catalog or to the public Office Store, and whether SharePoint is installed on-premises or is an online tenancy.</span></span> <span data-ttu-id="69ef7-363">In Verfahren 5 wird gezeigt, wie Die **QuickStatus-App** in einer lokalen Installation in einem privaten App-Katalog bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="69ef7-363">Procedure 5 shows how to deploy the **QuickStatus** app to an on-premises installation in a private app catalog.</span></span> <span data-ttu-id="69ef7-364">Weitere Informationen finden Sie unter [Installieren und Verwalten von Apps für SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) und Veröffentlichen von Apps für [SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span><span class="sxs-lookup"><span data-stu-id="69ef7-364">For more information, see [Install and manage apps for SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) and [Publish apps for SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span></span>
  
> [!NOTE]
> <span data-ttu-id="69ef7-365">Das Hinzufügen einer App zu einem SharePoint erfordert SharePoint Administratorberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-365">Adding an app to a SharePoint catalog requires SharePoint administrator permissions.</span></span> 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a><span data-ttu-id="69ef7-366">Prozedur 5.</span><span class="sxs-lookup"><span data-stu-id="69ef7-366">Procedure 5.</span></span> <span data-ttu-id="69ef7-367">So stellen Sie die QuickStatus-App zur Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="69ef7-367">To deploy the QuickStatus app</span></span>

1. <span data-ttu-id="69ef7-368">Speichern Visual Studio Alle Dateien, und klicken Sie dann im Projektmappen-Explorer  mit der rechten Maustaste auf das **Projekt QuickStatus,** und wählen Sie **Veröffentlichen aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-368">In Visual Studio, save all of the files, and then right-click the **QuickStatus** project in the **Solution Explorer** and choose **Publish**.</span></span>
    
2. <span data-ttu-id="69ef7-369">Da die **QuickStatus-App** SharePoint gehostet wird, gibt es nur sehr wenige Optionen für die Veröffentlichung (siehe Abbildung 8).</span><span class="sxs-lookup"><span data-stu-id="69ef7-369">Because the **QuickStatus** app is SharePoint-hosted, there are very few options for publishing (see Figure 8).</span></span> <span data-ttu-id="69ef7-370">Wählen Sie **im Dialogfeld Apps für Office und SharePoint** veröffentlichen die Option Fertig stellen **aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-370">In the **Publish apps for Office and SharePoint** dialog box, choose **Finish**.</span></span>
    
   <span data-ttu-id="69ef7-371">**Abbildung 8. Veröffentlichen der QuickStatus-App**</span><span class="sxs-lookup"><span data-stu-id="69ef7-371">**Figure 8. Publishing the QuickStatus app**</span></span>

   <span data-ttu-id="69ef7-372">![Verwenden des Assistenten zum Veröffentlichen](media/pj15_CreateStatusingApp_PublishWizard.gif "Verwenden des Assistenten zum Veröffentlichen")</span><span class="sxs-lookup"><span data-stu-id="69ef7-372">![Using the Publish Wizard](media/pj15_CreateStatusingApp_PublishWizard.gif "Using the Publish Wizard")</span></span>
  
3. <span data-ttu-id="69ef7-373">Kopieren Sie QuickStatus.app Datei aus dem Verzeichnis in ein bequemes Verzeichnis auf dem lokalen Computer (oder auf den SharePoint für eine lokale `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` Installation).</span><span class="sxs-lookup"><span data-stu-id="69ef7-373">Copy the QuickStatus.app file from the  `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` directory to a convenient directory on the local computer (or to the SharePoint computer for an on-premises installation).</span></span> 
    
4. <span data-ttu-id="69ef7-374">Wählen SharePoint In der Zentraladministration **apps** in der Schnellstart-Option aus, und wählen Sie **dann App-Katalog verwalten aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-374">In SharePoint Central Administration, choose **Apps** in the Quick Launch, and then choose **Manage App Catalog**.</span></span>
    
5. <span data-ttu-id="69ef7-375">Wenn kein App-Katalog vorhanden ist, erstellen Sie eine Websitesammlung für den App-Katalog, indem Sie den Abschnitt Konfigurieren der *App-Katalogwebsite* für eine Webanwendung unter Verwalten des App-Katalogs [in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx)folgen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-375">If an app catalog does not exist, create a site collection for the app catalog, by following the  *Configure the App Catalog site for a web application*  section in [Manage the App Catalog in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).</span></span>
    
   <span data-ttu-id="69ef7-376">Wenn ein App-Katalog vorhanden ist, navigieren Sie zur Website-URL auf der Seite App-Katalog verwalten.</span><span class="sxs-lookup"><span data-stu-id="69ef7-376">If an app catalog exists, navigate to the site URL on the Manage App Catalog page.</span></span> <span data-ttu-id="69ef7-377">In den folgenden Schritten ist beispielsweise die Website für den App-Katalog  `https://ServerName/sites/TestApps` .</span><span class="sxs-lookup"><span data-stu-id="69ef7-377">For example, in the following steps, the app catalog site is  `https://ServerName/sites/TestApps`.</span></span>
    
6. <span data-ttu-id="69ef7-378">Wählen Sie auf der Seite App-Katalog die Option **Apps for SharePoint** in der Schnellstartseite aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-378">On the app catalog page, choose **Apps for SharePoint** in the Quick Launch.</span></span> <span data-ttu-id="69ef7-379">Wählen Sie auf der Seite Apps SharePoint auf der Registerkarte **DATEIEN** des Menübands die Option **Hochladen Dokument aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-379">On the Apps for SharePoint page, on the **FILES** tab of the ribbon, choose **Upload Document**.</span></span>
    
7. <span data-ttu-id="69ef7-380">Suchen Sie **im** Dialogfeld Dokument hinzufügen nach der QuickStatus.app, fügen Sie Kommentare für die Version hinzu, und wählen Sie dann **OK aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-380">In the **Add a document** dialog box, browse for the QuickStatus.app file, add comments for the version, and then choose **OK**.</span></span>
    
8. <span data-ttu-id="69ef7-381">Wenn Sie eine App hinzufügen, können Sie auch lokale Informationen für die App-Beschreibung, das Symbol und andere Informationen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-381">When you add an app, you can also add local information for the app description, icon, and other information.</span></span> <span data-ttu-id="69ef7-382">Fügen Sie **im Dialogfeld Apps for SharePoint - QuickStatus.app** die Informationen hinzu, die Sie für die App in der SharePoint anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="69ef7-382">In the **Apps for SharePoint - QuickStatus.app** dialog box, add the information that you want to show for the app in the SharePoint site collection.</span></span> <span data-ttu-id="69ef7-383">Fügen Sie beispielsweise die folgenden Informationen hinzu:</span><span class="sxs-lookup"><span data-stu-id="69ef7-383">For example, add the following information:</span></span> 
    
   1. <span data-ttu-id="69ef7-384">**Feld Kurze Beschreibung:** Geben Sie Schnellstatus-Test-App ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-384">**Short Description** field: Type Quick Status test app.</span></span>
    
   2. <span data-ttu-id="69ef7-385">**Beschreibungsfeld:** Geben Sie Test app to update percent complete for tasks in multiple projects ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-385">**Description** field: Type Test app to update percent complete for tasks in multiple projects.</span></span>
    
   3. <span data-ttu-id="69ef7-386">**Symbol-URL-Felder:** Fügen Sie den Websiteressourcen für den App-Katalog ein 96 x 96-Pixel-Bild für das App-Symbol hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-386">**Icon URL** fields: Add a 96 x 96-pixel image for the app icon to the site assets for the app catalog.</span></span> <span data-ttu-id="69ef7-387">Navigieren Sie beispielsweise zu , wählen Sie im Dropdownmenü Einstellungen Websiteinhalte aus, wählen Sie `https://ServerName/sites/TestApps` **Websiteressourcen**  aus, und fügen Sie dann das quickStatusApp.png hinzu. </span><span class="sxs-lookup"><span data-stu-id="69ef7-387">For example, navigate to  `https://ServerName/sites/TestApps`, choose **Site contents** in the **Settings** drop-down menu, choose **Site Assets**, and then add the quickStatusApp.png image.</span></span> <span data-ttu-id="69ef7-388">Klicken Sie mit der rechten Maustaste auf das **quickStatusApp-Element,** wählen Sie **Eigenschaften** aus, und kopieren Sie dann den **Wert Address (URL)** im **Dialogfeld** Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69ef7-388">Right-click the **quickStatusApp** item, choose **Properties**, and then copy the **Address (URL)** value in the **Properties** dialog box.</span></span> <span data-ttu-id="69ef7-389">Kopieren Sie beispielsweise , und fügen Sie den Wert dann in das  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png` Feld **Symbol-URL-Webadresse** ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-389">For example, copy  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`, and then paste the value in the **Icon URL** web address field.</span></span> <span data-ttu-id="69ef7-390">Geben Sie eine Beschreibung für das Symbol ein, z. B. (wie in Abbildung 9), geben Sie QuickStatus-App-Symbol ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-390">Type a description for the icon, for example (as in Figure 9), type QuickStatus app icon.</span></span> <span data-ttu-id="69ef7-391">Testen Sie, ob die URL gültig ist.</span><span class="sxs-lookup"><span data-stu-id="69ef7-391">Test that the URL is valid.</span></span>
    
      <span data-ttu-id="69ef7-392">**Abbildung 9. Hinzufügen einer Symbol-URL für die QuickStatus-App**</span><span class="sxs-lookup"><span data-stu-id="69ef7-392">**Figure 9. Adding an icon URL for the QuickStatus app**</span></span>

      <span data-ttu-id="69ef7-393">![Festlegen von Eigenschaften für die App in SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Festlegen von Eigenschaften für die App in SharePoint")</span><span class="sxs-lookup"><span data-stu-id="69ef7-393">![Setting properties in SharePoint for the app](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Setting properties in SharePoint for the app")</span></span>
  
   4. <span data-ttu-id="69ef7-394">**Kategoriefeld:** Wählen Sie eine vorhandene Kategorie aus, oder geben Sie Einen eigenen Wert an.</span><span class="sxs-lookup"><span data-stu-id="69ef7-394">**Category** field: Choose an existing category, or specify your own value.</span></span> <span data-ttu-id="69ef7-395">Geben Sie beispielsweise Statusing ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-395">For example, type Statusing.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="69ef7-396">Eine Kategorie namens **Statusing** dient nur zu Testzwecken.</span><span class="sxs-lookup"><span data-stu-id="69ef7-396">A category named **Statusing** is just for testing purposes.</span></span> <span data-ttu-id="69ef7-397">Eine typische Kategorie für Project Server-Apps ist **Project Management**.</span><span class="sxs-lookup"><span data-stu-id="69ef7-397">A typical category for Project Server apps is **Project Management**.</span></span> 
  
   5. <span data-ttu-id="69ef7-398">**Publisher:** Geben Sie den Namen des Herausgebers ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-398">**Publisher name** field: Type the name of the publisher.</span></span> <span data-ttu-id="69ef7-399">Geben Sie in diesem Beispiel Project SDK ein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-399">In this example, type Project SDK.</span></span>
    
   6. <span data-ttu-id="69ef7-400">**Feld Aktiviert:** Aktivieren Sie das Kontrollkästchen Aktiviert, um die App für Project für die Installation sichtbar **zu** machen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-400">**Enabled** field: To make the app visible to Project Web App site administrators for installation, select the **Enabled** check box.</span></span> 
    
   7. <span data-ttu-id="69ef7-401">Zusätzliche Felder sind optional.</span><span class="sxs-lookup"><span data-stu-id="69ef7-401">Additional fields are optional.</span></span> <span data-ttu-id="69ef7-402">Sie können beispielsweise eine Support-URL und mehrere Hilfebilder für die Seite "App-Details" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-402">For example, you can add a support URL and multiple help images for the app details page.</span></span> <span data-ttu-id="69ef7-403">In Abbildung 9 enthalten die Felder **Bild-URL 1** die URL für einen Screenshot der App und eine Beschreibung des Screenshots.</span><span class="sxs-lookup"><span data-stu-id="69ef7-403">In Figure 9, the **Image URL 1** fields include the URL for a screenshot of the app and a description of the screenshot.</span></span> 
    
   8. <span data-ttu-id="69ef7-404">Wählen Sie **im SharePoint - QuickStatus.app** Dialogfeld Speichern **aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-404">In the **Apps for SharePoint - QuickStatus.app** dialog box, choose **Save**.</span></span> <span data-ttu-id="69ef7-405">In Abbildung 9 wird das Element Quick **Status Update** in der Bibliothek Apps für SharePoint zur Bearbeitung ausgecheckt.  Auf der Registerkarte **BEARBEITEN** des Dialogfeldbands würden Sie also Einchecken auswählen, um den Vorgang zu vervollständigen (siehe Abbildung 10).</span><span class="sxs-lookup"><span data-stu-id="69ef7-405">In Figure 9, the **Quick Status Update** item in the Apps for SharePoint library is checked out for editing, so on the **EDIT** tab of the dialog box ribbon, you would choose **Check In** to complete the process (see Figure 10).</span></span> 
    
      <span data-ttu-id="69ef7-406">**Abbildung 10. Die QuickStatus-App wird der Bibliothek Apps for SharePoint hinzugefügt.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-406">**Figure 10. The QuickStatus app is added to the Apps for SharePoint library.**</span></span>

      <span data-ttu-id="69ef7-407">![Die QuickStatus-App wird SharePoint hinzugefügt](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Die QuickStatus-App wird SharePoint hinzugefügt")</span><span class="sxs-lookup"><span data-stu-id="69ef7-407">![The QuickStatus app is added to SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "The QuickStatus app is added to SharePoint")</span></span>
  
9. <span data-ttu-id="69ef7-408">Wählen Project Web App im Dropdownmenü **Einstellungen** Hinzufügen **einer App aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-408">In Project Web App, in the **Settings** drop-down menu, choose **Add an app**.</span></span> <span data-ttu-id="69ef7-409">Wählen Sie auf der Seite Ihre Apps auf der Schnellstartleiste **Aus Ihrer** Organisation aus, und wählen Sie dann **App-Details** für die **App Für schnelles Statusupdate** aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-409">On the Your Apps page, in the Quick Launch, choose **From Your Organization**, and then choose **App Details** for the **Quick Status Update** app.</span></span> <span data-ttu-id="69ef7-410">Abbildung 11 zeigt die Detailseite mit dem App-Symbol, dem Screenshot und anderen Informationen, die Sie im vorherigen Schritt hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="69ef7-410">Figure 11 shows the details page with the app icon, screenshot, and other information that you added in the previous step.</span></span> 
    
   <span data-ttu-id="69ef7-411">**Abbildung 11. Verwenden der Detailseite "Quick Status Update" in Project Web App**</span><span class="sxs-lookup"><span data-stu-id="69ef7-411">**Figure 11. Using the Quick Status Update details page in Project Web App**</span></span>

   <span data-ttu-id="69ef7-412">![Hinzufügen der QuickStatus-App zu Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Hinzufügen der QuickStatus-App zu Project Web App")</span><span class="sxs-lookup"><span data-stu-id="69ef7-412">![Adding the QuickStatus app to Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Adding the QuickStatus app to Project Web App")</span></span>
  
10. <span data-ttu-id="69ef7-413">Wählen Sie auf der Seite Quick Status Update Details die Option **ADD IT aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-413">On the Quick Status Update details page, choose **ADD IT**.</span></span> <span data-ttu-id="69ef7-414">Project Web App zeigt ein Dialogfeld an, in dem die Vorgänge aufgeführt sind, die die QuickStatus-App ausführen kann (siehe Abbildung 12).</span><span class="sxs-lookup"><span data-stu-id="69ef7-414">Project Web App displays a dialog box that lists the operations that the QuickStatus app can perform (see Figure 12).</span></span> <span data-ttu-id="69ef7-415">Die Liste der Vorgänge wird von den **AppPermissionRequest-Elementen** in der AppManifest.xml abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="69ef7-415">The list of operations is derived from the **AppPermissionRequest** elements in the AppManifest.xml file.</span></span> 
    
    <span data-ttu-id="69ef7-416">**Abbildung 12. Überprüfen, ob Sie der Schnellstatus-App vertrauen**</span><span class="sxs-lookup"><span data-stu-id="69ef7-416">**Figure 12. Verifying that you trust the Quick Status app**</span></span>

    <span data-ttu-id="69ef7-417">![Überprüfen des Vertrauens gegenüber der QuickStatus-App](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Überprüfen des Vertrauens gegenüber der QuickStatus-App")</span><span class="sxs-lookup"><span data-stu-id="69ef7-417">![Verifying trust for the QuickStatus app](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Verifying trust for the QuickStatus app")</span></span>
  
11. <span data-ttu-id="69ef7-418">Wählen Sie **im Dialogfeld Schnellstatusaktualisierung** vertrauen die Option **Vertrauen aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-418">In the **Do you trust Quick Status Update** dialog box, choose **Trust It**.</span></span> <span data-ttu-id="69ef7-419">Die App wird der Seite Project Web App-Websiteinhalte hinzugefügt (siehe Abbildung 13).</span><span class="sxs-lookup"><span data-stu-id="69ef7-419">The app is added to the Project Web App Site Contents page (see Figure 13).</span></span>
    
    <span data-ttu-id="69ef7-420">**Abbildung 13. Anzeigen der Schnellstatus-App auf der Seite Websiteinhalte**</span><span class="sxs-lookup"><span data-stu-id="69ef7-420">**Figure 13. Viewing the Quick Status app on the Site Contents page**</span></span>

    <span data-ttu-id="69ef7-421">![Anzeigen der QuickStatus-App in den Websiteinhalten](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Anzeigen der QuickStatus-App in den Websiteinhalten")</span><span class="sxs-lookup"><span data-stu-id="69ef7-421">![Viewing the QuickStatus app in Site Contents](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Viewing the QuickStatus app in Site Contents")</span></span>
  
<span data-ttu-id="69ef7-422">Auf der Seite Websiteinhalte können Sie das Symbol Für **schnelles Statusupdate** auswählen, um die App ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="69ef7-422">On the Site Contents page, you can select the **Quick Status Update** icon to run the app.</span></span>

> [!NOTE]
> <span data-ttu-id="69ef7-423">Für zusätzliche Befehle, die Informationen zur App bereitstellen, wählen Sie  auf der Seite Websiteinhalte den Bereich aus, der den Namen des Schnellstatusupdates und die Auslassungspunkte (...) enthält. Sie können die Seite Informationen für die App überprüfen, die Seite App-Details anzeigen, die Informationen zu App-Fehlern enthält, die Seite app-Berechtigungen überprüfen oder die App aus Project Web App entfernen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-423">For additional commands that provide information about the app, on the Site Contents page, choose the region that contains the **Quick Status Update** name and the ellipsis (...). You can review the About page for the app, view the App Details page that contains information about app errors, review the app permissions page, or remove the app from Project Web App.</span></span> 
  
<span data-ttu-id="69ef7-424">Auf der Seite Aufgaben in Project Web App (siehe Abbildung 14) sollte die Schaltfläche **QuickStatus** im Menüband aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-424">On the Tasks page in Project Web App (see Figure 14), the **QuickStatus** button should be enabled on the ribbon.</span></span> <span data-ttu-id="69ef7-425">Wenn die **Schaltfläche Schnellstatus** deaktiviert ist, führen Sie die in der Anmerkung für Abbildung 7 beschriebenen Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-425">If the **Quick Status** button is disabled, try the actions described in the note for Figure 7.</span></span> 

<span data-ttu-id="69ef7-426">**Abbildung 14. Starten der QuickStatus-App über die Registerkarte TASKS**</span><span class="sxs-lookup"><span data-stu-id="69ef7-426">**Figure 14. Starting the QuickStatus app from the TASKS tab**</span></span>

<span data-ttu-id="69ef7-427">![Starten der QuickStatus-App von der Registerkarte "TASKS"](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starten der QuickStatus-App von der Registerkarte &quot;TASKS&quot;")</span><span class="sxs-lookup"><span data-stu-id="69ef7-427">![Starting the QuickStatus app from the TASKS tab](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starting the QuickStatus app from the TASKS tab")</span></span>
  
<span data-ttu-id="69ef7-428">In Prozedur 6 werden einige Tests gezeigt, die mit der QuickStatus-App durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-428">Procedure 6 shows some tests to make with the QuickStatus app.</span></span>

<span data-ttu-id="69ef7-429"><a name="pj15_StatusingApp_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-429"><a name="pj15_StatusingApp_Testing"> </a></span></span>

## <a name="testing-the-quickstatus-app"></a><span data-ttu-id="69ef7-430">Testen der QuickStatus-App</span><span class="sxs-lookup"><span data-stu-id="69ef7-430">Testing the QuickStatus app</span></span>

<span data-ttu-id="69ef7-431">Jeder Vorgang, den ein Benutzer in der **QuickStatus-App** ausprobieren kann, sollte auf einer Testinstallation von Project Server getestet werden, bevor die App auf einem Produktionsserver oder in einem Produktions mandanten von Project Online.</span><span class="sxs-lookup"><span data-stu-id="69ef7-431">Every operation that a user might try in the **QuickStatus** app should be tested on a test installation of Project Server before deploying the app to a production server or to a production tenant of Project Online.</span></span> <span data-ttu-id="69ef7-432">Mit einer Testinstallation können Sie Zuordnungen für Benutzer ändern und löschen, ohne dass sich dies auf die tatsächlichen Projekte ausdingt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-432">A test installation enables you to change and delete assignments for users without affecting actual projects.</span></span> <span data-ttu-id="69ef7-433">Tests sollten auch mehrere Benutzer mit unterschiedlichen Berechtigungssätzen umfassen, z. B. Administrator, Projektmanager und Teammitglied.</span><span class="sxs-lookup"><span data-stu-id="69ef7-433">Testing should also involve several users who have different sets of permissions, such as administrator, project manager, and team member.</span></span> <span data-ttu-id="69ef7-434">Bei gründlichen Tests können Änderungen aufgedeckt werden, die in der App vorgenommen werden sollten, die bei Tests während der Entwicklung nicht offensichtlich waren.</span><span class="sxs-lookup"><span data-stu-id="69ef7-434">Thorough testing can uncover changes that should be made in the app, which were not apparent in testing during development.</span></span> <span data-ttu-id="69ef7-435">Prozedur 6 listet mehrere Tests für die **QuickStatus-App** auf, enthält jedoch keine umfassende Reihe von Tests.</span><span class="sxs-lookup"><span data-stu-id="69ef7-435">Procedure 6 lists several tests for the **QuickStatus** app, but does not include an exhaustive series of tests.</span></span> 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a><span data-ttu-id="69ef7-436">Verfahren 6.</span><span class="sxs-lookup"><span data-stu-id="69ef7-436">Procedure 6.</span></span> <span data-ttu-id="69ef7-437">So testen Sie die QuickStatus-App</span><span class="sxs-lookup"><span data-stu-id="69ef7-437">To test the QuickStatus app</span></span>

1. <span data-ttu-id="69ef7-438">Führen Sie **die QuickStatus-App** aus, in der der Benutzer keine Zuweisungen hat.</span><span class="sxs-lookup"><span data-stu-id="69ef7-438">Run the **QuickStatus** app where the user has no assignments.</span></span> <span data-ttu-id="69ef7-439">Die App sollte am unteren Rand der Seite eine blaue Meldung anzeigen, z. B. Benutzername **hat keine Zuweisungen**.</span><span class="sxs-lookup"><span data-stu-id="69ef7-439">The app should show a blue message at the bottom of the page, for example, **User Name has no assignments**.</span></span>
    
   <span data-ttu-id="69ef7-440">Wählen **Sie Aktualisieren** aus, und die Nachrichtenänderungen zu grünen **Zuordnungen wurden aktualisiert.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-440">Choose **Update**, and the message changes to a green **Assignments have been updated**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="69ef7-441">Das Verhalten der App sollte so geändert werden, dass die Schaltfläche **Aktualisieren** deaktiviert ist, wenn keine Zuweisungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="69ef7-441">The app behavior should be changed so that the **Update** button is disabled when there are no assignments.</span></span> 
  
2. <span data-ttu-id="69ef7-442">Führen Sie die App aus, in der der Benutzer mehrere Zuordnungen in verschiedenen Projekten hat und einige Zuordnungen nicht abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="69ef7-442">Run the app where the user has multiple assignments in several different projects and some assignments are not complete.</span></span> <span data-ttu-id="69ef7-443">Beachten Sie die Darstellung der App, und führen Sie aktionen wie folgt aus (siehe Abbildung 15):</span><span class="sxs-lookup"><span data-stu-id="69ef7-443">Notice the appearance of the app and perform actions as follows (see Figure 15):</span></span>
    
   1. <span data-ttu-id="69ef7-444">Die **onGetAssignmentsSuccess-Funktion** erstellt eine Zeile in der Tabelle für jede Zuordnung für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="69ef7-444">The **onGetAssignmentsSuccess** function creates a row in the table for each assignment for the current user.</span></span> <span data-ttu-id="69ef7-445">Der Projektname wird nur einmal in fett formatierter Schriftart für die erste Zuordnung in jedem Projekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-445">The project name shows only once, in a bold font, for the first assignment in each project.</span></span> 
    
   2. <span data-ttu-id="69ef7-446">Aktivieren Sie das  Kontrollkästchen in der Spaltenüberschrift Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="69ef7-446">Clear the check box in the **Task name** column header.</span></span> <span data-ttu-id="69ef7-447">Der Ereignishandler für den Tabellenkopfklicken gibt alle anderen Kontrollkästchen in den Vorgangszeilen frei.</span><span class="sxs-lookup"><span data-stu-id="69ef7-447">The table header click event handler clears all of the other check boxes in the task rows.</span></span> 
    
   3. <span data-ttu-id="69ef7-448">Wählen Sie alle Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-448">Select all of the tasks.</span></span> <span data-ttu-id="69ef7-449">Der Click-Ereignishandler für jede Zeile bestimmt, ob alle Zeilen ausgewählt sind, und wählt in diesem Fall die Spaltenüberschrift **Vorgangsname** aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-449">The click event handler for each row determines whether all rows are selected, and if so, selects the **Task name** column header.</span></span> 
    
   4. <span data-ttu-id="69ef7-450">Löschen Sie alle Kontrollkästchen erneut, und wählen Sie dann eine Zuordnung mit verbleibender Arbeit aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-450">Clear all of the check boxes again, and then select one assignment that has some remaining work.</span></span> <span data-ttu-id="69ef7-451">In Abbildung 15 wird beispielsweise gezeigt, dass für die oberste Aufgabe T1 20 % verbleibende Arbeit übrig bleibt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-451">For example, Figure 15 shows the top task T1 has 20% remaining work to complete.</span></span>
    
   5. <span data-ttu-id="69ef7-452">Geben Sie **im Textfeld Prozent vollständig** festlegen 80 ein, und wählen Sie dann Aktualisieren **aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-452">In the **Set percent complete** text box, type 80, and then choose **Update**.</span></span> <span data-ttu-id="69ef7-453">Unten auf der Seite sollte eine grüne Meldung angezeigt werden, **Zuordnungen wurden aktualisiert.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-453">The bottom of the page should show a green message, **Assignments have been updated**.</span></span>
    
      <span data-ttu-id="69ef7-454">**Abbildung 15. Aktualisieren einer Zuordnung in der QuickStatus-App**</span><span class="sxs-lookup"><span data-stu-id="69ef7-454">**Figure 15. Updating an assignment in the QuickStatus app**</span></span>

      <span data-ttu-id="69ef7-455">![Aktualisieren einer Zuweisung in der QuickStatus-App](media/pj15_CreateStatusingApp_Testing1Update.gif "Aktualisieren einer Zuweisung in der QuickStatus-App")</span><span class="sxs-lookup"><span data-stu-id="69ef7-455">![Updating an assignment in the QuickStatus app](media/pj15_CreateStatusingApp_Testing1Update.gif "Updating an assignment in the QuickStatus app")</span></span>
  
3. <span data-ttu-id="69ef7-456">Wählen **Sie Aktualisieren** aus (siehe Abbildung 16).</span><span class="sxs-lookup"><span data-stu-id="69ef7-456">Choose **Refresh** (see Figure 16).</span></span> <span data-ttu-id="69ef7-457">Alle Aufgaben werden erneut ausgewählt, und die oberste Aufgabe zeigt 80 % abgeschlossen an.</span><span class="sxs-lookup"><span data-stu-id="69ef7-457">All of the tasks are selected again, and the top task shows 80% complete.</span></span> 
    
      <span data-ttu-id="69ef7-458">**Abbildung 16. Aktualisieren der Seite "Quick Status Update"**</span><span class="sxs-lookup"><span data-stu-id="69ef7-458">**Figure 16. Refreshing the Quick Status Update page**</span></span>

      <span data-ttu-id="69ef7-459">![Aktualisieren der QuickStatus-Seite](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Aktualisieren der QuickStatus-Seite")</span><span class="sxs-lookup"><span data-stu-id="69ef7-459">![Refreshing the QuickStatus page](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Refreshing the QuickStatus page")</span></span>
  
4. <span data-ttu-id="69ef7-460">Löschen Sie alle Kontrollkästchen, und wählen Sie dann einen anderen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="69ef7-460">Clear all of the check boxes, and then select another task.</span></span> <span data-ttu-id="69ef7-461">Wählen Sie z. B. **Neue Aufgabe aus PWA**.</span><span class="sxs-lookup"><span data-stu-id="69ef7-461">For example, select **New task from PWA**.</span></span> <span data-ttu-id="69ef7-462">Lassen Sie das Textfeld Prozent **vollständig festlegen** leer, löschen Sie den gesamten Text in der Spalte **% abgeschlossen** für die ausgewählte Aufgabe, und wählen Sie dann **Aktualisieren aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-462">Leave the **Set percent complete** text box empty, delete all text in the **% complete** column for the selected task, and then choose **Update**.</span></span> <span data-ttu-id="69ef7-463">Da beide Textfelder leer sind, zeigt die App eine rote Fehlermeldung an (siehe Abbildung 17).</span><span class="sxs-lookup"><span data-stu-id="69ef7-463">Because both text boxes are empty, the app shows a red error message (see Figure 17).</span></span>
    
      <span data-ttu-id="69ef7-464">**Abbildung 17. Testen der Fehlermeldung**</span><span class="sxs-lookup"><span data-stu-id="69ef7-464">**Figure 17. Testing the error message**</span></span>

      <span data-ttu-id="69ef7-465">![Testen der Fehlermeldung](media/pj15_CreateStatusingApp_Testing3Error.gif "Testen der Fehlermeldung")</span><span class="sxs-lookup"><span data-stu-id="69ef7-465">![Testing the error message](media/pj15_CreateStatusingApp_Testing3Error.gif "Testing the error message")</span></span>
  
5. <span data-ttu-id="69ef7-466">Aktualisieren Sie den vorherigen Vorgang auf 80 % abgeschlossen, und wählen Sie dann **Beenden aus.**</span><span class="sxs-lookup"><span data-stu-id="69ef7-466">Update the previous task to 80% complete, and then choose **Exit**.</span></span> <span data-ttu-id="69ef7-467">Die **exitToPwa-Funktion** ändert den Speicherort des Browserfensters in die Seite Aufgaben in der SharePoint Hostanwendung (d. h., die URL wird in https://ServerName/pwa/Tasks.aspx) geändert.</span><span class="sxs-lookup"><span data-stu-id="69ef7-467">The **exitToPwa** function changes the browser window location to the Tasks page in the SharePoint host application (that is, the URL changes to https://ServerName/pwa/Tasks.aspx).</span></span> <span data-ttu-id="69ef7-468">Abbildung 18 zeigt, dass der **T1-Vorgang** und der neue Vorgang aus **PWA** jeweils 80 % abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="69ef7-468">Figure 18 shows that the **T1** task and the **New task from PWA** task each show 80% complete.</span></span> 
    
      <span data-ttu-id="69ef7-469">**Abbildung 18. Überprüfen der Aktualisierung der Aufgaben in Project Web App**</span><span class="sxs-lookup"><span data-stu-id="69ef7-469">**Figure 18. Verifying the tasks are updated in Project Web App**</span></span>

      <span data-ttu-id="69ef7-470">![Überprüfen der aktualisierten Aufgaben in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Überprüfen der aktualisierten Aufgaben in Project Web App")</span><span class="sxs-lookup"><span data-stu-id="69ef7-470">![Verifying the updated tasks in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Verifying the updated tasks in Project Web App")</span></span>
  
6. <span data-ttu-id="69ef7-471">Bevor der aktualisierte Status in Project Professional 2013 angezeigt wird, müssen die Änderungen zur Genehmigung übermittelt und dann vom Projektmanager genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-471">Before the updated status shows in Project Professional 2013, the changes must be submitted for approval, and then approved by the project manager.</span></span>
    
<span data-ttu-id="69ef7-472">Tests zeigen verschiedene andere Änderungen an, die in der **QuickStatus-App** vorgenommen werden sollten, um die Benutzerfreundlichkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="69ef7-472">Testing reveals several other changes that should be made in the **QuickStatus** app for improved usability.</span></span> <span data-ttu-id="69ef7-473">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="69ef7-473">For example:</span></span>

- <span data-ttu-id="69ef7-474">Es sollten zusätzliche Fehlerüberprüfungen und Überprüfungen von Textfeldwerten durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-474">There should be additional error checks and validation of text box values.</span></span> <span data-ttu-id="69ef7-475">Derzeit kann ein Benutzer einen nicht numerischen oder einen negativen Wert für abgeschlossenen Prozentwert eingeben, was zu einer unfreundlichen Fehlermeldung führt.</span><span class="sxs-lookup"><span data-stu-id="69ef7-475">Currently, a user can enter a non-numeric value or a negative value for percent complete, which results in an unfriendly error message.</span></span> <span data-ttu-id="69ef7-476">Bei einem negativen Wert lautet die Fehlermeldung beispielsweise Fehleraktualisierungszuweisungen: **PJClientCallableException: StatusingSetDataValueInvalid**.</span><span class="sxs-lookup"><span data-stu-id="69ef7-476">For example, with a negative value, the error message is **Error updating assignments: PJClientCallableException: StatusingSetDataValueInvalid**.</span></span>
    
- <span data-ttu-id="69ef7-477">Die Fehlermeldung für leere Textfelder könnte das Projekt und den Vorgang zusätzlich zur Zeilennummer auflisten.</span><span class="sxs-lookup"><span data-stu-id="69ef7-477">The error message for blank text boxes could list the project and task, in addition to the row number.</span></span>
    
- <span data-ttu-id="69ef7-478">Die Erfolgsmeldung könnte eine Liste der aktualisierten Aufgaben enthalten. oder wenn die **updateAssignments-Funktion** erfolgreich ist, kann sie eine automatische Seitenaktualisierung durchführen und aktualisierte Aufgaben oder Prozentsätze in einer anderen Farbe und fett formatierten Schriftart anzeigen.</span><span class="sxs-lookup"><span data-stu-id="69ef7-478">The success message could include a list of the tasks updated; or if the **updateAssignments** function is successful, it could perform an automatic page refresh and show updated tasks or percentages in a different color and bold font.</span></span> 
    
- <span data-ttu-id="69ef7-479">Um eine sehr große Tabelle zu vermeiden, sollte die Zuordnungstabelle auf Vorgänge beschränkt sein, die weniger als 100 % abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="69ef7-479">To avoid a very large table, the table of assignments should be limited to tasks that are less than 100% complete.</span></span> <span data-ttu-id="69ef7-480">Oder fügen Sie eine Option zum Anzeigen aller Vorgänge hinzu.</span><span class="sxs-lookup"><span data-stu-id="69ef7-480">Or, add an option to show all tasks.</span></span> <span data-ttu-id="69ef7-481">Dieses Problem kann auch mithilfe eines jQuery-basierten Rasters anstelle einer Tabelle gelöst werden, in der Sie problemlos Filterung und Rasterauslagerung implementieren können.</span><span class="sxs-lookup"><span data-stu-id="69ef7-481">This problem could also be solved by using a jQuery-based grid instead of a table, where you can easily implement filtering and grid paging.</span></span>
    
- <span data-ttu-id="69ef7-482">Da  die **QuickStatus-App** den Status nicht übermittelt, wäre das Symbol **Schnellstatus** auf der  Registerkarte AUFGABEN des Menübands logischer das erste Symbol in der Gruppe Aufgaben und nicht das letzte Symbol in der Gruppe Absenden. </span><span class="sxs-lookup"><span data-stu-id="69ef7-482">Because the **QuickStatus** app does not submit status, the **Quick Status** icon on the **TASKS** tab of the ribbon would more logically be the first icon in the **Tasks** group, rather than the last icon in the **Submit** group.</span></span> 
    
- <span data-ttu-id="69ef7-483">Da die **onGetAssignmentsSuccess-Funktion** den **BtnSubmitUpdate-Schaltflächentext** initialisiert, die anderen Textwerte der Schaltflächen jedoch in HTML initialisiert werden, bleibt die Seite während der Ausgeführten der **getAssignments-Funktion** in einem teilweise initialisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="69ef7-483">Because the **onGetAssignmentsSuccess** function initializes the **btnSubmitUpdate** button text, but the other button text values are initialized in HTML, the page is left in a partially initialized state while the **getAssignments** function runs.</span></span> <span data-ttu-id="69ef7-484">Schaltflächen auf der Seite würden konsistenter angezeigt, wenn alle Textwerte in HTML initialisiert würden.</span><span class="sxs-lookup"><span data-stu-id="69ef7-484">Buttons on the page would appear more consistent if the text values were all initialized in HTML.</span></span> 
    
<span data-ttu-id="69ef7-485">Am wichtigsten ist, dass der von der **QuickStatus-App** verwendete Ansatz, bei dem die Prozent für Zuordnungen vollständig geändert wird, in einer Produktions-App überarbeitet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="69ef7-485">Most importantly, the approach that the **QuickStatus** app uses, where it changes percent complete for assignments, should be revised in a production app.</span></span> <span data-ttu-id="69ef7-486">Weitere Informationen finden Sie im [Abschnitt Nächste](#pj15_StatusingApp_NextSteps) Schritte.</span><span class="sxs-lookup"><span data-stu-id="69ef7-486">For more information, see the [Next steps](#pj15_StatusingApp_NextSteps) section.</span></span> 

<span data-ttu-id="69ef7-487"><a name="pj15_StatusingApp_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-487"><a name="pj15_StatusingApp_Example"> </a></span></span>

## <a name="example-code-for-the-quickstatus-app"></a><span data-ttu-id="69ef7-488">Beispielcode für die QuickStatus-App</span><span class="sxs-lookup"><span data-stu-id="69ef7-488">Example code for the QuickStatus app</span></span>

### <a name="defaultaspx-file"></a><span data-ttu-id="69ef7-489">Datei "Default.aspx"</span><span class="sxs-lookup"><span data-stu-id="69ef7-489">Default.aspx file</span></span>

<span data-ttu-id="69ef7-490">Der folgende Code befindet sich in `Pages\Default.aspx` der Datei des **QuickStatus-Projekts:**</span><span class="sxs-lookup"><span data-stu-id="69ef7-490">The following code is in the  `Pages\Default.aspx` file of the **QuickStatus** project:</span></span> 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a><span data-ttu-id="69ef7-491">App.js-Datei</span><span class="sxs-lookup"><span data-stu-id="69ef7-491">App.js file</span></span>

<span data-ttu-id="69ef7-492">Der folgende Code befindet sich in `Scripts\App.js` der Datei des **QuickStatus-Projekts:**</span><span class="sxs-lookup"><span data-stu-id="69ef7-492">The following code is in the  `Scripts\App.js` file of the **QuickStatus** project:</span></span> 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a><span data-ttu-id="69ef7-493">App.css-Datei</span><span class="sxs-lookup"><span data-stu-id="69ef7-493">App.css file</span></span>

<span data-ttu-id="69ef7-494">Der folgende CSS-Code befindet sich in `Content\App.css` der Datei des **QuickStatus-Projekts:**</span><span class="sxs-lookup"><span data-stu-id="69ef7-494">The following CSS code is in the  `Content\App.css` file of the **QuickStatus** project:</span></span> 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a><span data-ttu-id="69ef7-495">Elements.xml für das Menüband</span><span class="sxs-lookup"><span data-stu-id="69ef7-495">Elements.xml file for the ribbon</span></span>

<span data-ttu-id="69ef7-496">Die folgende XML-Definition für die hinzugefügte Schaltfläche auf der Registerkarte **TASKS** im Menüband befindet sich in der Datei `RibbonQuickStatusAction\Elements.xml` des **QuickStatus-Projekts:**</span><span class="sxs-lookup"><span data-stu-id="69ef7-496">The following XML definition, for the added button on the **TASKS** tab on the ribbon, is in the  `RibbonQuickStatusAction\Elements.xml` file of the **QuickStatus** project:</span></span> 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a><span data-ttu-id="69ef7-497">Die Datei "AppManifest.xml"</span><span class="sxs-lookup"><span data-stu-id="69ef7-497">AppManifest.xml file</span></span>

<span data-ttu-id="69ef7-498">Im Folgenden finden Sie die XML für das App-Manifest des **QuickStatus-Projekts,** das die beiden Berechtigungsanforderungsbereiche enthält, die zum Aktualisieren des Zuweisungsstatus des App-Benutzers in mehreren Projekten erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="69ef7-498">Following is the XML for the app manifest of the **QuickStatus** project, which includes the two permission request scopes that are necessary for updating the app user's assignment status in multiple projects:</span></span> 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a><span data-ttu-id="69ef7-499">AppIcon.png-Datei</span><span class="sxs-lookup"><span data-stu-id="69ef7-499">AppIcon.png file</span></span>

<span data-ttu-id="69ef7-500">Die vollständige Visual Studio für die **QuickStatus-App** enthält eine benutzerdefinierte AppIcon.png Datei.</span><span class="sxs-lookup"><span data-stu-id="69ef7-500">The complete Visual Studio solution for the **QuickStatus** app includes a custom AppIcon.png file.</span></span> <span data-ttu-id="69ef7-501">Die Lösung wird im Download des Project 2013 SDK enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="69ef7-501">The solution will be included in the Project 2013 SDK download.</span></span> 

<span data-ttu-id="69ef7-502"><a name="pj15_StatusingApp_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-502"><a name="pj15_StatusingApp_NextSteps"> </a></span></span>

## <a name="next-steps"></a><span data-ttu-id="69ef7-503">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="69ef7-503">Next steps</span></span>

<span data-ttu-id="69ef7-504">Die **QuickStatus-App** ist ein relativ einfaches Beispiel für das Schreiben von Apps, die auf Project Server 2013 und Project Online.</span><span class="sxs-lookup"><span data-stu-id="69ef7-504">The **QuickStatus** app is a relatively simple example of how to write apps that can be installed on Project Server 2013 and Project Online.</span></span> <span data-ttu-id="69ef7-505">Im [Abschnitt Testen der QuickStatus-App](#pj15_StatusingApp_Testing) werden mehrere Verbesserungen aufgeführt, die für eine bessere Benutzerfreundlichkeit vorgenommen werden können.</span><span class="sxs-lookup"><span data-stu-id="69ef7-505">The [Testing the QuickStatus app](#pj15_StatusingApp_Testing) section lists several improvements that can be made for better usability.</span></span> <span data-ttu-id="69ef7-506">Die **QuickStatus-App** verwendet JavaScript-Funktionen, um den Zuweisungsstatus für Project Web App zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="69ef7-506">The **QuickStatus** app uses JavaScript functions to update assignment status for Project Web App.</span></span> <span data-ttu-id="69ef7-507">Das Ändern des abgeschlossenen Zuordnungsprozentes ist jedoch keine empfohlene Projektverwaltungspraxis.</span><span class="sxs-lookup"><span data-stu-id="69ef7-507">But, changing the assignment percent complete is not a recommended project management practice.</span></span> <span data-ttu-id="69ef7-508">Ein weiterer Ansatz wäre das Aktualisieren des tatsächlichen Startdatums und der verbleibenden Dauer der zugewiesenen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="69ef7-508">Another approach would be to update the actual start date and remaining duration of assigned tasks.</span></span> <span data-ttu-id="69ef7-509">Eine Diskussion der Probleme finden Sie unter [Update Better](https://www.mpug.com/articles/update-better) im MPUG-Newsletter.</span><span class="sxs-lookup"><span data-stu-id="69ef7-509">For a discussion of the issues, see [Update Better](https://www.mpug.com/articles/update-better) in the MPUG newsletter.</span></span> 

<span data-ttu-id="69ef7-510"><a name="pj15_StatusingApp_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="69ef7-510"><a name="pj15_StatusingApp_AdditionalResources"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="69ef7-511">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69ef7-511">See also</span></span>

- [<span data-ttu-id="69ef7-512">Project Serverprogrammierungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="69ef7-512">Project Server programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="69ef7-513">SharePoint-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="69ef7-513">SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163230.aspx)
- [<span data-ttu-id="69ef7-514">Verwalten von Vorgangsaktualisierungen in Project Web App</span><span class="sxs-lookup"><span data-stu-id="69ef7-514">Managing task updates in Project Web App</span></span>](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [<span data-ttu-id="69ef7-515">Erstellen benutzerdefinierter Aktionen zur Bereitstellung mit SharePoint-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="69ef7-515">Create custom actions to deploy with SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163954.aspx)
    

