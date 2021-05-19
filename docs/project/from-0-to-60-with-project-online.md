---
title: Von 0 auf 100 mit Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Ein Anwendungsentwickler kann eine Project Online (SharePoint gehostet) mithilfe von eigenständigen Anwendungen und/oder Project-Add-Ins anpassen. Es ist eine Vielzahl von Anwendungen möglich, die von der Behandlung der Anforderungen der an einem Projekt beteiligten Personen bis hin zu PMO-Supportfunktionen reichen, z. B. eine der folgenden:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344408"
---
# <a name="from-0-to-60-with-project-online"></a>Von 0 auf 100 mit Project Online

Ein Anwendungsentwickler kann eine Project Online (SharePoint gehostet) mithilfe von eigenständigen Anwendungen und/oder Project-Add-Ins anpassen. Es ist eine Vielzahl von Anwendungen möglich, die von der Behandlung der Anforderungen der an einem Projekt beteiligten Personen bis hin zu PMO-Supportfunktionen reichen, z. B. eine der folgenden:
  
- Optimierte Zeitkartendateneingabe für Mitarbeiter
- Effiziente Genehmigung von Zeitkarten für Vorgesetzte
- Aufsicht über Genehmigungen (Beschaffung und Status), die für ein Projekt erforderlich sind
- Status-/Integritätsprüfung aktiver Projekte
- Problembericht
- Bericht zum Änderungsverwaltungsstatus
    
Project Online umfasst DIE-API-Unterstützung für die folgenden Szenarien:
  
- Für ein Project (SharePoint) gehostetes Add-In:
    
  - Code (JavaScript, HTML, CSS), der in SharePoint Online gehostet wird
  - Objekte, die in den Browser heruntergeladen und für SharePoint Online ausgeführt werden.  
  - Geschäftslogik in JavaScript   
  - Zugriff auf Daten, die in Project Online oder SharePoint gespeichert sind(aber nicht beschränkt auf):  
  - Benutzerdefinierte Felder  
  - Listen
    
- Für ein Project (SharePoint) vom Anbieter gehostetes Add-In:
    
  - Code, der auf einer Website außerhalb der Website Project Online ist 
  - Eine externe Website, die (aber nicht beschränkt auf) sein kann:  
  - Eine andere SharePoint Website  
  - Web App/Service auf einer beliebigen Plattform  
  - Die externe Website enthält Geschäftslogik  
  - Der Browser wird von Project Online zu einer externen Website mit Zugriffstoken zu Project Online  
  - Die externe Website kann Anrufe an SharePoint und Project Online
    
- Für ein externes/eigenständiges Add-In:
    
  - Benutzer führt eine Anwendung auf ihrem Gerät aus
  - Anwendung authentifiziert und ruft Project Online APIs direkt auf
    

|Art der Anwendung|API-Implementierung|Zielumgebung|Anwendungsbeispiele|
|:-----|:-----|:-----|:-----|
|Project gehostet  <br/> |JSOM (Java Script Object Model)  <br/> REST  <br/> |Browser  <br/> |Zeitkarteneintrag  <br/> Genehmigung von Zeitkarten  <br/> Project Status  <br/> Problembericht  <br/> |
|Project Anbieter gehostet  <br/> |CSOM-Clientbibliothek  <br/> |Azure-Website/App  <br/> Nicht Windows Umgebung (LAMP usw.)  <br/> |Externer Arbeitszeittabellen-Validator  <br/> Project Importer  <br/> |
|Extern/Eigenständig  <br/> |REST  <br/> CSOM  <br/> |REST – beliebige Plattform  <br/> CSOM – jede von .NET unterstützte Plattform  <br/> |Zeitkarteneintrag  <br/> Migration von Projekten zu einer neuen Website  <br/> Änderungsverwaltungsstatus.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Was dauert es, um mit der Entwicklung von Anwendungen für Project Online?

Die allgemeinen Elemente, die für die Entwicklung von Project Online-Anwendungen benötigt werden, sind ein Project Online-Konto und Testdaten – Projekte und projektbezogene Informationen, die Zuordnungen, Vorgänge, Ressourcen und benutzerdefinierte Felder enthalten. Es ist auch eine Entwicklungsumgebung erforderlich, aber die Spezifischen der Entwicklungsumgebung hängen vom Anwendungstyp und der api-Schnittstelle ab, die für die Anwendung erforderlich sind. In den nächsten Abschnitten werden die Entwicklungsanforderungen für die drei API-Schnittstellen beschrieben.
  
In der Referenzdokumentation wird das Objektmodell beschrieben, das für alle drei Schnittstellen üblich ist, sowie eine Entitätszuordnung, die Beziehungen zwischen den Objektmodellkomponenten zeigt.
  
## <a name="project-hosted-add-in-development-environment"></a>Project gehostete Add-In-Entwicklungsumgebung

Ein gehostetes Add-In ist ein Add-In, das sich auf dem Server befindet und zur Laufzeitausführung in einen Browser heruntergeladen wird. Gehostete Add-Ins können die JSOM- oder REST-Schnittstellen verwenden und werden in JavaScript geschrieben. Project Online stellt Verweise auf die JSOM-Bibliothek zur Laufzeitausführung zur Verfügung. Wenn die Entwicklung auf einer Windows ist, folgen die benötigten Ressourcen:
  
