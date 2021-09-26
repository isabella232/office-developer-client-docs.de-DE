---
title: Von 0 auf 100 mit Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Ein Anwendungsentwickler kann eine Project Online Website (SharePoint gehostet) mit eigenständigen Anwendungen und/oder Project-Add-Ins anpassen. Es ist eine Vielzahl von Anwendungen möglich, die von der Erfüllung der Anforderungen der an einem Projekt beteiligten Personen bis hin zu PMO-Supportfunktionen reichen, z. B. eine der folgenden:'
ms.openlocfilehash: 3ea7c451022c3c7b55d1ce788b002df6bb8bb591
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619239"
---
# <a name="from-0-to-60-with-project-online"></a>Von 0 auf 100 mit Project Online

Ein Anwendungsentwickler kann eine Project Online Website (SharePoint gehostet) mit eigenständigen Anwendungen und/oder Project-Add-Ins anpassen. Es ist eine Vielzahl von Anwendungen möglich, die von der Erfüllung der Anforderungen der an einem Projekt beteiligten Personen bis hin zu PMO-Supportfunktionen reichen, z. B. eine der folgenden:
  
- Optimierte Zeitcarddateneingabe für Mitarbeiter
- Effiziente Genehmigung von Zeitkarten für Vorgesetzte
- Überwachung der für ein Projekt erforderlichen Genehmigungen (Beschaffung und Status)
- Status-/Integritätsprüfung aktiver Projekte
- Problembericht
- Änderungsverwaltungsstatusbericht
    
Project Online bietet API-Unterstützung für die folgenden Szenarien:
  
- Für ein Project (SharePoint) gehostetes Add-In:
    
  - Code (JavaScript, HTML, CSS), der in SharePoint Online gehostet wird
  - Ressourcen, die in den Browser heruntergeladen und für SharePoint Online ausgeführt werden.  
  - Geschäftslogik in JavaScript   
  - Zugreifen auf Daten, die in Project Online oder SharePoint gespeichert sind, z. B. (aber nicht beschränkt auf):  
  - Benutzerdefinierte Felder  
  - Listen
    
- Für ein vom Anbieter gehostetes Project-Add-In (SharePoint):
    
  - Code, der auf einer Website außerhalb der Project Online-Website vorhanden ist 
  - Eine externe Website, die sein kann (aber nicht beschränkt auf):  
  - Eine weitere SharePoint Website  
  - Web App/Service, die auf einer beliebigen Plattform basiert  
  - Die externe Website enthält Geschäftslogik.  
  - Der Browser wird von Project Online zu einer externen Website umgeleitet, mit Zugriffstoken an Project Online  
  - Die externe Website kann Aufrufe an SharePoint und Project Online
    
- Für ein externes/eigenständiges Add-In:
    
  - Der Benutzer führt eine Anwendung auf dem Gerät aus.
  - Anwendung authentifiziert sich und ruft Project Online APIs direkt auf
    

|Art der Anwendung|API-Implementierung|Zielumgebung|Anwendungsbeispiele|
|:-----|:-----|:-----|:-----|
|Project gehostet  <br/> |JSOM (Java Script-Objektmodell)  <br/> REST  <br/> |Browser  <br/> |Timecardeintrag  <br/> Timecard-Genehmigung  <br/> Project Status  <br/> Problembericht  <br/> |
|Project Vom Anbieter gehostet  <br/> |CSOM-Clientbibliothek  <br/> |Azure-Website/-App  <br/> Nicht Windows Umgebung (LAMP usw.)  <br/> |Externer Arbeitszeittabellenprüfer  <br/> Project Importeur  <br/> |
|Extern/Eigenständig  <br/> |REST  <br/> CSOM  <br/> |REST – eine beliebige Plattform  <br/> CSOM – jede von .NET unterstützte Plattform  <br/> |Timecardeintrag  <br/> Migration von Projekten zu einer neuen Website  <br/> Änderungsverwaltungsstatus.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Was dauert es, um mit der Entwicklung von Anwendungen für Project Online zu beginnen?

Die allgemeinen Elemente, die für die Entwicklung Project Online Anwendungen erforderlich sind, sind ein Project Online Konto und Testdatenprojekte und projektbezogene Informationen, die Zuordnungen, Aufgaben, Ressourcen und benutzerdefinierte Felder umfassen. Eine Entwicklungsumgebung ist auch erforderlich, aber die Einzelheiten der Entwicklungsumgebung hängen vom Anwendungstyp und der FÜR die Anwendung benötigten API-Schnittstelle ab. In den nächsten Abschnitten werden die Entwicklungsanforderungen für die drei API-Schnittstellen beschrieben.
  
In der Referenzdokumentation wird das objektmodell beschrieben, das für alle drei Schnittstellen verwendet wird, sowie eine Entitätszuordnung, die Beziehungen zwischen den Objektmodellkomponenten anzeigt.
  
## <a name="project-hosted-add-in-development-environment"></a>Project gehostete Add-In-Entwicklungsumgebung

Ein gehostetes Add-In ist ein Add-In, das sich auf dem Server befindet und zur Laufzeit in einen Browser heruntergeladen wird. Gehostete Add-Ins können die JSOM- oder REST-Schnittstellen verwenden und werden in JavaScript geschrieben. Project Online stellt Verweise auf die JSOM-Bibliothek für die Ausführung zur Laufzeit bereit. Wenn die Entwicklung auf einer Windows Plattform erfolgt, folgen die erforderlichen Ressourcen:
  
