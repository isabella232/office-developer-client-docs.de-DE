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
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite

Add-in-Parts werden in **iframe** -Elementen gehostet, die vollständig von der Hostingseite isoliert sind. Wenn Sie Informationen über das aktuelle Projekt aus einem Add-in-Webpart auf der Projektdetailseite (PDP) abrufen möchten, können Sie die **Window. PostMessage** -Methode, einen Ereignislistener und einen Ereignishandler verwenden, der die Projekt-ID aus der Nachricht analysiert. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>VoraussetZungen für das Erstellen eines von SharePoint gehosteten Add-in-Parts, das die Projekt-ID abruft
<a name="Prereqs"> </a>

Um das Codebeispiel in diesem Artikel verwenden zu können, benötigen Sie eine der folgenden Optionen:
  
- SharePoint 2013 und Project Server 2013, konfiguriert für die Add-in-Isolierung. Wenn Sie Remote entwickeln, muss der Server querladen von Add-Ins unterstützen, oder Sie müssen das Add-in auf einer Entwickler Website installieren.
  
- SharePoint Online und Project Online
    
    - Visual Studio 2013, Visual Studio 2012 mit Office Developer Tools für Visual Studio 2013 oder Napa
        
    - Über ausreichende Berechtigungen für den angemeldeten Benutzer:
        
        - Lokale Administratorberechtigungen auf dem Entwicklungscomputer installiert.
            
        - Lesezugriff auf mindestens ein Projekt.
            
        - Berechtigung zum Bearbeiten von Seiten auf der Project Web App-Website.
            
        - Sie müssen als eine andere Person als das Systemkonto angemeldet sein. Das Systemkonto verfügt nicht über die Berechtigung zum Installieren eines Add-Ins.
    
Weitere Informationen zu Add-Ins für Project finden Sie unter [vorausSetzungen für die Erstellung eines Add-Ins für Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) . Unter [Einrichten einer lokalen Entwicklungsumgebung für SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) finden Sie Anleitungen zum lokalen Setup (einschließlich der Deaktivierung der Loopbacküberprüfung). Wenn Sie Remote entwickeln, finden Sie weitere Informationen unter [entwickeln von Apps für SharePoint auf einem Remote System](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Erstellen des von SharePoint gehosteten Add-in-und Client-Webparts
<a name="CreateApp"> </a>

1. Öffnen Sie Visual Studio, und wählen Sie **Datei** > **Neues** > **Projekt**aus.
    
2. Wählen Sie im Dialogfeld **Neues Projekt** aus der Dropdownliste oben im Dialogfeld die Option **.NET Framework 4.5**. 
    
3. wählen sie In der liste **vorlagen** die option **Visual C#** > **Office/sharepoint** > **add-ins** > **add-in für sharepoint 2013**.
    
4. Nennen Sie das Add-in-GetProjectIdAddinPart, und klicken Sie dann auf die Schaltfläche **OK** . 
    
5. Geben Sie im Dialogfeld **Neues Add-in für SharePoint** die URL der PWA-Website ein, die Sie zum Debuggen verwenden möchten (Beispiel: _https://contoso.com/sites/pwasite/_).
    
6. Wählen Sie die von **SharePoint gehostete** Option aus, um Ihr Add-in zu hosten, und klicken Sie dann auf die Schaltfläche **Fertig stellen** . 
    
7. Öffnen Sie im Projektmappen- **Explorer**das Kontextmenü für das GetProjectIdAddinPart-Projekt, und wählen Sie dann**Neues Element** **Hinzufügen** > aus.
    
8. Wählen Sie im Dialogfeld **Neues Element hinzufügen** die Option **Client Webpart (Host Web)** aus, benennen Sie das Webpart getprojecto, und klicken Sie dann auf die Schaltfläche **Hinzufügen** . 
    
9. Wählen Sie im Dialogfeld **Client-Webpart erstellen** die Option **neuen Client-Webpart erstellen** aus, und klicken Sie dann auf die Schaltfläche **Fertig stellen** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Abrufen der Projekt-ID im Add-in-Webpart
<a name="GetProjectId"> </a>

Der getProjectable-Add-in-Webpart definiert seinen benutzerdefinierten Code auf der Seite getProjected. aspx des Client-Webparts. Die Logik, die die Nachricht empfängt und verarbeitet, wird im **Head** -Element der Seite definiert, und die Page-Steuerelemente werden im **Body** -Element der Seite definiert. 
  
1. Öffnen Sie die Webpartseite getProjectable. aspx (im Ordner **pages** ). 
    
2. Ersetzen Sie im **Head** -Element der Seite den Code zwischen den **Script** -Tags durch den folgenden Code. 
    
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

3. Fügen Sie den folgenden Code in das **Body** -Element der Seite ein. Der Code definiert ein Span-Steuerelement, das die Projekt-ID anzeigt. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. Ändern Sie optional in der Datei Elements. XML den Namen, den Titel, die Beschreibung und die Standardgröße des Add-in-Parts. In diesem Beispiel werden die Standardwerte verwendet.
    
5. Um das Add-in-Webpart zu testen, wählen Sie auf der Menüleiste **Debuggen**, **Debuggen starten**aus. Wenn Sie aufgefordert werden, die Datei "web.config" zu ändern, klicken Sie auf **OK**. 
    
   Um das Add-in-Webpart zu debuggen, legen Sie die entsprechenden Haltepunkte im hinzugefügten Skript fest.
    
6. Navigieren Sie zu einer PDP-Seite, und wählen Sie im Menü Extras (Zahnradsymbol) die Option **Seite bearbeiten** aus. 
    
7. Fügen Sie das getProjectable- **Titel** Teil zu einem Webpart auf der Seite hinzu. Die Projekt-ID wird im **Span** -Steuerelement auf der Webpartseite angezeigt. 
    
## <a name="next-steps"></a>Nächste Schritte
<a name="NextSteps"> </a>

Das Add-in-Webpart in diesem Beispiel greift nicht auf Project Server-Daten oder SharePoint-Daten zu. Sie können die Produkt-ID verwenden, um Informationen zum aktuellen Projekt mithilfe einer Client-API abzurufen, beispielsweise des JavaScript-Objektmodells oder des REST-Diensts.
  
Geben Sie in der Datei Datei AppManifest. XML die Berechtigungen an, die das Add-in für den Zugriff auf Project Server-Daten oder SharePoint-Daten benötigt. 
  
Weitere Informationen zum Festlegen von benutzerdefinierten Eigenschaften für ein Add-in-Webpart finden Sie unter [Erstellen von Add-in-Komponenten für die Installation mit Ihrem SharePoint-Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) . 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Beispiel: Aufrufen der Projekt-ID in einem Add-in-Webpart auf einer PDP-Seite
<a name="CodeExample"> </a>

Das folgende Beispiel ist der vollständige Code auf der Seite getProjecto. aspx des Client Webparts. Der Code registriert einen Ereignislistener und einen Ereignishandler, der eine Nachricht empfängt und analysiert, die die Projekt-ID enthält.
  
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
- [Erstellen von Add-In-Webparts zur Installation mit Ihrem SharePoint-Add-In](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

