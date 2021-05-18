---
title: Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Add-In-Teile werden in iframe-Elementen gehostet, die vollständig von der Hostingseite isoliert sind. Um Informationen zum aktuellen Projekt aus einem Add-In-Teil auf der Project-Detailseite (PDP) zu erhalten, können Sie die window.postMessage-Methode, einen Ereignislistener und einen Ereignishandler verwenden, der die Projekt-ID aus der Nachricht analysiert.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322596"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="78794-104">Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite</span><span class="sxs-lookup"><span data-stu-id="78794-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="78794-105">Add-In-Teile werden in **iframe-Elementen** gehostet, die vollständig von der Hostingseite isoliert sind.</span><span class="sxs-lookup"><span data-stu-id="78794-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="78794-106">Zum Erhalten von Informationen zum aktuellen Projekt aus einem Add-In-Teil auf Project Details Page (PDP) können Sie die **window.postMessage-Methode,** einen Ereignislistener und einen Ereignishandler verwenden, der die Projekt-ID aus der Nachricht analysiert.</span><span class="sxs-lookup"><span data-stu-id="78794-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="78794-107">Voraussetzungen für das Erstellen SharePoint gehosteten Add-In-Teils, das die Projekt-ID ab ruft</span><span class="sxs-lookup"><span data-stu-id="78794-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="78794-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="78794-108"><a name="Prereqs"> </a></span></span>

<span data-ttu-id="78794-109">Um das Codebeispiel in diesem Artikel zu verwenden, benötigen Sie eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="78794-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="78794-110">SharePoint 2013 und Project Server 2013, konfiguriert für die Add-In-Isolation.</span><span class="sxs-lookup"><span data-stu-id="78794-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="78794-111">Wenn Sie remote entwickeln, muss der Server das Querladen von Add-Ins unterstützen, oder Sie müssen das Add-In auf einer Entwicklerwebsite installieren.</span><span class="sxs-lookup"><span data-stu-id="78794-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="78794-112">SharePoint Online und Project Online</span><span class="sxs-lookup"><span data-stu-id="78794-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="78794-113">Visual Studio 2013, Visual Studio 2012 mit Office Entwicklertools für Visual Studio 2013 oder Napa</span><span class="sxs-lookup"><span data-stu-id="78794-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="78794-114">Über ausreichende Berechtigungen für den angemeldeten Benutzer:</span><span class="sxs-lookup"><span data-stu-id="78794-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="78794-115">Lokale Administratorberechtigungen auf dem Entwicklungscomputer installiert.</span><span class="sxs-lookup"><span data-stu-id="78794-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="78794-116">Lesezugriff auf mindestens ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="78794-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="78794-117">Berechtigung zum Bearbeiten von Seiten auf Project Web App-Website.</span><span class="sxs-lookup"><span data-stu-id="78794-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="78794-118">Sie müssen als eine andere Person als das Systemkonto angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="78794-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="78794-119">Das Systemkonto verfügt nicht über die Berechtigung zum Installieren eines Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="78794-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="78794-120">Weitere Informationen zu Add-Ins für Project [Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) finden Sie unter Voraussetzungen für das Erstellen eines Project.</span><span class="sxs-lookup"><span data-stu-id="78794-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="78794-121">Unter Einrichten einer lokalen Entwicklungsumgebung für [SharePoint-Add-Ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) finden Sie Anleitungen zum lokalen Setup (einschließlich der Deaktivierung der Loopbacküberprüfung, falls erforderlich).</span><span class="sxs-lookup"><span data-stu-id="78794-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="78794-122">Wenn Sie remote entwickeln, finden Sie weitere Informationen unter [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="78794-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="78794-123">Erstellen SharePoint gehosteten Add-Ins und Clientwebteils</span><span class="sxs-lookup"><span data-stu-id="78794-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="78794-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="78794-124"><a name="CreateApp"> </a></span></span>

1. <span data-ttu-id="78794-125">Öffnen Visual Studio, und wählen **Sie Datei**  >  **Neu**  >  **Project**.</span><span class="sxs-lookup"><span data-stu-id="78794-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="78794-126">Wählen Sie im Dialogfeld **Neues Projekt** in der Dropdownliste oben im Dialogfeld **.NET Framework 4.5** aus.</span><span class="sxs-lookup"><span data-stu-id="78794-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="78794-127">Wählen Sie **in** der Liste Vorlagen die **Option Visual C#**  >  **Office/SharePoint-Add-Ins-Add-In**  >  **für**  >  **SharePoint 2013 aus.**</span><span class="sxs-lookup"><span data-stu-id="78794-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="78794-128">Nennen Sie das Add-In GetProjectIdAddinPart, und wählen Sie dann die **Schaltfläche OK** aus.</span><span class="sxs-lookup"><span data-stu-id="78794-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="78794-129">Geben Sie im Dialogfeld Neues **Add-In** für SharePoint die URL der PWA-Website ein, die Sie zum Debuggen verwenden möchten (z. B.: _https://contoso.com/sites/pwasite/_ ).</span><span class="sxs-lookup"><span data-stu-id="78794-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="78794-130">Wählen Sie **SharePoint gehostete Option** aus, um Ihr Add-In zu hosten, und klicken Sie dann auf die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="78794-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="78794-131">Öffnen **Sie im** Projektmappen-Explorer das Kontextmenü für das Projekt GetProjectIdAddinPart, und wählen Sie **dann Neues** Element  >  **hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="78794-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="78794-132">Wählen Sie im Dialogfeld Neues **Element** hinzufügen die Option **Clientwebteil (Hostweb),** benennen Sie das Webteil GetProjectId, und wählen Sie dann die Schaltfläche **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="78794-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="78794-133">Wählen Sie **im Dialogfeld Client-Web part** erstellen die Option Neue **Clientwebseite** erstellen aus, und klicken Sie dann auf **die** Schaltfläche Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="78794-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="78794-134">Die Projekt-ID im Add-In-Teil erhalten</span><span class="sxs-lookup"><span data-stu-id="78794-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="78794-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="78794-135"><a name="GetProjectId"> </a></span></span>

