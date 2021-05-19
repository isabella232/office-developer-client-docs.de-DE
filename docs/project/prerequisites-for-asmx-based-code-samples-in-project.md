---
title: Voraussetzungen für ASMX-basierte Codebeispiele in Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- Codebeispiele, Projektserver,Project Server, Programmierung, PSI, Kompilieren von Codebeispielen,PSI, Programmierung
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Informationen zum Erstellen von Projekten in Visual Studio mithilfe der ASMX-basierten Codebeispiele, die in den Referenzthemen Project Server Interface (PSI) enthalten sind.
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357083"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a><span data-ttu-id="89b8a-104">Voraussetzungen für ASMX-basierte Codebeispiele in Project</span><span class="sxs-lookup"><span data-stu-id="89b8a-104">Prerequisites for ASMX-based code samples in Project</span></span>

<span data-ttu-id="89b8a-105">Informationen zum Erstellen von Projekten in Visual Studio mithilfe der ASMX-basierten Codebeispiele, die in den Referenzthemen Project Server Interface (PSI) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="89b8a-105">Learn information to help you create projects in Visual Studio by using the ASMX-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
  
<span data-ttu-id="89b8a-106">Viele der Codebeispiele in der klassenbibliotheks- und webdienstreferenz von [Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) wurden ursprünglich für das Office Project 2007 SDK erstellt und verwenden ein Standardformat für ASMX-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="89b8a-106">Many of the code samples included in the [Project Server 2013 class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Office Project 2007 SDK, and use a standard format for ASMX web services.</span></span> <span data-ttu-id="89b8a-107">Die Beispiele funktionieren weiterhin in Project Server 2013 und sind so konzipiert, dass sie in eine Konsolenanwendung kopiert und als vollständige Einheit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-107">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="89b8a-108">Ausnahmen werden im Beispiel erwähnt.</span><span class="sxs-lookup"><span data-stu-id="89b8a-108">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="89b8a-109">Neue PSI-Beispiele im Project 2013 SDK entsprechen einem Format, das Windows Communication Foundation (WCF)-Dienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="89b8a-109">New PSI samples in the Project 2013 SDK conform to a format that uses Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="89b8a-110">Die ASMX-basierten Beispiele können auch für die Verwendung von WCF-Diensten angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-110">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="89b8a-111">In diesem Artikel wird gezeigt, wie Sie die Beispiele mit ASMX-Webdiensten verwenden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-111">This article shows how to use the samples with ASMX web services.</span></span> <span data-ttu-id="89b8a-112">Informationen zur Verwendung der Beispiele mit WCF-Diensten finden Sie unter [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="89b8a-112">For information about using the samples with WCF services, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="89b8a-113">Die ASMX-Webdienstschnittstelle der PSI ist in Project Server 2013 zwar veraltet, wird aber weiterhin unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89b8a-113">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but is still supported.</span></span> <span data-ttu-id="89b8a-114">Wenn das clientseitige Objektmodell (CSOM) die von Ihrer Anwendung benötigten Methoden enthält, sollten neue Anwendungen mit dem CSOM entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-114">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="89b8a-115">Mit dem CSOM können Anwendungen mit Project Online oder einer lokalen Installation von Project Server 2013 arbeiten.</span><span class="sxs-lookup"><span data-stu-id="89b8a-115">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="89b8a-116">Wenn Ihre Anwendung andernfalls die PSI verwendet, sollte sie die WCF-Schnittstelle verwenden, die Technologie, die wir für die Netzwerkkommunikation empfehlen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-116">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="89b8a-117">Anwendungen, die die ASMX-Schnittstelle oder die WCF-Schnittstelle verwenden, können nur für lokale Installationen von Project Server 2013 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-117">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="89b8a-118">Weitere Informationen zum CSOM finden Sie [unter Project Server 2013](project-server-2013-architecture.md) architecture and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="89b8a-118">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="89b8a-119">Bevor Sie die Codebeispiele ausführen, müssen Sie die Entwicklungsumgebung einrichten, die Anwendung konfigurieren und generische Konstantenwerte entsprechend Ihrer Umgebung ändern.</span><span class="sxs-lookup"><span data-stu-id="89b8a-119">Before running the code samples, you must set up the development environment, configure the application, and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="89b8a-120">Einrichten der Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="89b8a-120">Setting up the development environment</span></span>
<span data-ttu-id="89b8a-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span></span>

1. <span data-ttu-id="89b8a-122">**Richten Sie einen Test Project Serversystem ein.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-122">**Set up a test Project Server system**.</span></span>
    
   <span data-ttu-id="89b8a-123">Verwenden Sie ein Project Serversystem, wenn Sie entwickeln oder testen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-123">Use a test Project Server system whenever you are developing or testing.</span></span> <span data-ttu-id="89b8a-124">Auch wenn Ihr Code einwandfrei funktioniert, können Abhängigkeiten zwischen Projekten, Berichte oder andere Umgebungsfaktoren unbeabsichtigte Folgen haben.</span><span class="sxs-lookup"><span data-stu-id="89b8a-124">Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="89b8a-125">Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server sind, und überprüfen Sie, ob Sie über ausreichende Berechtigungen für die von Ihrer Anwendung verwendeten PSI-Aufrufe verfügen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-125">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="89b8a-126">Das Referenzthema für jede PSI-Methode enthält eine Project Server Permissions-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="89b8a-126">The reference topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="89b8a-127">Beispielsweise wird [Project. Die QueueCreateProject-Methode](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) erfordert die globale **NewProject-Berechtigung** und **die SaveProjectTemplate-Berechtigung.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-127">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
   <span data-ttu-id="89b8a-128">In einigen Fällen müssen Sie möglicherweise remote debuggen auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="89b8a-128">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="89b8a-129">Möglicherweise müssen Sie auch einen Ereignishandler einrichten, indem Sie auf jedem Project Server-Computer in der SharePoint-Farm eine Ereignishandler assembly installieren und dann den Ereignishandler für die Project Web App-Instanz mithilfe der Seite Project Server Einstellungen in der Allgemeinen Anwendung Einstellungen der SharePoint-Zentraladministration konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="89b8a-129">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="89b8a-130">**Richten Sie einen Entwicklungscomputer ein.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-130">**Set up a development computer.**</span></span>
    
   <span data-ttu-id="89b8a-131">In der Regel greifen Sie über ein Netzwerk auf die PSI zu.</span><span class="sxs-lookup"><span data-stu-id="89b8a-131">You usually access the PSI through a network.</span></span> <span data-ttu-id="89b8a-132">Die Codebeispiele sind so konzipiert, dass sie auf einem Client ausgeführt werden, der vom Server getrennt ist, sofern nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="89b8a-132">The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
   1. <span data-ttu-id="89b8a-133">**Installieren Sie die richtige Version Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-133">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="89b8a-134">Sofern nicht erwähnt, werden die Codebeispiele in Visual C#.</span><span class="sxs-lookup"><span data-stu-id="89b8a-134">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="89b8a-135">Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-135">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="89b8a-136">Stellen Sie sicher, dass Das neueste Service Pack installiert ist.</span><span class="sxs-lookup"><span data-stu-id="89b8a-136">Ensure that you have the most recent service pack installed.</span></span> 
        
   2. <span data-ttu-id="89b8a-137">**Kopieren Project Server-DLLs auf den Entwicklungscomputer.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-137">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="89b8a-138">Kopieren Sie die folgenden Assemblys `[Program Files]\Microsoft Office Servers\15.0\Bin` aus Project Servercomputer auf den Entwicklungscomputer:</span><span class="sxs-lookup"><span data-stu-id="89b8a-138">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
        
      - <span data-ttu-id="89b8a-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="89b8a-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
      - <span data-ttu-id="89b8a-140">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="89b8a-140">Microsoft.Office.Project.Server.Library.dll</span></span>
        
   3. <span data-ttu-id="89b8a-141">Informationen zum Kompilieren und Verwenden der ProjectServerServices.dll-Proxy-Assembly für die ASMX-Webdienste in der PSI finden Sie unter [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="89b8a-141">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the ASMX web services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
3. <span data-ttu-id="89b8a-142">**Installieren Sie die IntelliSense Dateien.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-142">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="89b8a-143">Um IntelliSense Beschreibungen für Klassen und Mitglieder in Project Serverassemblys zu verwenden, kopieren Sie die aktualisierten IntelliSense-XML-Dateien aus dem Project 2013-SDK-Download in das Verzeichnis, in dem sich die Project Server-Assemblys befinden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-143">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="89b8a-144">Kopieren Sie beispielsweise die Microsoft.Office.Project.Server.Library.xml in das Verzeichnis, in dem Ihre Anwendung einen Verweis auf die Assembly Microsoft.Office.Project.Server.Library.dll wird.</span><span class="sxs-lookup"><span data-stu-id="89b8a-144">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="89b8a-145">IntelliSense Beschreibungen für die PSI-Webdienste erfordern, dass Sie eine PSI-Proxyassembly mithilfe des Skripts CompileASMXProxyAssembly.cmd im Unterverzeichnis im `Documentation\IntelliSense\WSDL` Project 2013 SDK-Download erstellen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-145">IntelliSense descriptions for the PSI web services require that you create a PSI proxy assembly by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="89b8a-146">Das Skript erstellt die ASMX-basierte ProjectServerServices.dll Proxy-Assembly.</span><span class="sxs-lookup"><span data-stu-id="89b8a-146">The script creates the ASMX-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="89b8a-147">Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im SDK-Download.</span><span class="sxs-lookup"><span data-stu-id="89b8a-147">For more information, see the [ReadMe_IntelliSense] file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a><span data-ttu-id="89b8a-148">Erstellen der Anwendung und Hinzufügen einer Webdienstreferenz</span><span class="sxs-lookup"><span data-stu-id="89b8a-148">Creating the application and adding a web service reference</span></span>
<span data-ttu-id="89b8a-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span></span>

1. <span data-ttu-id="89b8a-150">**Erstellen einer Konsolenanwendung**.</span><span class="sxs-lookup"><span data-stu-id="89b8a-150">**Create a console application**.</span></span>
    
   <span data-ttu-id="89b8a-151">Wenn Sie eine Konsolenanwendung erstellen, wählen Sie in der Dropdownliste des Dialogfelds Neue **Project** die Option **.NET Framework 4 aus.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-151">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**.</span></span> <span data-ttu-id="89b8a-152">Sie können den PSI-Beispielcode in die neue Anwendung kopieren.</span><span class="sxs-lookup"><span data-stu-id="89b8a-152">You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="89b8a-153">**Fügen Sie den für ASMX erforderlichen Verweis hinzu.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-153">**Add the reference required for ASMX.**</span></span>
    
   <span data-ttu-id="89b8a-154">Fügen Sie im Projektmappen-Explorer einen Verweis auf **System.Web.Services** hinzu (siehe Abbildung 1).</span><span class="sxs-lookup"><span data-stu-id="89b8a-154">In Solution Explorer, add a reference to **System.Web.Services** (see Figure 1).</span></span> 
    
   <span data-ttu-id="89b8a-155">**Abbildung 1. Hinzufügen eines Verweises in Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="89b8a-155">**Figure 1. Adding a reference in Visual Studio**</span></span>

   <span data-ttu-id="89b8a-156">![Hinzufügen eines Verweises in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Hinzufügen eines Verweises in Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="89b8a-156">![Adding a reference in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Adding a reference in Visual Studio")</span></span>
  
3. <span data-ttu-id="89b8a-157">**Kopieren Sie den Code**.</span><span class="sxs-lookup"><span data-stu-id="89b8a-157">**Copy the code**.</span></span>
    
   <span data-ttu-id="89b8a-158">Kopieren Sie das vollständige Codebeispiel in die Datei Program.cs der Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="89b8a-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="89b8a-159">**Legen Sie den Namespace für die Beispielanwendung .**</span><span class="sxs-lookup"><span data-stu-id="89b8a-159">**Set the namespace for the sample application**.</span></span>
    
   <span data-ttu-id="89b8a-160">Sie können entweder den oben im Beispiel aufgeführten Namespace in den Standardnamespace der Anwendung ändern oder den Standardanwendungsnamespace so ändern, dass er mit dem Beispiel übereinstimmen kann.</span><span class="sxs-lookup"><span data-stu-id="89b8a-160">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample.</span></span> <span data-ttu-id="89b8a-161">Sie können den Standardanwendungsnamespace ändern, indem Sie die Anwendungseigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="89b8a-161">You can change the default application namespace by changing the application properties.</span></span>
    
   <span data-ttu-id="89b8a-162">Das Codebeispiel für [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) verfügt beispielsweise über den Namespace **Microsoft.SDK.Project. Samples.RenameProject**.</span><span class="sxs-lookup"><span data-stu-id="89b8a-162">For example, the code sample for [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) has the namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span></span> <span data-ttu-id="89b8a-163">Wenn der Name des Visual Studio-Projekts **RenameProject** ist, kopieren Sie den Namespace aus der  Datei Program.cs, und öffnen Sie dann den Projekteigenschaftenbereich **(wählen** Sie im Menü Project **RenameProject Properties** aus).</span><span class="sxs-lookup"><span data-stu-id="89b8a-163">If the name of the Visual Studio project is **RenameProject**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **RenameProject Properties**).</span></span> <span data-ttu-id="89b8a-164">Kopieren Sie **auf** der Registerkarte Anwendung den Namespace in das Textfeld **Standardnamespace.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="89b8a-165">**Legen Sie die Webverweise .**</span><span class="sxs-lookup"><span data-stu-id="89b8a-165">**Set the web references**.</span></span>
    
   <span data-ttu-id="89b8a-166">Die meisten Beispiele erfordern einen Verweis auf mindestens einen der PSI-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="89b8a-166">Most examples require a reference to one or more of the PSI web services.</span></span> <span data-ttu-id="89b8a-167">Diese werden im Beispiel selbst oder in Kommentaren vor dem Beispiel aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="89b8a-167">These are listed in the sample itself or in comments that precede the sample.</span></span> <span data-ttu-id="89b8a-168">Um den richtigen Namespace der Webverweise zu erhalten, stellen Sie sicher, dass Sie zuerst den Standardanwendungsnamespace festlegen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-168">To get the correct namespace of the web references, ensure that you first set the default application namespace.</span></span>
    
   <span data-ttu-id="89b8a-169">Es gibt drei Möglichkeiten, eine ASMX-Webdienstreferenz für die PSI hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="89b8a-169">There are three ways to add an ASMX web service reference for the PSI:</span></span>
    
   - <span data-ttu-id="89b8a-170">Erstellen Sie eine PSI-Proxy assembly namens ProjectServerServices.dll, und legen Sie dann einen Verweis auf die Assembly.</span><span class="sxs-lookup"><span data-stu-id="89b8a-170">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly.</span></span> <span data-ttu-id="89b8a-171">Um eine IntelliSense zu erhalten, wird empfohlen, einen PSI-Verweis hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-171">To get IntelliSense, this is the recommended way to add a PSI reference.</span></span> <span data-ttu-id="89b8a-172">Weitere Informationen finden Sie unter Using [a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="89b8a-172">See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
   - <span data-ttu-id="89b8a-173">Fügen Sie eine Proxydatei aus der wsdl.exe der Visual Studio hinzu.</span><span class="sxs-lookup"><span data-stu-id="89b8a-173">Add a proxy file from the wsdl.exe output to the Visual Studio solution.</span></span> <span data-ttu-id="89b8a-174">Weitere [Informationen finden Sie unter Hinzufügen einer PSI-Proxydatei](#pj15_PrerequisitesASMX_AddingProxyFile).</span><span class="sxs-lookup"><span data-stu-id="89b8a-174">See [Adding a PSI proxy file](#pj15_PrerequisitesASMX_AddingProxyFile).</span></span>
    
   - <span data-ttu-id="89b8a-175">Fügen Sie einen Webdienstverweis mithilfe von Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="89b8a-175">Add a web service reference by using Visual Studio.</span></span> <span data-ttu-id="89b8a-176">Weitere [Informationen finden Sie unter Hinzufügen einer Webdienstreferenz](#pj15_PrerequisitesASMX_AddingServiceReference).</span><span class="sxs-lookup"><span data-stu-id="89b8a-176">See [Adding a web service reference](#pj15_PrerequisitesASMX_AddingServiceReference).</span></span>

<span data-ttu-id="89b8a-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span></span>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="89b8a-178">Verwenden einer PSI-Proxy-Assembly und IntelliSense Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="89b8a-178">Using a PSI proxy assembly and IntelliSense descriptions</span></span>

<span data-ttu-id="89b8a-179">Sie können die ProjectServerServices.dll-Proxyassembly für alle ASMX-basierten Webdienste in der PSI erstellen und verwenden, indem Sie das Skript CompileASMXProxyAssembly.cmd im Ordner des `Documentation\IntelliSense\WSDL` Project 2013 SDK-Downloads verwenden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-179">You can build and use the ProjectServerServices.dll proxy assembly for all ASMX-based web services in the PSI, by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` folder of the Project 2013 SDK download.</span></span> <span data-ttu-id="89b8a-180">Einen Link zum Download finden Sie unter [Project 2013 Developer Documentation](project-2013-developer-documentation.md).</span><span class="sxs-lookup"><span data-stu-id="89b8a-180">For a link to the download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="89b8a-181">Wenn Sie die Proxyquellendateien aus der Source.zip-Datei extrahieren, sind die Dateien im Ordner ab dem Veröffentlichungsdatum des Project `Documentation\IntelliSense\WSDL\Source` 2013 SDK-Downloads aktuell.</span><span class="sxs-lookup"><span data-stu-id="89b8a-181">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WSDL\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="89b8a-182">Führen Sie zum Generieren aktualisierter PSI-Proxyquellendateien das Skript GenASMXProxyAssembly.cmd auf dem Project Server aus.</span><span class="sxs-lookup"><span data-stu-id="89b8a-182">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="89b8a-183">Die Skripts im  `Documentation\IntelliSense\WCF` Ordner funktionieren nicht für ASMX-basierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-183">The scripts in the  `Documentation\IntelliSense\WCF` folder do not work for ASMX-based applications.</span></span> <span data-ttu-id="89b8a-184">Das GenWCFProxyAssembly.cmd-Skript ruft SvcUtil.exe auf, das Quellcodedateien für die WCF-Dienste generiert.</span><span class="sxs-lookup"><span data-stu-id="89b8a-184">The GenWCFProxyAssembly.cmd script calls SvcUtil.exe, which generates source code files for the WCF services.</span></span> <span data-ttu-id="89b8a-185">Die WCF-Proxydateien enthalten unterschiedliche Attribute, die Kanalschnittstelle und eine Clientklasse für jeden PSI-Dienst.</span><span class="sxs-lookup"><span data-stu-id="89b8a-185">The WCF proxy files include different attributes, the channel interface, and a client class for each PSI service.</span></span> <span data-ttu-id="89b8a-186">Der WCF-basierte Ressourcendienst umfasst beispielsweise die **ResourceChannel-Schnittstelle,** die **Resource-Schnittstelle** und die **ResourceClient-Klasse.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-186">For example, the WCF-based Resource service includes the **ResourceChannel** interface, the **Resource** interface, and the **ResourceClient** class.</span></span> <span data-ttu-id="89b8a-187">Das ASMX-basierte Ressourcenweb enthält die **Resource-Klasse** mit einigen verschiedenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89b8a-187">The ASMX-based Resource web includes the **Resource** class with some different properties.</span></span> 
  
<span data-ttu-id="89b8a-188">Im Folgenden sehen Sie das GenASMXProxyAssembly.cmd-Skript, das WSDL-Ausgabedateien für die PSI-Webdienste generiert und anschließend die Assembly kompiliert.</span><span class="sxs-lookup"><span data-stu-id="89b8a-188">Following is the GenASMXProxyAssembly.cmd script that generates WSDL output files for the PSI web services, and then compiles the assembly.</span></span>
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=https://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

<span data-ttu-id="89b8a-189">Das Skript verwendet die ClassList_asmx.txt-Datei, die die Liste der Webdienste enthält, die für Drittanbieterentwickler verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="89b8a-189">The script uses the ClassList_asmx.txt file, which contains the list of web services that are available for third-party developers.</span></span>
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

<span data-ttu-id="89b8a-190">Die Skripts erstellen eine Assembly namens ProjectServerServices.dll.</span><span class="sxs-lookup"><span data-stu-id="89b8a-190">The scripts create an assembly named ProjectServerServices.dll.</span></span> <span data-ttu-id="89b8a-191">Vermeiden Sie es mit ProjectServerServices.dll für die WCF-basierte Assembly zu verwechseln.</span><span class="sxs-lookup"><span data-stu-id="89b8a-191">Avoid confusing it with ProjectServerServices.dll for the WCF-based assembly.</span></span> <span data-ttu-id="89b8a-192">Die Assemblynamen sind identisch, um die Verwendung einer assembly mit der ProjectServerServices.xml IntelliSense aktivieren.</span><span class="sxs-lookup"><span data-stu-id="89b8a-192">The assembly names are the same, to enable using either assembly with the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="89b8a-193">Der von den Skripts für die ASMX-Webdienste und die WCF-Dienste erstellte beliebige Namespace ist identisch, sodass die ProjectServerServices.xml IntelliSense-Datei mit beiden Assemblys funktioniert.</span><span class="sxs-lookup"><span data-stu-id="89b8a-193">The arbitrary namespace created by the scripts for both the ASMX web services and the WCF services is the same, so that the ProjectServerServices.xml IntelliSense file works with either assembly.</span></span> <span data-ttu-id="89b8a-194">Beispielsweise ist der Namespace des Ressourcendiensts in der WCF-basierten Proxy-Assembly und in der ASMX-basierten Proxy-Assembly **SvcResource**.</span><span class="sxs-lookup"><span data-stu-id="89b8a-194">For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**.</span></span> <span data-ttu-id="89b8a-195">Sie können die Namespacenamen natürlich ändern, wenn Sie sicherstellen, dass sie in der Proxy-Assembly und in der ProjectServerServices.xml IntelliSense sind.</span><span class="sxs-lookup"><span data-stu-id="89b8a-195">You can, of course, change the namespace names—if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="89b8a-196">Wenn in einem Codebeispiel ein anderer Name für einen PSI-Webdienstnamespace verwendet wird, z. B. **ProjectWebSvc** IntelliSense , müssen Sie das Beispiel so ändern, dass **SvcProject** verwendet wird, damit der Namespace der Proxy assembly entspricht.</span><span class="sxs-lookup"><span data-stu-id="89b8a-196">If a code sample uses a different name for a PSI web service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="89b8a-197">Ein Vorteil bei der Verwendung der ASMX-basierten Proxy-Assembly ist, dass sie alle #A0 enthält. Sie müssen nicht mehrere Webverweise erstellen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-197">An advantage to using the ASMX-based proxy assembly is that it includes all PSI web service namespaces; you do not have to create multiple web references.</span></span> <span data-ttu-id="89b8a-198">Ein weiterer Vorteil: Wenn Sie die ProjectServerServices.xml-Datei demselben Verzeichnis hinzufügen, in dem Sie einen Verweis auf die ProjectServerServices.dll-Proxy assembly festlegen, können Sie IntelliSense Beschreibungen für die PSI-Klassen und -Member erhalten.</span><span class="sxs-lookup"><span data-stu-id="89b8a-198">Another advantage is that, if you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="89b8a-199">Abbildung 2 zeigt den IntelliSense text für die **Project. QueueCreateProject-Methode.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-199">Figure 2 shows the IntelliSense text for the **Project.QueueCreateProject** method.</span></span> <span data-ttu-id="89b8a-200">Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im ordner IntelliSense des Project 2013 SDK-Downloads.</span><span class="sxs-lookup"><span data-stu-id="89b8a-200">For more information, see the [ReadMe_IntelliSense] file in the IntelliSense folder of the Project 2013 SDK download.</span></span> 
  
<span data-ttu-id="89b8a-201">**Abbildung 2. Verwenden IntelliSense für eine Methode im Project Webdienst**</span><span class="sxs-lookup"><span data-stu-id="89b8a-201">**Figure 2. Using IntelliSense for a method in the Project web service**</span></span>

<span data-ttu-id="89b8a-202">![Verwenden von Intellisense für eine Methode in einem PSI-Dienst]Verwenden von(media/pj15_PrerequisitesASMX_Intellisense.gif "Intellisense für eine Methode in einem PSI-Dienst")</span><span class="sxs-lookup"><span data-stu-id="89b8a-202">![Using Intellisense for a method in a PSI service](media/pj15_PrerequisitesASMX_Intellisense.gif "Using Intellisense for a method in a PSI service")</span></span>
  
<span data-ttu-id="89b8a-203">Nachteile bei der Verwendung der Proxy assembly sind, dass die Lösung größer ist und Sie die Proxy assembly mit der Lösung verteilen und installieren müssen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-203">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution.</span></span> <span data-ttu-id="89b8a-204">Sie müssen auch die gleichen Namespaces verwenden, die sich in der Proxy assembly und IntelliSense-Dateien befinden, es sei denn, Sie ändern das Skript und die ProjectServerServices.xml IntelliSense-Datei, um unterschiedliche Namespaces zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-204">You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script and ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="89b8a-205">Hinzufügen einer PSI-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="89b8a-205">Adding a PSI proxy file</span></span>
<span data-ttu-id="89b8a-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span></span>

<span data-ttu-id="89b8a-207">Der Project 2013 SDK-Download enthält die Quelldateien, die durch den Befehl Wsdl.exe für die Proxy assembly generiert werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-207">The Project 2013 SDK download includes the source files generated by the Wsdl.exe command for the proxy assembly.</span></span> <span data-ttu-id="89b8a-208">Die Quelldateien befinden sich Source.zip im  `Documentation\IntelliSense\ASMX` Unterverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="89b8a-208">The source files are in Source.zip in the  `Documentation\IntelliSense\ASMX` subdirectory.</span></span> <span data-ttu-id="89b8a-209">Anstatt einen Verweis auf die Proxy assembly zu setzen, können Sie eine oder mehrere Quelldateien zu einer Visual Studio hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-209">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="89b8a-210">Fügen Sie beispielsweise nach dem Ausführen des Skripts GenASMXProxyAssembly.cmd das wsdl hinzu. Project.cs-Datei in die Lösung.</span><span class="sxs-lookup"><span data-stu-id="89b8a-210">For example, after running the GenASMXProxyAssembly.cmd script, add the wsdl.Project.cs file to the solution.</span></span> <span data-ttu-id="89b8a-211">Anstatt das Skript auszuführen, können Sie die folgenden Befehle ausführen, um eine einzelne Quelldatei zu generieren, z. B.:</span><span class="sxs-lookup"><span data-stu-id="89b8a-211">Instead of running the script, you can run the following commands to generate a single source file, for example:</span></span> 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

<span data-ttu-id="89b8a-212">Verwenden Sie den **folgenden Code, um** ein Project als Klassenvariable namens **Project** zu definieren.</span><span class="sxs-lookup"><span data-stu-id="89b8a-212">To define a **Project** object as a class variable named **project**, use the following code.</span></span> <span data-ttu-id="89b8a-213">Die **AddContextInfo-Methode** fügt dem  Projektobjekt die Kontextinformationen für die Windows und formularbasierte Authentifizierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="89b8a-213">The **AddContextInfo** method adds the context information to the **project** object for Windows authentication and Forms-based authentication.</span></span> 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "https://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> <span data-ttu-id="89b8a-214">Unabhängig davon, ob Sie eine PSI-Proxy-Assembly verwenden oder eine Proxydatei für einen Project-Dienstverweis namens **SvcProject** hinzufügen, würden Sie denselben Code verwenden, um ein **Projektobjekt zu** erstellen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-214">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcProject**, you would use the same code to create a **project** object.</span></span> 
  
### <a name="adding-a-web-service-reference"></a><span data-ttu-id="89b8a-215">Hinzufügen einer Webdienstreferenz</span><span class="sxs-lookup"><span data-stu-id="89b8a-215">Adding a web service reference</span></span>
<span data-ttu-id="89b8a-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span></span>

<span data-ttu-id="89b8a-217">Wenn Sie die ASMX-basierte Proxy-Assembly nicht verwenden oder keine WSDL-Ausgabedatei hinzufügen, können Sie einen oder mehrere einzelne Webverweise festlegen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-217">If you do not use the ASMX-based proxy assembly or add a WSDL output file, you can set one or more individual web references.</span></span> <span data-ttu-id="89b8a-218">Die folgenden Schritte zeigen, wie Sie einen Webverweis mithilfe von Visual Studio 2012 festlegen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-218">The following steps show how to set a web reference by using Visual Studio 2012.</span></span>
  
1. <span data-ttu-id="89b8a-219">Klicken **Sie im** Projektmappen-Explorer mit der rechten Maustaste auf den Ordner **Verweise,** und wählen Sie **dann Dienstreferenz hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-219">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
2. <span data-ttu-id="89b8a-220">Wählen Sie **im Dialogfeld Dienstreferenz** hinzufügen die Option **Erweitert aus.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-220">In the **Add Service Reference** dialog box, choose **Advanced**.</span></span>
    
3. <span data-ttu-id="89b8a-221">Wählen Sie **im Einstellungen** Dienstreferenz die Option **Webreferenz hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-221">In the **Service Reference Settings** dialog box, choose **Add Web Reference**.</span></span>
    
4. <span data-ttu-id="89b8a-222">Geben Sie **im Textfeld URL** `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` ein, und drücken Sie dann die **EINGABETASTE,** oder wählen Sie das **Symbol Los** aus.</span><span class="sxs-lookup"><span data-stu-id="89b8a-222">In the **URL** text box, type `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, and then press **Enter** or choose the **Go** icon.</span></span> <span data-ttu-id="89b8a-223">Wenn Secure Sockets Layer (SSL) installiert ist, sollten Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls verwenden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-223">If you have Secure Sockets Layer (SSL) installed, you should use the HTTPS protocol instead of the HTTP protocol.</span></span> 

   <span data-ttu-id="89b8a-224">Verwenden Sie beispielsweise die folgende URL für den Project auf der Website `https://MyServer/pwa` für Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span><span class="sxs-lookup"><span data-stu-id="89b8a-224">For example, use the following URL for the Project service on the  `https://MyServer/pwa` site for Project Web App: `https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span></span>
    
   <span data-ttu-id="89b8a-225">Öffnen Sie auch Ihren Webbrowser, und navigieren Sie zu `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` .</span><span class="sxs-lookup"><span data-stu-id="89b8a-225">Or, open your web browser, and navigate to `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span></span> <span data-ttu-id="89b8a-226">Speichern Sie die Datei in einem lokalen Verzeichnis, z. B. `C:\Project\WebServices\ServiceName.wsdl` .</span><span class="sxs-lookup"><span data-stu-id="89b8a-226">Save the file to a local directory, such as `C:\Project\WebServices\ServiceName.wsdl`.</span></span> <span data-ttu-id="89b8a-227">Geben Sie **im Dialogfeld Webreferenz** hinzufügen für **URL** das Dateiprotokoll und den Pfad zur Datei ein.</span><span class="sxs-lookup"><span data-stu-id="89b8a-227">In the **Add Web Reference** dialog box, for **URL**, type the file protocol and the path to the file.</span></span> <span data-ttu-id="89b8a-228">Geben Sie z. B. `file://C:\Project\WebServices\Project.wsdl` ein.</span><span class="sxs-lookup"><span data-stu-id="89b8a-228">For example, type `file://C:\Project\WebServices\Project.wsdl`.</span></span> 
    
5. <span data-ttu-id="89b8a-229">Nachdem der Verweis aufgelöst wurde, geben Sie den Verweisnamen in das Textfeld **Webverweisname** ein.</span><span class="sxs-lookup"><span data-stu-id="89b8a-229">After the reference resolves, type the reference name in the **Web reference name** text box.</span></span> <span data-ttu-id="89b8a-230">Codebeispiele in der Project 2013-Entwicklerdokumentation verwenden den beliebigen Standardreferenznamen **Svc _ServiceName_**.</span><span class="sxs-lookup"><span data-stu-id="89b8a-230">Code examples in the Project 2013 developer documentation use the arbitrary standard reference name **Svc _ServiceName_**.</span></span> <span data-ttu-id="89b8a-231">Beispielsweise heißt Project Webdienst **SvcProject** (siehe Abbildung 3).</span><span class="sxs-lookup"><span data-stu-id="89b8a-231">For example, the Project web service is named **SvcProject** (see Figure 3).</span></span> 
    
   <span data-ttu-id="89b8a-232">**Abbildung 3. Hinzufügen einer ASMX-Webdienstreferenz**</span><span class="sxs-lookup"><span data-stu-id="89b8a-232">**Figure 3. Adding an ASMX web service reference**</span></span>

   <span data-ttu-id="89b8a-233">![Hinzufügen einer ASMX-Webdienstreferenz](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Hinzufügen einer ASMX-Webdienstreferenz")</span><span class="sxs-lookup"><span data-stu-id="89b8a-233">![Adding an ASMX web service reference](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adding an ASMX web service reference")</span></span>
  
<span data-ttu-id="89b8a-234">Verwenden Sie für Anwendungskomponenten, die auf dem computer Project Server ausgeführt werden müssen, den Identitätswechsel verwenden oder über erhöhte Berechtigungen verfügen, einen WCF-Dienstverweis anstelle eines ASMX-Webverweises.</span><span class="sxs-lookup"><span data-stu-id="89b8a-234">For application components that must run on the Project Server computer, use impersonation, or have elevated permissions, use a WCF service reference instead of an ASMX web reference.</span></span> <span data-ttu-id="89b8a-235">Weitere Informationen finden Sie unter [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="89b8a-235">For more information, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="setting-other-references"></a><span data-ttu-id="89b8a-236">Festlegen anderer Verweise</span><span class="sxs-lookup"><span data-stu-id="89b8a-236">Setting other references</span></span>
<span data-ttu-id="89b8a-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span></span>

<span data-ttu-id="89b8a-238">Project Serveranwendungen verwenden häufig andere Dienste, z. B. SharePoint Server 2013-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="89b8a-238">Project Server applications often use other services, such as SharePoint Server 2013 web services.</span></span> <span data-ttu-id="89b8a-239">Wenn andere Dienste erforderlich sind, werden sie im Beispiel notiert.</span><span class="sxs-lookup"><span data-stu-id="89b8a-239">If other services are required, they are noted in the example.</span></span>
  
<span data-ttu-id="89b8a-240">Lokale Verweise für das Codebeispiel sind in **using-Anweisungen** am Anfang des Beispiels aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="89b8a-240">Local references for the code sample are listed in **using** statements at the top of the sample:</span></span> 
  
1. <span data-ttu-id="89b8a-241">Klicken **Sie im Projektmappen-Explorer** mit der rechten Maustaste auf den Ordner **Verweise,** und wählen Sie **dann Verweis hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-241">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="89b8a-242">Wählen **Sie Durchsuchen** aus, und navigieren Sie dann zu dem Speicherort, an dem Sie die zuvor kopierten Project Server-DLLs gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="89b8a-242">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously.</span></span> <span data-ttu-id="89b8a-243">Wählen Sie die benötigten DLLs aus, und wählen Sie dann **OK aus.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-243">Choose the DLLs you need, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="89b8a-244">Stellen Sie sicher, dass die Assemblyversionen auf Ihrem Entwicklungscomputer genau mit denen auf dem Zielcomputer Project übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-244">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="89b8a-245">Verwenden mehrerer Authentifizierungen</span><span class="sxs-lookup"><span data-stu-id="89b8a-245">Using multiple authentication</span></span>
<span data-ttu-id="89b8a-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span></span>

<span data-ttu-id="89b8a-247">Die Authentifizierung von lokalen Project Serverbenutzern, Windows Authentifizierung oder Formularauthentifizierung, erfolgt über die Anspruchsverarbeitung in SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="89b8a-247">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint Server 2013.</span></span> <span data-ttu-id="89b8a-248">Die mehrfache Authentifizierung bedeutet, dass die Webanwendung, für die Project Web App bereitgestellt wird, sowohl die Windows als auch die formularbasierte Authentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89b8a-248">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="89b8a-249">In diesem Fall tritt bei einem Aufruf eines ASMX-Webdiensts, der die Windows-Authentifizierung verwendet, ein Fehler auf, da der Anspruchsprozess nicht bestimmen kann, welcher Benutzertyp authentifiziert werden soll:</span><span class="sxs-lookup"><span data-stu-id="89b8a-249">If that is the case, a call to an ASMX web service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. . . .`

<span data-ttu-id="89b8a-250">Um das Problem für ASMX zu beheben, sollten alle Aufrufe von PSI-Methoden für eine abgeleitete Klasse verwendet werden, die für jeden PSI-Webdienst definiert ist.</span><span class="sxs-lookup"><span data-stu-id="89b8a-250">To fix the problem for ASMX, all calls to PSI methods should be to a derived class that is defined for each PSI web service.</span></span> <span data-ttu-id="89b8a-251">Die abgeleitete Klasse muss auch die **SvcLoginWindows.LoginWindows-Klasse** verwenden, um ein Cookie für die abgeleitete PSI-Dienstklasse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="89b8a-251">The derived class must also use the **SvcLoginWindows.LoginWindows** class to get a cookie for the derived PSI service class.</span></span> <span data-ttu-id="89b8a-252">Im folgenden Beispiel wird die **ProjectDerived-Klasse** von der **SvcProject.Project-Klasse** ab.</span><span class="sxs-lookup"><span data-stu-id="89b8a-252">In the following example, the **ProjectDerived** class derives from the **SvcProject.Project** class.</span></span> <span data-ttu-id="89b8a-253">Die abgeleitete Klasse fügt die **EnforceWindowsAuth-Eigenschaft** hinzu und überschreibt den Webanforderungsheader für jeden Aufruf einer Methode in der **Project** Klasse.</span><span class="sxs-lookup"><span data-stu-id="89b8a-253">The derived class adds the **EnforceWindowsAuth** property and overrides the web request header for every call to a method in the **Project** class.</span></span> <span data-ttu-id="89b8a-254">Wenn die **EnforceWindowsAuth-Eigenschaft** **true** ist, fügt die **GetWebRequest-Methode** einen Header hinzu, der die Formularauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="89b8a-254">If the **EnforceWindowsAuth** property is **true**, the **GetWebRequest** method adds a header that disables Forms authentication.</span></span> <span data-ttu-id="89b8a-255">Wenn **EnforceWindowsAuth** **auf false gesetzt ist,** kann die Formularauthentifizierung fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-255">If **EnforceWindowsAuth** is **false**, Forms authentication can proceed.</span></span>
  
<span data-ttu-id="89b8a-256">Um das folgende ASMXLogon_MultiAuth **zu** verwenden, erstellen Sie eine Konsolenanwendung, führen Sie die Schritte unter [Erstellen](#pj15_PrerequisitesASMX_Configure)der Anwendung und Hinzufügen eines Webdienstverweises aus, und fügen Sie dann das wsdl hinzu. LoginWindows.cs-Proxydatei und wsdl. Project.cs-Proxydatei.</span><span class="sxs-lookup"><span data-stu-id="89b8a-256">To use the following **ASMXLogon_MultiAuth** sample, create a console application, follow the steps in [Creating the application and adding a web service reference](#pj15_PrerequisitesASMX_Configure), and then add the wsdl.LoginWindows.cs proxy file and the wsdl.Project.cs proxy file.</span></span> <span data-ttu-id="89b8a-257">Die **Main-Methode** erstellt **die Projektinstanz** der **ProjectDerived-Klasse.**</span><span class="sxs-lookup"><span data-stu-id="89b8a-257">The **Main** method creates the **project** instance of the **ProjectDerived** class.</span></span> <span data-ttu-id="89b8a-258">Das Beispiel muss die abgeleitete **LoginWindowsDerived-Klasse** verwenden, um ein **CookieContainer-Objekt** für das Projekt **zu erhalten. CookieContainer-Eigenschaft,** die die Formularauthentifizierung von der Windows unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="89b8a-258">The sample must use the derived **LoginWindowsDerived** class to get a **CookieContainer** object for the **project.CookieContainer** property, which distinguishes Forms authentication from Windows authentication.</span></span> <span data-ttu-id="89b8a-259">Das **Projektobjekt** kann dann zum Aufrufen einer beliebigen Methode in der **SvcProject.Project** werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-259">The **project** object can then be used to make calls to any method in the **SvcProject.Project** class.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="89b8a-260">Der **LoginWindows-Dienst** ist nur für ASMX-Anwendungen in einer Umgebung mit mehreren Authentifizierungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="89b8a-260">The **LoginWindows** service is required only for ASMX applications in a multiple authentication environment.</span></span> <span data-ttu-id="89b8a-261">Im **ASMXLogon_MultiAuth** ruft die **GetLogonCookie-Methode** ein Cookie für das **loginWindows-Objekt** ab.</span><span class="sxs-lookup"><span data-stu-id="89b8a-261">In the **ASMXLogon_MultiAuth** sample, the **GetLogonCookie** method gets a cookie for the **loginWindows** object.</span></span> <span data-ttu-id="89b8a-262">Das **Projekt. Die CookieContainer-Eigenschaft** wird auf den **Wert loginWindows.CookieContainer** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89b8a-262">The **project.CookieContainer** property is set to the **loginWindows.CookieContainer** value.</span></span> 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "https://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

<span data-ttu-id="89b8a-263">Die Verwendung der abgeleiteten **LoginWindows-Klasse** und das Ausführen von PSI-Aufrufen mit einem Webanforderungsheader, der die Formularauthentifizierung deaktiviert, ist für Anwendungen erforderlich, die in einer Umgebung mit mehreren Authentifizierungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-263">Using the derived **LoginWindows** class, and making PSI calls with a web request header that disables Forms authentication, is required for applications that run in a multiple authentication environment.</span></span> <span data-ttu-id="89b8a-264">Wenn Project Server nur die Anspruchsauthentifizierung verwendet, ist es nicht erforderlich, eine Klasse zu leiten, die einen Webanforderungsheader hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="89b8a-264">If Project Server uses only claims authentication, it is not necessary to derive a class that adds a web request header.</span></span> <span data-ttu-id="89b8a-265">Das vorherige Beispiel wird in beiden Umgebungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89b8a-265">The previous example runs in both environments.</span></span> 
  
<span data-ttu-id="89b8a-266">Die Lösung für eine WCF-basierte Anwendung ist anders.</span><span class="sxs-lookup"><span data-stu-id="89b8a-266">The fix for a WCF-based application is different.</span></span> <span data-ttu-id="89b8a-267">Weitere Informationen finden  Sie im Abschnitt Verwenden mehrerer Authentifizierungen unter [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="89b8a-267">For more information, see the  *Using multiple authentication*  section in [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="changing-the-values-of-generic-constants"></a><span data-ttu-id="89b8a-268">Ändern der Werte generischer Konstanten</span><span class="sxs-lookup"><span data-stu-id="89b8a-268">Changing the values of generic constants</span></span>
<span data-ttu-id="89b8a-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span></span>

<span data-ttu-id="89b8a-270">Die meisten Beispiele enthalten eine oder mehrere Variablen, die Sie aktualisieren müssen, damit das Beispiel in Ihrer Umgebung ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="89b8a-270">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="89b8a-271">Wenn Sie SSL installiert haben, verwenden Sie im folgenden Beispiel das HTTPS-Protokoll anstelle des HTTP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="89b8a-271">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="89b8a-272">Ersetzen  _Sie ServerName_ durch den Namen des servers, den Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="89b8a-272">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="89b8a-273">Ersetzen _Sie ProjectServerName_ durch den virtuellen Verzeichnisnamen Ihrer Project Serverwebsite, z. B. PWA.</span><span class="sxs-lookup"><span data-stu-id="89b8a-273">Replace  _ProjectServerName_ with the virtual directory name of your Project Server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

<span data-ttu-id="89b8a-274">Alle anderen Variablen, die Sie ändern müssen, oder andere Voraussetzungen werden am Anfang des Codebeispiels notiert.</span><span class="sxs-lookup"><span data-stu-id="89b8a-274">Any other variables that you must change or other prerequisites are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="89b8a-275">Überprüfen der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="89b8a-275">Verifying the results</span></span>
<span data-ttu-id="89b8a-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span></span>

<span data-ttu-id="89b8a-277">Das Abrufen und Interpretieren von Ergebnissen aus einem Codebeispiel ist nicht immer einfach.</span><span class="sxs-lookup"><span data-stu-id="89b8a-277">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="89b8a-278">Wenn Sie beispielsweise ein Projekt erstellen, müssen Sie das Projekt veröffentlichen, bevor es auf der Seite Project Center in Project Web App angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="89b8a-278">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="89b8a-279">Sie können Codebeispielergebnisse auf verschiedene Weise überprüfen, z. B.:</span><span class="sxs-lookup"><span data-stu-id="89b8a-279">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="89b8a-280">Verwenden Sie Project Professional 2013-Client, um das Projekt auf dem Project Server-Computer zu öffnen und die elemente, die Sie möchten, anzeigen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-280">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="89b8a-281">Zeigen Sie veröffentlichte Projekte auf der Project Center-Seite von Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ) an.</span><span class="sxs-lookup"><span data-stu-id="89b8a-281">View published projects on the Project Center page of Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="89b8a-282">Anzeigen des Warteschlangenprotokolls in Project Web App.</span><span class="sxs-lookup"><span data-stu-id="89b8a-282">View the Queue log in Project Web App.</span></span> <span data-ttu-id="89b8a-283">Öffnen Sie die Seite Server Einstellungen (wählen Sie **das Symbol Einstellungen** in der  oberen rechten Ecke aus), und wählen Sie dann Meine Warteschlangenaufträge unter dem Abschnitt Persönliche **Einstellungen** aus ( `https://ServerName/ProjectServerName/MyJobs.aspx` ).</span><span class="sxs-lookup"><span data-stu-id="89b8a-283">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `https://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="89b8a-284">In der **Dropdownliste** Ansicht können Sie nach auftragsstatus sortieren.</span><span class="sxs-lookup"><span data-stu-id="89b8a-284">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="89b8a-285">Der Standardstatus ist **In Bearbeitung und Fehlgeschlagene Aufträge in der vergangenen Woche**.</span><span class="sxs-lookup"><span data-stu-id="89b8a-285">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="89b8a-286">Verwenden Sie die Seite Server Einstellungen in Project Web App ( ), um alle Warteschlangenaufträge zu verwalten und Unternehmensobjekte zu löschen oder `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-286">Use the Server Settings page in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="89b8a-287">Sie müssen über Administratorberechtigungen verfügen, um auf diese Links auf der Serverserverseite Einstellungen können.</span><span class="sxs-lookup"><span data-stu-id="89b8a-287">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="89b8a-288">Verwenden **Microsoft SQL Server Management Studio,** um eine Abfrage für eine Tabelle in der Datenbank Project ausführen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-288">Use **Microsoft SQL Server Management Studio** to run a query on a table in the Project database.</span></span> <span data-ttu-id="89b8a-289">Verwenden Sie beispielsweise die folgende Abfrage, um die 200 obersten Zeilen des Pubs auszuwählen. MSP_WORKFLOW_STAGE_PDPS, um Informationen zu den Projektdetailsetailseiten (PDPs) in Workflowphasen zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-289">For example, use the following query to select the top 200 rows of the pub.MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
   ```sql
    SELECT TOP 200 [STAGE_UID]
            ,[PDP_UID]
            ,[PDP_NAME]
            ,[PDP_POSITION]
            ,[PDP_ID]
            ,[PDP_STAGE_DESCRIPTION]
            ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
   ```

## <a name="cleaning-up"></a><span data-ttu-id="89b8a-290">Löschen</span><span class="sxs-lookup"><span data-stu-id="89b8a-290">Cleaning up</span></span>
<span data-ttu-id="89b8a-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span></span>

<span data-ttu-id="89b8a-292">Nachdem Sie einige Codebeispiele testiert haben, gibt es Enterprise-Objekte und -Einstellungen, die gelöscht oder zurückgesetzt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="89b8a-292">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="89b8a-293">Sie können die Seite Server Einstellungen in Project Web App verwenden, um Unternehmensdaten zu verwalten ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ).</span><span class="sxs-lookup"><span data-stu-id="89b8a-293">You can use the Server Settings page in Project Web App to manage enterprise data ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="89b8a-294">Über Links auf der Seite Server Einstellungen können Sie alte Elemente löschen, Eincheckprojekte erzwingen, die Auftragswarteschlange für alle Benutzer verwalten und andere administrative Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-294">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="89b8a-295">Im Folgenden finden Sie einige der Links auf der Seite Server Einstellungen, die Sie für typische Bereinigungsaktivitäten verwenden können, nachdem Sie Codebeispiele ausgeführt haben:</span><span class="sxs-lookup"><span data-stu-id="89b8a-295">Following are some of the links on the Server Settings page that you can use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="89b8a-296">**Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen**</span><span class="sxs-lookup"><span data-stu-id="89b8a-296">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="89b8a-297">**Verwalten von Warteschlangenaufträgen**</span><span class="sxs-lookup"><span data-stu-id="89b8a-297">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="89b8a-298">**Löschen Enterprise Objekten**</span><span class="sxs-lookup"><span data-stu-id="89b8a-298">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="89b8a-299">**Erzwingen des Eincheckens Enterprise Objekten**</span><span class="sxs-lookup"><span data-stu-id="89b8a-299">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="89b8a-300">**Enterprise-Projekttypen**</span><span class="sxs-lookup"><span data-stu-id="89b8a-300">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="89b8a-301">**Workflowphasen**</span><span class="sxs-lookup"><span data-stu-id="89b8a-301">**Workflow Phases**</span></span>
    
- <span data-ttu-id="89b8a-302">**Workflowstufen**</span><span class="sxs-lookup"><span data-stu-id="89b8a-302">**Workflow Stages**</span></span>
    
- <span data-ttu-id="89b8a-303">**Projektdetailseiten**</span><span class="sxs-lookup"><span data-stu-id="89b8a-303">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="89b8a-304">**Zeiträume in Zeitberichten**</span><span class="sxs-lookup"><span data-stu-id="89b8a-304">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="89b8a-305">**Einstellungen und Standardwerte in der Arbeitszeittabelle**</span><span class="sxs-lookup"><span data-stu-id="89b8a-305">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="89b8a-306">**Linienklassifikationen**</span><span class="sxs-lookup"><span data-stu-id="89b8a-306">**Line Classifications**</span></span>
    
<span data-ttu-id="89b8a-307">Zusätzliche Einstellungen werden von SharePoint Server 2013 für jede Project Web App-Instanz und nicht von einer bestimmten Project Web App Server-Einstellungen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="89b8a-307">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="89b8a-308">Wählen Sie in der SharePoint-Zentraladministrationsanwendung allgemeine Anwendung  **Einstellungen** aus, wählen Sie verwalten unter **Project Server Einstellungen** aus, und wählen Sie dann die Project Web App-Instanz in der Dropdownliste auf der Seite Server Einstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="89b8a-308">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="89b8a-309">Wählen Sie z. B. **Serverseitige Ereignishandler** aus, um Ereignishandler für die ausgewählte Project Web App-Instanz hinzuzufügen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="89b8a-309">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89b8a-310">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89b8a-310">See also</span></span>
<span data-ttu-id="89b8a-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="89b8a-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span></span>

- [<span data-ttu-id="89b8a-312">Voraussetzungen für WCF-basierte Codebeispiele in Project</span><span class="sxs-lookup"><span data-stu-id="89b8a-312">Prerequisites for WCF-based code samples in Project</span></span>](prerequisites-for-wcf-based-code-samples-in-project.md)
- [<span data-ttu-id="89b8a-313">Verwenden des Identitätswechsels mit WCF</span><span class="sxs-lookup"><span data-stu-id="89b8a-313">Use Impersonation with WCF</span></span>](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [<span data-ttu-id="89b8a-314">Übersicht über die Project PSI-Referenz</span><span class="sxs-lookup"><span data-stu-id="89b8a-314">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
- [<span data-ttu-id="89b8a-315">SharePoint Developer Center</span><span class="sxs-lookup"><span data-stu-id="89b8a-315">SharePoint Developer Center</span></span>](https://msdn.microsoft.com/sharepoint/default.aspx)
    

