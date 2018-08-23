---
title: Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Add-in-Komponenten gehostet werden in Iframe-Elemente, die von der Hostingseite vollständig isoliert sind. Um Informationen über das aktuelle Projekt aus einer Webpart-Add-in auf Projekt Details Seite (PDP) erhalten, können Sie die window.postMessage-Methode, einen Ereignislistener und einen Ereignishandler, der analysiert wird, die Projekt-ID aus der Nachricht.
ms.openlocfilehash: d9f6d02f328860f46784f86c049581fa28bb4749
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594425"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite

Add-in-Komponenten gehostet werden in **Iframe** -Elemente, die von der Hostingseite vollständig isoliert sind. Um Informationen über das aktuelle Projekt aus einer Webpart-Add-in auf Projekt Details Seite (PDP) erhalten, können Sie die **window.postMessage** -Methode, einen Ereignislistener und einen Ereignishandler, der analysiert wird, die Projekt-ID aus der Nachricht. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Voraussetzungen zum Erstellen eines SharePoint-Hosting-add-in Webparts, das die Projekt-ID versehen werden.
<a name="Prereqs"> </a>

Um das Codebeispiel in diesem Artikel zu verwenden, benötigen Sie eine der folgenden:
  
- SharePoint 2013 und Project Server 2013, für die Add-in-Isolation konfiguriert sind. Wenn Sie Remote-Entwicklung, muss der Server Sideloading Add-in-Unterstützung oder müssen Sie das Add-in auf einer Entwicklerwebsite installieren.
  
- SharePoint Online und Project Online
    
    - Visual Studio 2013 Visual Studio 2012 mit Office-Entwickler-Tools für Visual Studio 2013 oder Napa
        
    - Über ausreichende Berechtigungen für den angemeldeten Benutzer:
        
        - Lokale Administratorberechtigungen auf dem Entwicklungscomputer installiert.
            
        - Lesezugriff auf mindestens ein Projekt.
            
        - Berechtigung zum Bearbeiten von Seiten auf der Project Web App-Website.
            
        - Sie müssen als eine andere Person als das Systemkonto angemeldet sein. Das Systemkonto verfügt nicht über die Berechtigung um ein Add-in zu installieren.
    