<span data-ttu-id="78794-136">Das GetProjectId-Add-In-Part definiert seinen benutzerdefinierten Code auf der GetProjectId.aspx-Seite des Clientwebteils.</span><span class="sxs-lookup"><span data-stu-id="78794-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="78794-137">Die Logik, die die Nachricht empfängt und verarbeitet, wird im **Head-Element** der Seite definiert, und die Seitensteuerelemente werden im **Textelement** der Seite definiert.</span><span class="sxs-lookup"><span data-stu-id="78794-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="78794-138">Öffnen Sie die Web part-Seite GetProjectId.aspx (im Ordner **Seiten).**</span><span class="sxs-lookup"><span data-stu-id="78794-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="78794-139">Ersetzen Sie **im head-Element** der Seite den Code zwischen den **Skripttags** durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="78794-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="78794-140">Fügen Sie den folgenden Code im **Textelement** der Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="78794-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="78794-141">Der Code definiert ein Spansteuerelement, das die Projekt-ID anzeigt.</span><span class="sxs-lookup"><span data-stu-id="78794-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="78794-142">Ändern Sie Elements.xml Namen, Titel, Beschreibung und Standardgröße des Add-In-Teils in der datei.</span><span class="sxs-lookup"><span data-stu-id="78794-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="78794-143">In diesem Beispiel werden die Standardwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="78794-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="78794-144">Wählen Sie zum Testen des Add-In-Teils auf der Menüleiste **Debuggen**, **Debuggen starten aus.**</span><span class="sxs-lookup"><span data-stu-id="78794-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="78794-145">Wenn Sie aufgefordert werden, die Datei "web.config" zu ändern, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="78794-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="78794-146">Zum Debuggen des Add-In-Teils legen Sie geeignete Haltepunkte in dem skript fest, das Sie hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="78794-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="78794-147">Navigieren Sie zu einer PDP-Seite, und wählen Sie **im** Menü Extras die Option Seite bearbeiten (Zahnradsymbol).</span><span class="sxs-lookup"><span data-stu-id="78794-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="78794-148">Fügen Sie **das GetProjectId Title-Teil** zu einem Webteil auf der Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="78794-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="78794-149">Die Projekt-ID wird im **Span-Steuerelement** auf der Web part-Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="78794-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="78794-150">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="78794-150">Next steps</span></span>
<span data-ttu-id="78794-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="78794-151"><a name="NextSteps"> </a></span></span>

<span data-ttu-id="78794-152">Das Add-In-Teil in diesem Beispiel hat keinen Zugriff auf Project Serverdaten oder SharePoint Daten.</span><span class="sxs-lookup"><span data-stu-id="78794-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="78794-153">Sie können die Produkt-ID verwenden, um Informationen zum aktuellen Projekt mithilfe einer Client-API wie dem JavaScript-Objektmodell oder dem REST-Dienst zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="78794-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="78794-154">Geben Sie in AppManifest.xml die Berechtigungen an, die Ihr Add-In für den Zugriff auf Project Serverdaten oder SharePoint benötigt.</span><span class="sxs-lookup"><span data-stu-id="78794-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="78794-155">Weitere Informationen zum Festlegen von benutzerdefinierten Eigenschaften für ein Add-In-Teil finden Sie unter Erstellen von Add-In-Teilen, die mit Ihrem [SharePoint-Add-In](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) installiert werden.</span><span class="sxs-lookup"><span data-stu-id="78794-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="78794-156">Beispiel: Abrufen der Projekt-ID in einem Add-In-Part auf einer PDP-Seite</span><span class="sxs-lookup"><span data-stu-id="78794-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="78794-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="78794-157"><a name="CodeExample"> </a></span></span>

<span data-ttu-id="78794-158">Das folgende Beispiel ist der vollständige Code auf der GetProjectID.aspx-Seite des Clientwebteils.</span><span class="sxs-lookup"><span data-stu-id="78794-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="78794-159">Der Code registriert einen Ereignislistener und einen Ereignishandler, der eine Nachricht empfängt und analysiert, die die Projekt-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="78794-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="78794-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78794-160">See also</span></span>

- [<span data-ttu-id="78794-161">Project-Programmieraufgaben</span><span class="sxs-lookup"><span data-stu-id="78794-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="78794-162">Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="78794-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="78794-163">Erstellen von Add-In-Webparts zur Installation mit Ihrem SharePoint-Add-In</span><span class="sxs-lookup"><span data-stu-id="78794-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

