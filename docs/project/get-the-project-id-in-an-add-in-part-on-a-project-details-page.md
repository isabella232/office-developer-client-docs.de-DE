---
title: Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Add-In-Webparts werden in iframe-Elementen gehostet, die vollständig von der Hostingseite isoliert sind. Um Informationen zum aktuellen Projekt aus einem Add-In-Webpart auf Project Detailseite (PDP) abzurufen, können Sie die Window.postMessage-Methode, einen Ereignislistener und einen Ereignishandler verwenden, der die Projekt-ID aus der Nachricht analysiert.
ms.openlocfilehash: 78851a6008157741ed489ce8b3868497823d48d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623558"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Abrufen der Projekt-ID in einem Add-In-Webpart auf einer Project-Detailseite

Add-In-Webparts werden in **iframe-Elementen** gehostet, die vollständig von der Hostingseite isoliert sind. Um Informationen zum aktuellen Projekt aus einem Add-In-Webpart auf Project Detailseite (PDP) abzurufen, können Sie die **window.postMessage-Methode,** einen Ereignislistener und einen Ereignishandler verwenden, der die Projekt-ID aus der Nachricht analysiert. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Voraussetzungen für das Erstellen eines SharePoint gehosteten Add-In-Webparts, das die Projekt-ID abruft
<a name="Prereqs"> </a>

Um das Codebeispiel in diesem Artikel zu verwenden, benötigen Sie eine der folgenden Komponenten:
  
- SharePoint 2013 und Project Server 2013, konfiguriert für die Add-In-Isolation. Wenn Sie remote entwickeln, muss der Server das Querladen von Add-Ins unterstützen, oder Sie müssen das Add-In auf einer Entwicklerwebsite installieren.
  
- SharePoint Online und Project Online
    
    - Visual Studio 2013, Visual Studio 2012 mit Office Developer Tools für Visual Studio 2013 oder Napa
        
    - Über ausreichende Berechtigungen für den angemeldeten Benutzer:
        
        - Lokale Administratorberechtigungen auf dem Entwicklungscomputer installiert.
            
        - Lesezugriff auf mindestens ein Projekt.
            
        - Berechtigung zum Bearbeiten von Seiten auf der Project Web App-Website.
            
        - Sie müssen als eine andere Person als das Systemkonto angemeldet sein. Das Systemkonto verfügt nicht über die Berechtigung zum Installieren eines Add-Ins.
    
