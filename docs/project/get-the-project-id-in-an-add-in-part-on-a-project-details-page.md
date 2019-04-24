---
title: Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Add-in-Parts werden in iframe-Elementen gehostet, die vollständig von der Hostingseite isoliert sind. Wenn Sie Informationen über das aktuelle Projekt aus einem Add-in-Webpart auf der Projektdetailseite (PDP) abrufen möchten, können Sie die Window. PostMessage-Methode, einen Ereignislistener und einen Ereignishandler verwenden, der die Projekt-ID aus der Nachricht analysiert.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322596"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="c7ce3-104">Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite</span><span class="sxs-lookup"><span data-stu-id="c7ce3-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="c7ce3-105">Add-in-Parts werden in **iframe** -Elementen gehostet, die vollständig von der Hostingseite isoliert sind.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="c7ce3-106">Wenn Sie Informationen über das aktuelle Projekt aus einem Add-in-Webpart auf der Projektdetailseite (PDP) abrufen möchten, können Sie die **Window. PostMessage** -Methode, einen Ereignislistener und einen Ereignishandler verwenden, der die Projekt-ID aus der Nachricht analysiert.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="c7ce3-107">VoraussetZungen für das Erstellen eines von SharePoint gehosteten Add-in-Parts, das die Projekt-ID abruft</span><span class="sxs-lookup"><span data-stu-id="c7ce3-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="c7ce3-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="c7ce3-108"></span></span>

<span data-ttu-id="c7ce3-109">Um das Codebeispiel in diesem Artikel verwenden zu können, benötigen Sie eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="c7ce3-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="c7ce3-110">SharePoint 2013 und Project Server 2013, konfiguriert für die Add-in-Isolierung.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="c7ce3-111">Wenn Sie Remote entwickeln, muss der Server querladen von Add-Ins unterstützen, oder Sie müssen das Add-in auf einer Entwickler Website installieren.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="c7ce3-112">SharePoint Online und Project Online</span><span class="sxs-lookup"><span data-stu-id="c7ce3-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="c7ce3-113">Visual Studio 2013, Visual Studio 2012 mit Office Developer Tools für Visual Studio 2013 oder Napa</span><span class="sxs-lookup"><span data-stu-id="c7ce3-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="c7ce3-114">Über ausreichende Berechtigungen für den angemeldeten Benutzer:</span><span class="sxs-lookup"><span data-stu-id="c7ce3-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="c7ce3-115">Lokale Administratorberechtigungen auf dem Entwicklungscomputer installiert.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="c7ce3-116">Lesezugriff auf mindestens ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="c7ce3-117">Berechtigung zum Bearbeiten von Seiten auf der Project Web App-Website.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="c7ce3-118">Sie müssen als eine andere Person als das Systemkonto angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="c7ce3-119">Das Systemkonto verfügt nicht über die Berechtigung zum Installieren eines Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="c7ce3-120">Weitere Informationen zu Add-Ins für Project finden Sie unter [vorausSetzungen für die Erstellung eines Add-Ins für Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) .</span><span class="sxs-lookup"><span data-stu-id="c7ce3-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="c7ce3-121">Unter [Einrichten einer lokalen Entwicklungsumgebung für SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) finden Sie Anleitungen zum lokalen Setup (einschließlich der Deaktivierung der Loopbacküberprüfung).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="c7ce3-122">Wenn Sie Remote entwickeln, finden Sie weitere Informationen unter [entwickeln von Apps für SharePoint auf einem Remote System](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="c7ce3-123">Erstellen des von SharePoint gehosteten Add-in-und Client-Webparts</span><span class="sxs-lookup"><span data-stu-id="c7ce3-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="c7ce3-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="c7ce3-124"></span></span>

1. <span data-ttu-id="c7ce3-125">Öffnen Sie Visual Studio, und wählen Sie **Datei** > **Neues** > **Projekt**aus.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="c7ce3-126">Wählen Sie im Dialogfeld **Neues Projekt** aus der Dropdownliste oben im Dialogfeld die Option **.NET Framework 4.5**.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="c7ce3-127">wählen sie In der liste **vorlagen** die option **Visual C#** > **Office/sharepoint** > **add-ins** > **add-in für sharepoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="c7ce3-128">Nennen Sie das Add-in-GetProjectIdAddinPart, und klicken Sie dann auf die Schaltfläche **OK** .</span><span class="sxs-lookup"><span data-stu-id="c7ce3-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="c7ce3-129">Geben Sie im Dialogfeld **Neues Add-in für SharePoint** die URL der PWA-Website ein, die Sie zum Debuggen verwenden möchten (Beispiel: _https://contoso.com/sites/pwasite/_).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="c7ce3-130">Wählen Sie die von **SharePoint gehostete** Option aus, um Ihr Add-in zu hosten, und klicken Sie dann auf die Schaltfläche **Fertig stellen** .</span><span class="sxs-lookup"><span data-stu-id="c7ce3-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="c7ce3-131">Öffnen Sie im Projektmappen- **Explorer**das Kontextmenü für das GetProjectIdAddinPart-Projekt, und wählen Sie dann**Neues Element** **Hinzufügen** > aus.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="c7ce3-132">Wählen Sie im Dialogfeld **Neues Element hinzufügen** die Option **Client Webpart (Host Web)** aus, benennen Sie das Webpart getprojecto, und klicken Sie dann auf die Schaltfläche **Hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="c7ce3-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="c7ce3-133">Wählen Sie im Dialogfeld **Client-Webpart erstellen** die Option **neuen Client-Webpart erstellen** aus, und klicken Sie dann auf die Schaltfläche **Fertig stellen** .</span><span class="sxs-lookup"><span data-stu-id="c7ce3-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="c7ce3-134">Abrufen der Projekt-ID im Add-in-Webpart</span><span class="sxs-lookup"><span data-stu-id="c7ce3-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="c7ce3-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="c7ce3-135"></span></span>

