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
# <a name="from-0-to-60-with-project-online"></a>Von 0 auf 100 mit Project Online

Ein Anwendungsentwickler kann eine Project Online-Website (in SharePoint gehostet) mithilfe eigenständiger Anwendungen und/oder Projekt-Add-Ins anpassen. Es gibt eine Vielzahl von Anwendungen, die von den Anforderungen der Beteiligten an einem Projekt bis hin zu PMO-Supportfunktionen reichen, wie beispielsweise einem der folgenden:
  
- Optimierter Zeitkarten Dateneintrag für Arbeitskräfte
- Effiziente Zeitkarten Genehmigung für Vorgesetzte
- Aufsicht über Genehmigungen (Beschaffung und Status), die für ein Projekt erforderlich sind
- Status/Integritätsprüfung aktiver Projekte
- Problembericht
- Change Management-Status Bericht
    
Project Online umfasst API-Unterstützung für die folgenden Szenarien:
  
- Für ein gehostetes Projekt (SharePoint):
    
  - Code (JavaScript, HTML, CSS), der in SharePoint Online gehostet wird
  - Objekte, die in den Browser heruntergeladen und für SharePoint Online ausgeführt werden.  
  - Geschäftslogik in JavaScript   
  - Zugreifen auf Daten, die in Project Online oder SharePoint wie (aber nicht beschränkt auf) in gespeichert sind:  
  - Custom fields (benutzerdefinierte Felder)  
  - Listen
    
- Für ein von einem Projekt (SharePoint) vom Anbieter gehostetes Add-in:
    
  - Code, der auf einer Website außerhalb der Project Online-Website vorhanden ist 
  - Eine externe Website, die (aber nicht beschränkt auf) sein kann:  
  - Eine andere SharePoint-Website  
  - Web-App/Dienst auf einer beliebigen Plattform  
  - Die externe Website enthält Geschäftslogik  
  - Der Browser wird von Project online zu externer Website mit Zugriffstoken zu Project Online umgeleitet.  
  - Die externe Website kann Aufrufe an SharePoint und Project online tätigen
    
- Für ein externes/eigenständiges Add-in:
    
  - Der Benutzer führt eine Anwendung auf dem Gerät aus.
  - Anwendung authentifiziert und ruft Project Online-APIs direkt auf
    

|Art der Anwendung|API-Implementierung|Zielumgebung|Anwendungsbeispiele|
|:-----|:-----|:-----|:-----|
|Projekt gehostet  <br/> |JSOM (Java Script Object Model)  <br/> REST  <br/> |Browser  <br/> |Zeitkarten Eintrag  <br/> Zeitkarten Genehmigung  <br/> Projekt Status  <br/> Problembericht  <br/> |
|Gehosteter Projektanbieter  <br/> |CSOM-Clientbibliothek  <br/> |Azure-Website/-App  <br/> Nicht-Windows-Umgebung (Lampe usw.)  <br/> |Externe Validierung in der Arbeitszeittabelle  <br/> Projekt-Importierer  <br/> |
|Extern/eigenständig  <br/> |REST  <br/> CSOM  <br/> |REST – beliebige Plattform  <br/> CSOM-beliebige von .NET unterstützte Plattform  <br/> |Zeitkarten Eintrag  <br/> Migration von Projekten zu einer neuen Website  <br/> Change Management Status.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Was wird benötigt, um die Entwicklung von Anwendungen für Project online zu beginnen?

Die allgemeinen Elemente, die für die Entwicklung von Project Online-Anwendungen erforderlich sind, sind Project Online-Konto und Testdaten--Projekte und projektbezogene Informationen, die Zuordnungen, Aufgaben, Ressourcen und benutzerdefinierte Felder einbeziehen. Eine Entwicklungsumgebung ist ebenfalls erforderlich, aber die Spezifik der Entwicklungsumgebung hängt vom Typ der Anwendung und der API-Schnittstelle ab, die für die Anwendung benötigt wird. In den nächsten Abschnitten werden die Entwicklungsanforderungen für die drei API-Schnittstellen beschrieben.
  
In der Referenzdokumentation wird das für alle drei Schnittstellen gängige Objektmodell sowie eine Entitätszuordnung beschrieben, in der die Beziehungen zwischen den Objektmodell Komponenten angezeigt werden.
  
## <a name="project-hosted-add-in-development-environment"></a>Projekt gehostete Add-in-Entwicklungsumgebung

Ein gehostetes Add-in ist ein Add-in, das sich auf dem Server befindet und zur Laufzeitausführung in einen Browser heruntergeladen wird. Gehostete Add-Ins können die JSOM-oder REST-Schnittstellen verwenden und in JavaScript geschrieben werden. Project Online stellt Verweise auf die JSOM-Bibliothek für die Laufzeitausführung bereit. Unter der Voraussetzung, dass die Entwicklung auf einer Windows-Plattform erfolgt, folgen die erforderlichen Ressourcen:
  
- Visual Studio 2015 (bevorzugt) oder Visual Studio 2013
    