Weitere Informationen zu Add-Ins für Project finden Sie unter "Voraussetzungen für das [Erstellen eines Add-Ins für Project Server 2013".](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) Informationen zum lokalen Setup finden Sie unter [Einrichten einer lokalen Entwicklungsumgebung für SharePoint-Add-Ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) (einschließlich der Deaktivierung der Loopbacküberprüfung, falls erforderlich). Wenn Sie remote entwickeln, lesen Sie ["Entwickeln von Apps für SharePoint auf einem Remotesystem".](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Erstellen des SharePoint gehosteten Add-Ins und Clientwebparts
<a name="CreateApp"> </a>

1. Öffnen Sie Visual Studio, und wählen Sie  >  **"Datei**  >  **neu" Project** aus.
    
2. Wählen Sie im Dialogfeld **Neues Projekt** in der Dropdownliste oben im Dialogfeld **.NET Framework 4.5** aus. 
    
3. Wählen Sie in der **Vorlagenliste** **Visual C#**  >  **Office/SharePoint**  >  **Add-Ins-Add-In**  >  **für SharePoint 2013** aus.
    
4. Geben Sie dem Add-In den Namen "GetProjectIdAddinPart", und klicken Sie dann auf die Schaltfläche **"OK".** 
    
5. Geben Sie im Dialogfeld **"Neues Add-In für SharePoint"** die URL der PWA Website ein, die Sie zum Debuggen verwenden möchten (z. B.: _https://contoso.com/sites/pwasite/_ ).
    
6. Wählen Sie die **SharePoint gehostete** Option aus, um Ihr Add-In zu hosten, und klicken Sie dann auf die Schaltfläche **"Fertig stellen".** 
    
7. Öffnen Sie im **Projektmappen-Explorer** das Kontextmenü für das Projekt "GetProjectIdAddinPart", und wählen Sie dann "Neues Element **hinzufügen"**  >  aus.
    
8. Wählen Sie im Dialogfeld **"Neues Element hinzufügen"** das **Clientwebpart (Hostweb)** aus, benennen Sie das Webpart "GetProjectId", und klicken Sie dann auf die Schaltfläche **"Hinzufügen".** 
    
9. Wählen Sie im Dialogfeld **"Client-Webpart erstellen"** die Option **"Neue Clientwebpartseite** erstellen" aus, und klicken Sie dann auf die Schaltfläche **"Fertig stellen".** 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Abrufen der Projekt-ID im Add-In-Webpart
<a name="GetProjectId"> </a>

Das Add-In-Webpart "GetProjectId" definiert den benutzerdefinierten Code auf der Seite "GetProjectId.aspx" des Clientwebparts. Die Logik, die die Nachricht empfängt und behandelt, wird im **Kopfelement** der Seite definiert, und die Seitensteuerelemente werden im **Textelement** der Seite definiert. 
  
1. Öffnen Sie die Webpartseite "GetProjectId.aspx" (im Ordner **"Pages").** 
    
2. Ersetzen Sie im **Head-Element** der Seite den Code zwischen den **Skripttags** durch den folgenden Code. 
    
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

3. Fügen Sie den folgenden Code im **Textelement** der Seite hinzu. Der Code definiert ein Span-Steuerelement, das die Projekt-ID anzeigt. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. Ändern Sie in der datei Elements.xml optional den Namen, titel, die Beschreibung und die Standardgröße des Add-In-Webparts. In diesem Beispiel werden die Standardwerte verwendet.
    
5. Um das Add-In-Webpart zu testen, wählen Sie in der Menüleiste **"Debuggen"** und **"Debuggen starten"** aus. Wenn Sie aufgefordert werden, die Datei "web.config" zu ändern, klicken Sie auf **OK**. 
    
   Um das Add-In-Webpart zu debuggen, legen Sie die entsprechenden Haltepunkte im Skript fest, das Sie hinzugefügt haben.
    
6. Navigieren Sie zu einer PDP-Seite, und wählen Sie im Menü "Extras" (Zahnradsymbol) die **Seite "Bearbeiten"** aus. 
    
7. Fügen Sie das **GetProjectId-Titelpart** zu einem Webpart auf der Seite hinzu. Die Projekt-ID wird im **Span-Steuerelement** auf der Webpartseite angezeigt. 
    
## <a name="next-steps"></a>Nächste Schritte
<a name="NextSteps"> </a>

Das Add-In-Webpart in diesem Beispiel greift nicht auf Project Serverdaten oder SharePoint Daten zu. Sie können die Produkt-ID verwenden, um Informationen zum aktuellen Projekt mithilfe einer Client-API wie dem JavaScript-Objektmodell oder dem REST-Dienst abzurufen.
  
Geben Sie in der datei AppManifest.xml die Berechtigungen an, die Ihr Add-In für den Zugriff auf Project Serverdaten oder SharePoint Daten benötigt. 
  
Weitere Informationen zum Festlegen benutzerdefinierter Eigenschaften für ein Add-In-Webpart finden Sie unter Erstellen von [Add-In-Webparts für die Installation mit Ihrem SharePoint-Add-In.](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Beispiel: Abrufen der Projekt-ID in einem Add-In-Webpart auf einer PDP-Seite
<a name="CodeExample"> </a>

Das folgende Beispiel ist der vollständige Code auf der Seite "GetProjectID.aspx" des Clientwebparts. Der Code registriert einen Ereignislistener und einen Ereignishandler, der eine Nachricht empfängt und analysiert, die die Projekt-ID enthält.
  
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
    