Weitere Informationen zur-Add-ins für Project finden Sie unter [Voraussetzungen für die Erstellung einer Add-in für Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) . Hinweise zum lokalen Setup (einschließlich wie das Kontrollkästchen Loopback deaktivieren, falls erforderlich) finden Sie unter [Einrichten einer lokalen Entwicklungsumgebung für SharePoint-Add-ins](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) . Wenn Sie einen Remote entwickeln, finden Sie unter [Developing apps für SharePoint auf einem Remotesystem](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Erstellen Sie das SharePoint-Hosting-add-in und Client-Webpart
<a name="CreateApp"> </a>

1. Öffnen Sie Visual Studio, und wählen Sie **Datei** > **New** > **Projekt**.
    
2. Wählen Sie im Dialogfeld **Neues Projekt** aus der Dropdownliste oben im Dialogfeld die Option **.NET Framework 4.5**. 
    
3. Wählen Sie in der Liste **Vorlagen** , **Visual C#-** > **Office/SharePoint** > **-Add-ins** > **Add-in für SharePoint 2013**.
    
4. Nennen Sie die GetProjectIdAddinPart-Add-in, und wählen Sie dann auf die Schaltfläche **OK** . 
    
5. Geben Sie im Dialogfeld **Neues Add-In für SharePoint** die URL der PWA-Website, die Sie für das debugging verwenden möchten (zum Beispiel: _https://contoso.com/sites/pwasite/_).
    
6. Wählen Sie die Option **SharePoint-Hosting** zum Hosten Ihrer-add-in, und wählen Sie dann auf die Schaltfläche **Fertig stellen** . 
    
7. Klicken Sie im **Projektmappen-Explorer**, öffnen Sie das Kontextmenü für das Projekt GetProjectIdAddinPart, und wählen Sie dann **Hinzufügen** > **Neues Element**.
    
8. Klicken Sie im Dialogfeld **Neues Element hinzufügen** wählen Sie **Clientwebpart (Hostweb)**, nennen Sie das Webpart GetProjectId, und wählen Sie dann auf die Schaltfläche **Hinzufügen** . 
    
9. Klicken Sie im Dialogfeld **Erstellen Clientwebpart** wählen Sie die Option **Erstellen einer neuen Client Webpart-Seite** aus aus, und wählen Sie dann auf die Schaltfläche **Fertig stellen** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Rufen Sie die Project-ID im Webpart-Add-in
<a name="GetProjectId"> </a>

Add-in-Teil GetProjectId definiert den benutzerdefinierten Code auf der Seite GetProjectId.aspx des Client-WebParts. Die Logik, die empfängt und verarbeitet die Nachricht im **Head** -Element der Seite und die Steuerelemente im **Body** -Element auf der Seite definiert sind. 
  
1. Öffnen Sie die Webpartseite GetProjectId.aspx (im Ordner **Seiten** ). 
    
2. Ersetzen Sie im **Head** -Element der Seite den Code zwischen den **Script** -Tags mit den folgenden Code ein. 
    
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

3. Fügen Sie den folgenden Code im **Body** -Element auf der Seite. Der Code definiert ein Span-Steuerelement, das die Projekt-ID anzeigt 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. Optional in der Datei "Elements.xml" Ändern der Name, Titel, Beschreibung und Standardgröße des Add-in-Webparts. In diesem Beispiel werden die Standardwerte verwendet.
    
5. Wählen Sie zum Testen des Webparts-Add-in auf der Menüleiste **Debuggen**, **Debuggen starten**aus. Wenn Sie aufgefordert werden, ändern Sie die Datei "Web.config", und wählen Sie die Schaltfläche **OK** . 
    
   Um das Webpart-Add-in zu debuggen, legen Sie die geeigneten Haltepunkte in das Skript, das Sie hinzugefügt haben.
    
6. Navigieren Sie zu einer PDP-Seite, und wählen Sie im Menü Extras (Zahnradsymbol) **Bearbeiten (Seite)** . 
    
7. Ein Webpart auf der Seite das Webpart **GetProjectId Titel** hinzuzufügen. Die Projekt-ID in das **span** -Steuerelement auf einer Webpartseite angezeigt. 
    
## <a name="next-steps"></a>Nächste Schritte
<a name="NextSteps"> </a>

In diesem Beispiel wird das Teil-Add-in zugreifen nicht Project Server-Daten oder SharePoint-Daten. Sie können die Produkt-ID zum Abrufen von Informationen über das aktuelle Projekt mithilfe einer Clients-API, wie das JavaScript-Objektmodell oder den REST-Dienst verwenden.
  
Geben Sie in der Datei AppManifest.XML die Berechtigungen, die Ihr Add-in benötigt Zugriff auf Project Server-Daten oder SharePoint-Daten. 
  
Finden Sie unter [Create-Add-in Webparts mit Ihrer SharePoint-Add-in installieren](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) , erfahren, wie benutzerdefinierte Eigenschaften für ein Webpart-Add-in festgelegt. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Beispiel: Abrufen der Project-ID in einem Webpart-Add-in auf einem Zeichenblatt PDP
<a name="CodeExample"> </a>

Im folgende Beispiel wird der vollständige Code in die Clientwebpart GetProjectID.aspx Seite. Der Code registriert einen Ereignislistener und einen Ereignishandler, der empfängt und analysiert eine Nachricht mit der Project-ID.
  
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

## <a name="see-also"></a>Siehe auch

- [Project-Programmieraufgaben](project-programming-tasks.md)
- [Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins](create-a-sharepoint-hosted-project-server-add-in.md)
- [Erstellen von Add-In-Webparts zur Installation mit Ihrem SharePoint-Add-In](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