- Visual Studio 2015 (bevorzugt) oder Visual Studio 2013
    
- Office Entwicklungstools für Visual Studio
    
- JavaScript-Sprache
    
Besuchen https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages Sie eine Beispielanwendung. 
  
Sie können das Beispiel in einigen einfachen Schritten herunterladen und ausführen:
  
1. Herunterladen und Öffnen der Beispielanwendung
    
2. Aktualisieren von SiteURL im Eigenschaftenfenster
    
   Project Online untersucht sowohl den Anwendungsbereich des Add-Ins als auch die Benutzerberechtigungen zum Steuern des Zugriffs auf Informationen auf dem Project Online Host. Wenn der Zugriff in einer oder beiden Einstellungen explizit verweigert wird, Project Online zugriff auf die Informationen verweigert. Andernfalls wird Der Zugriff gewährt.
    
3. Aktivieren [sie das Querladen](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website.  
    
4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Project vom Anbieter gehostete Add-In-Entwicklungsumgebung

Vom Anbieter gehostete Add-Ins sind Anwendungen, die auf jeder Beliebigen Webplattform geschrieben und dort ansässig sind. Sie können Datenvorgänge mithilfe der REST-API (oder CSOM für Microsoft-Plattformen) verbinden und ausführen. Jede Sprache und Umgebung, die die REST-Schnittstelle unterstützt, kann für die Entwicklung verwendet werden. 
  
Ein Beispiel für die Windows für diesen Anwendungstyp enthält die folgenden Elemente:
  
-  Visual Studio 2015 (bevorzugt) oder Visual Studio 2013 
    
- Microsoft Office Entwicklungstools für Visual Studio (im Lieferumfang Visual Studio 2015 Professional und Enterprise Editionen)
    
- .NET Framework 4.0 oder neuer
    
- [SharePointOnline-CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe) 
    
- Eine Programmiersprache, z. B. C # 
    
Besuchen https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations Sie zum Arbeiten von Beispielskripts. 
  
Sie können das Beispiel in einigen Schritten ausführen:
  
1. Herunterladen und Öffnen der Beispielanwendung
    
2. Aktualisieren von SiteURL im Eigenschaftenfenster
    
   Project Online untersucht sowohl den Anwendungsbereich des Add-Ins als auch die Benutzerberechtigungen zum Steuern des Zugriffs auf Informationen auf dem Project Online Host. Wenn der Zugriff in einer oder beiden Einstellungen explizit verweigert wird, Project Online zugriff auf die Informationen verweigert. Andernfalls wird Der Zugriff gewährt.
    
3. Aktivieren [sie das Querladen](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) auf Ihrer Website. 
    
4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="externalstandalone-application-development-environment"></a>Externe/eigenständige Anwendungsentwicklungsumgebung

Eine eigenständige Anwendung kann Project Online Client Side Object Model (CSOM) oder REST aufrufen, um mit Project Online zu kommunizieren, um Informationen zu erstellen, abzurufen, zu aktualisieren und zu löschen, die sich auf dem Server befinden. Dies ist eine eigenständige Clientanwendung, die von der benutzerzugriffsebene abhängt, die ausgeführt werden soll. 
  
Ein Beispiel für die Windows für diesen Anwendungstyp enthält die folgenden Elemente:
  
- Visual Studio 2015 (bevorzugt) oder Visual Studio 2013 
    
- Microsoft Office Entwicklungstools für Visual Studio (im Lieferumfang Visual Studio 2015 Professional und Enterprise Editionen)
    
- .NET Framework 4.0 oder neuer
    
- [SharePointOnline-CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (für CSOM-Aufrufe) 
    
- Eine Programmiersprache, z. B. C # 
    
Besuchen https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields Sie eine Beispielanwendung. 
  
Sie können das Beispiel in einigen Schritten ausführen:
  
1. Herunterladen der Beispielanwendung
    
2. Nehmen Sie einige Änderungen vor, um auf Ihre Project Online zu zugreifen– den Websitenamen, das Benutzerkonto und das Kennwort.
    
   Stellen Sie sicher, dass der Benutzer Zugriff auf alle Projekte hat. Project Online verwendet Benutzerberechtigungen, um den Zugriff auf Informationen im Datenspeicher zu steuern.
    
3. Fügen Sie die SharePoint-Assembly mithilfe der Nuget-Paket-Manager-Konsole hinzu, die im Menü Extras verfügbar ist, indem Sie in der Nuget-Konsole Folgendes eingeben: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="next-steps"></a>Nächste Schritte

Jede Beispielanwendung enthält einen Artikel, in dem die Highlights der Arbeit mit der einzelnen Project werden. Die Artikel werden in der folgenden Liste zusammen mit einigen Artikeln angezeigt, in denen die Entitätsbeziehungen, Informationen zum Abfragesystem und der Zugriff auf benutzerdefinierte Felder beschrieben werden. 
  
- [Entwickeln einer Project Online-Anwendung mithilfe des clientseitigen Objektmodells](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Zugriff auf benutzerdefinierte Project Online-Unternehmensfelder](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/en-us/project).
    