<span data-ttu-id="c7ce3-136">Der getProjectable-Add-in-Webpart definiert seinen benutzerdefinierten Code auf der Seite getProjected. aspx des Client-Webparts.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="c7ce3-137">Die Logik, die die Nachricht empfängt und verarbeitet, wird im **Head** -Element der Seite definiert, und die Page-Steuerelemente werden im **Body** -Element der Seite definiert.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="c7ce3-138">Öffnen Sie die Webpartseite getProjectable. aspx (im Ordner **pages** ).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="c7ce3-139">Ersetzen Sie im **Head** -Element der Seite den Code zwischen den **Script** -Tags durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
   ```js
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
                (function () {
                    var hostUrl = '';
                    var link = document.createElement('link');
                    link.setAttribute('rel', 'stylesheet');
                    if (document.URL.indexOf('?') != -1) {
                        var params = document.URL.split('?')[1].split('&');
                        for (var i = 0; i < params.length; i++) {
                            var p = decodeURIComponent(params[i]);
                            if (/^SPHostUrl=/i.test(p)) {
                                hostUrl = p.split('=')[1];
                                link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                                break;
                            }
                        }
                    }
                    if (hostUrl == '') {
                        link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
                    }
                    document.head.appendChild(link);
                })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
   ```

3. <span data-ttu-id="c7ce3-140">Fügen Sie den folgenden Code in das **Body** -Element der Seite ein.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="c7ce3-141">Der Code definiert ein Span-Steuerelement, das die Projekt-ID anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="c7ce3-142">Ändern Sie optional in der Datei Elements. XML den Namen, den Titel, die Beschreibung und die Standardgröße des Add-in-Parts.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="c7ce3-143">In diesem Beispiel werden die Standardwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="c7ce3-144">Um das Add-in-Webpart zu testen, wählen Sie auf der Menüleiste **Debuggen**, **Debuggen starten**aus.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="c7ce3-145">Wenn Sie aufgefordert werden, die Datei "web.config" zu ändern, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="c7ce3-146">Um das Add-in-Webpart zu debuggen, legen Sie die entsprechenden Haltepunkte im hinzugefügten Skript fest.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="c7ce3-147">Navigieren Sie zu einer PDP-Seite, und wählen Sie im Menü Extras (Zahnradsymbol) die Option **Seite bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="c7ce3-148">Fügen Sie das getProjectable- **Titel** Teil zu einem Webpart auf der Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="c7ce3-149">Die Projekt-ID wird im **Span** -Steuerelement auf der Webpartseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="c7ce3-150">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c7ce3-150">Next steps</span></span>
<span data-ttu-id="c7ce3-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="c7ce3-151"></span></span>

<span data-ttu-id="c7ce3-152">Das Add-in-Webpart in diesem Beispiel greift nicht auf Project Server-Daten oder SharePoint-Daten zu.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="c7ce3-153">Sie können die Produkt-ID verwenden, um Informationen zum aktuellen Projekt mithilfe einer Client-API abzurufen, beispielsweise des JavaScript-Objektmodells oder des REST-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="c7ce3-154">Geben Sie in der Datei Datei AppManifest. XML die Berechtigungen an, die das Add-in für den Zugriff auf Project Server-Daten oder SharePoint-Daten benötigt.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="c7ce3-155">Weitere Informationen zum Festlegen von benutzerdefinierten Eigenschaften für ein Add-in-Webpart finden Sie unter [Erstellen von Add-in-Komponenten für die Installation mit Ihrem SharePoint-Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c7ce3-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="c7ce3-156">Beispiel: Aufrufen der Projekt-ID in einem Add-in-Webpart auf einer PDP-Seite</span><span class="sxs-lookup"><span data-stu-id="c7ce3-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="c7ce3-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="c7ce3-157"></span></span>

<span data-ttu-id="c7ce3-158">Das folgende Beispiel ist der vollständige Code auf der Seite getProjecto. aspx des Client Webparts.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="c7ce3-159">Der Code registriert einen Ereignislistener und einen Ereignishandler, der eine Nachricht empfängt und analysiert, die die Projekt-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
```HTML
<%@ Page language="C#" Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<WebPartPages:AllowFraming ID="AllowFraming" runat="server" />
<html>
<head>
    <title></title>
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/MicrosoftAjax.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.js"></script>
    <script type="text/javascript">
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
        (function () {
            var hostUrl = '';
            var link = document.createElement('link');
            link.setAttribute('rel', 'stylesheet');
            if (document.URL.indexOf('?') != -1) {
                var params = document.URL.split('?')[1].split('&');
                for (var i = 0; i < params.length; i++) {
                    var p = decodeURIComponent(params[i]);
                    if (/^SPHostUrl=/i.test(p)) {
                        hostUrl = p.split('=')[1];
                        link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                        break;
                    }
                }
            }
            if (hostUrl == '') {
                link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
            }
            document.head.appendChild(link);
        })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
    </script>
</head>
<body>
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
</body>
</html>

```

## <a name="see-also"></a><span data-ttu-id="c7ce3-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7ce3-160">See also</span></span>

- [<span data-ttu-id="c7ce3-161">Project-Programmieraufgaben</span><span class="sxs-lookup"><span data-stu-id="c7ce3-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="c7ce3-162">Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="c7ce3-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="c7ce3-163">Erstellen von Add-In-Webparts zur Installation mit Ihrem SharePoint-Add-In</span><span class="sxs-lookup"><span data-stu-id="c7ce3-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