- Office-Entwicklungstools für Visual Studio
    
- JavaScript-Sprache
    
Besuchen https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages Sie für eine Beispielanwendung. 
  
Sie können das Beispiel in wenigen einfachen Schritten herunterladen und ausführen:
  
1. Herunterladen und Öffnen der Beispielanwendung
    
2. Aktualisieren des SiteURL im Eigenschaftenfenster
    
   Project Online untersucht sowohl den Anwendungsbereich des Add-Ins als auch die Benutzerberechtigungen für den Zugriff auf Informationen auf dem Project Online-Host. Wenn der Zugriff explizit in einer oder beiden Einstellungen verweigert wird, verweigert Project Online den Zugriff auf die Informationen. Andernfalls wird der Zugriff gewährt.
    
3. Aktivieren Sie [querladen](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website.  
    
4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Projektanbieter-gehostete Add-in-Entwicklungsumgebung

Vom Anbieter gehostete Add-Ins sind Anwendungen, die auf einer beliebigen Webplattform geschrieben wurden. Sie können mithilfe der REST-API (oder CSOM für Microsoft-Plattformen) eine Verbindung herstellen und Datenvorgänge ausführen. Jede Sprache und Umgebung, die die REST-Schnittstelle unterstützt, kann für die Entwicklung verwendet werden. 
  
Ein Beispiel für die Windows-Entwicklungsumgebung für diesen Anwendungstyp umfasst die folgenden Elemente:
  
-  Visual Studio 2015 (bevorzugt) oder Visual Studio 2013 
    
- Microsoft Office-Entwicklungs Tools für Visual Studio (im Lieferumfang von Visual Studio 2015 Professional und Enterprise Edition)
    
- .NET Framework 4,0 oder höher
    
- [SHAREPOINTONLINE CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe) 
    
- Eine Programmiersprache wie C# 
    
Besuchen https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations Sie für funktionsfähige Beispielskripts. 
  
Sie können das Beispiel in wenigen Schritten ausführen:
  
1. Herunterladen und Öffnen der Beispielanwendung
    
2. Aktualisieren des SiteURL im Eigenschaftenfenster
    
   Project Online untersucht sowohl den Anwendungsbereich des Add-Ins als auch die Benutzerberechtigungen für den Zugriff auf Informationen auf dem Project Online-Host. Wenn der Zugriff explizit in einer oder beiden Einstellungen verweigert wird, verweigert Project Online den Zugriff auf die Informationen. Andernfalls wird der Zugriff gewährt.
    
3. Aktivieren Sie [querladen](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website. 
    
4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="externalstandalone-application-development-environment"></a>Entwicklungsumgebung für externe/eigenständige Anwendungen

Eine eigenständige Anwendung kann Project Online mithilfe des Client seitigen Objektmodells (CSOM) oder REST für die Kommunikation mit Project Online aufrufen, um Informationen auf dem Server zu erstellen, abzurufen, zu aktualisieren und zu löschen. Hierbei handelt es sich um eine eigenständige Clientanwendung, die von der Benutzerzugriffsebene abhängig ist. 
  
Ein Beispiel für die Windows-Entwicklungsumgebung für diesen Anwendungstyp umfasst die folgenden Elemente:
  
- Visual Studio 2015 (bevorzugt) oder Visual Studio 2013 
    
- Microsoft Office-Entwicklungs Tools für Visual Studio (im Lieferumfang von Visual Studio 2015 Professional und Enterprise Edition)
    
- .NET Framework 4,0 oder höher
    
- [SHAREPOINTONLINE CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe) 
    
- Eine Programmiersprache wie C# 
    
Besuchen https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields Sie für eine Beispielanwendung. 
  
Sie können das Beispiel in wenigen Schritten ausführen:
  
1. Herunterladen der Beispielanwendung
    
2. Führen Sie einige Änderungen aus, um auf Ihre Project Online-Website zuzugreifen: den Websitenamen, das Benutzerkonto und das Kennwort.
    
   Stellen Sie sicher, dass der Benutzer Zugriff auf alle Projekte hat. Project Online verwendet Benutzerberechtigungen, um den Zugriff auf Informationen im Datenspeicher zu steuern.
    
3. Fügen Sie die SharePoint-Assembly den verweisen mithilfe der Nuget-Paket-Manager-Konsole hinzu, die im Menü Extras verfügbar ist, indem Sie Folgendes in der Nuget-Konsole eingeben: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="next-steps"></a>Nächste Schritte

Jede Beispielanwendung enthält einen Artikel, in dem die Highlights der Arbeit mit der einzelnen Projekt-API erläutert werden. Die Artikel werden in der folgenden Liste zusammen mit einigen Artikeln angezeigt, in denen die Entitätsbeziehungen, Informationen zum Abfragesystem und der Zugriff auf benutzerdefinierte Felder beschrieben werden. 
  
- [Entwickeln einer Project Online-Anwendung mithilfe des Client seitigen Objektmodells](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Zugriff auf benutzerdefinierte Project Online-Unternehmensfelder](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/en-us/project).
    