- Visual Studio 2015 (bevorzugt) oder Visual Studio 2013
    
- Office Entwicklungstools für Visual Studio
    
- JavaScript-Sprache
    
Besuchen Sie https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages eine Beispielanwendung. 
  
Sie können das Beispiel in wenigen einfachen Schritten herunterladen und ausführen:
  
1. Herunterladen und Öffnen der Beispielanwendung
    
2. Aktualisieren der SiteURL im Eigenschaftenfenster
    
   Project Online untersucht sowohl den Anwendungsumfang des Add-Ins als auch die Benutzerberechtigungen, um den Zugriff auf Informationen auf dem Project Online Host zu steuern. Wenn der Zugriff in einer oder beiden Einstellungen explizit verweigert wird, verweigert Project Online den Zugriff auf die Informationen. Andernfalls wird Zugriff gewährt.
    
3. Aktivieren Sie [das Querladen](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website.  
    
4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Project vom Anbieter gehosteten Add-In-Entwicklungsumgebung

Vom Anbieter gehostete Add-Ins sind Anwendungen, die auf einer beliebigen Webplattform geschrieben und gespeichert sind. Sie können Datenvorgänge mithilfe der REST-API (oder CSOM für Microsoft-Plattformen) verbinden und ausführen. Jede Sprache und Umgebung, die die REST-Schnittstelle unterstützt, kann für die Entwicklung verwendet werden. 
  
Ein Beispiel für die Windows Entwicklungsumgebung für diesen Anwendungstyp umfasst die folgenden Elemente:
  
-  Visual Studio 2015 (bevorzugt) oder Visual Studio 2013 
    
- Microsoft Office Entwicklungstools für Visual Studio (bereitgestellt mit Visual Studio 2015-Professional- und Enterprise-Editionen)
    
- .NET Framework 4.0 oder höher
    
- [SharePointOnline-CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe) 
    
- Eine Programmiersprache, z. B. C # 
    
Besuchen Sie https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations die Arbeitsbeispielskripts. 
  
Sie können das Beispiel in wenigen Schritten ausführen:
  
1. Herunterladen und Öffnen der Beispielanwendung
    
2. Aktualisieren der SiteURL im Eigenschaftenfenster
    
   Project Online untersucht sowohl den Anwendungsumfang des Add-Ins als auch die Benutzerberechtigungen, um den Zugriff auf Informationen auf dem Project Online Host zu steuern. Wenn der Zugriff in einer oder beiden Einstellungen explizit verweigert wird, verweigert Project Online den Zugriff auf die Informationen. Andernfalls wird Zugriff gewährt.
    
3. Aktivieren Sie [das Querladen](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website. 
    
4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="externalstandalone-application-development-environment"></a>Externe/eigenständige Anwendungsentwicklungsumgebung

Eine eigenständige Anwendung kann Project Online mithilfe des clientseitigen Objektmodells (CSOM) oder REST aufrufen, um mit Project Online zu kommunizieren, um Informationen zu erstellen, abzurufen, zu aktualisieren und zu löschen, die sich auf dem Server befinden. Dies ist eine eigenständige Clientanwendung, die von der auszuführenden Benutzerzugriffsebene abhängt. 
  
Ein Beispiel für die Windows Entwicklungsumgebung für diesen Anwendungstyp umfasst die folgenden Elemente:
  
- Visual Studio 2015 (bevorzugt) oder Visual Studio 2013 
    
- Microsoft Office Entwicklungstools für Visual Studio (bereitgestellt mit Visual Studio 2015-Professional- und Enterprise-Editionen)
    
- .NET Framework 4.0 oder höher
    
- [SharePointOnline-CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe) 
    
- Eine Programmiersprache, z. B. C # 
    
Besuchen Sie https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields eine Beispielanwendung. 
  
Sie können das Beispiel in wenigen Schritten ausführen:
  
1. Herunterladen der Beispielanwendung
    
2. Nehmen Sie einige Änderungen vor, um auf Ihre Project Online Website zuzugreifen– den Websitenamen, das Benutzerkonto und das Kennwort.
    
   Stellen Sie sicher, dass der Benutzer Zugriff auf alle Projekte hat. Project Online verwendet Benutzerberechtigungen, um den Zugriff auf Informationen im Datenspeicher zu steuern.
    
3. Fügen Sie die SharePoint-Assembly den Verweisen mithilfe der Nuget Paket-Manager-Konsole hinzu, die im Menü "Extras" verfügbar ist, indem Sie Folgendes in der Nuget-Konsole eingeben: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="next-steps"></a>Nächste Schritte

Jede Beispielanwendung enthält einen Artikel, in dem die Highlights der Arbeit mit der einzelnen Project-API erläutert werden. Die Artikel werden in der folgenden Liste zusammen mit einigen Artikeln angezeigt, die die Entitätsbeziehungen, Informationen zum Abfragesystem und den Zugriff auf benutzerdefinierte Felder beschreiben. 
  
- [Entwickeln einer Project Online-Anwendung mithilfe des clientseitigen Objektmodells](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Zugriff auf benutzerdefinierte Project Online-Unternehmensfelder](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/en-us/project).
    

