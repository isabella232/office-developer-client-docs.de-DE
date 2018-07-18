---
title: Von 0 auf 100 mit Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Anwendungsentwickler kann eine Project Online Site (SharePoint gehostet) mithilfe von eigenständigen Applications und/oder Projekt-add-ins anpassen. Eine Vielzahl von Clientanwendungen ist möglich, die im Bereich von Adressierung Beteiligten in einem Projekt auf PMO Support-Funktionen, beispielsweise eine der folgenden Anforderungen:'
ms.openlocfilehash: c50ed12e9f1127f6313a02db4d84a151778e17b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796171"
---
# <a name="from-0-to-60-with-project-online"></a>Von 0 auf 100 mit Project Online

Anwendungsentwickler kann eine Project Online Site (SharePoint gehostet) mithilfe von eigenständigen Applications und/oder Projekt-add-ins anpassen. Eine Vielzahl von Clientanwendungen ist möglich, die im Bereich von Adressierung Beteiligten in einem Projekt auf PMO Support-Funktionen, beispielsweise eine der folgenden Anforderungen:
  
- Optimierte Zeitkarte Dateneingabe für Mitarbeiter
- Effiziente Zeitkarte Genehmigung für Vorgesetzte
- Aufsicht über ermöglicht (Beschaffung und Status) für ein Projekt erforderlich ist
- Status/Überprüfung des aktiven Projekte
- Problembericht
- Ändern von Management Statusbericht
    
Project Online enthält die API-Unterstützung, um die folgenden Szenarien zu ermöglichen:
  
- Für ein Projekt (SharePoint) gehostet add-in:
    
  - Code (JavaScript, HTML, CSS), die in SharePoint Online gehostet wird
  - Anlagen, die in den Browser heruntergeladen und in SharePoint Online ausgeführt werden.  
  - Geschäftslogik in JavaScript   
  - Zugreifen auf Daten, die in/gespeichert in Project Online oder SharePoint wie (aber nicht beschränkt auf):  
  - Benutzerdefinierte Felder  
  - Listen
    
- Für ein Projekt (SharePoint) vom Anbieter gehosteten add-in:
    
  - Code, der auf einer Website, die außerhalb der Project Online-Website vorhanden ist 
  - Eine externe Website, die werden kann (jedoch nicht auf beschränkt ist):  
  - Anderen SharePoint-Website  
  - App/Webdienst integriert auf einer beliebigen Plattform  
  - Die externe Website enthält die Geschäftslogik  
  - Der Browser wird von Project Online an externe Website mit Zugriffstoken mit Project Online umgeleitet.  
  - Die externe Website kann Anrufe auf SharePoint und Project Online tätigen.
    
- Für eine externe/Standalone-add-in:
    
  - Benutzer führt eine Anwendung auf ihrem Gerät aus.
  - Anwendung authentifiziert und Project Online-APIs direkt anrufen
    

|Art der Anwendung|API-Implementierung|Zielumgebung|Beispiele für die Anwendung|
|:-----|:-----|:-----|:-----|
|Projekt gehostet  <br/> |JSOM (Java Script-Objektmodell)  <br/> REST  <br/> |Browser  <br/> |Zeitkarteneintrag  <br/> Zeitkarte Genehmigung  <br/> Projektstatus  <br/> Problembericht  <br/> |
|Project-Anbieter gehostet  <br/> |CSOM-Clientbibliothek  <br/> |Azure-Website-App  <br/> Nicht-Windows-Umgebung (LAMP usw.)  <br/> |Externe Arbeitszeittabelle validator  <br/> Projekt zu verwendenden Importprogramms  <br/> |
|Extern/eigenständige  <br/> |REST  <br/> CSOM  <br/> |REST - jeder Plattform  <br/> CSOM - jeder .NET unterstützten Plattform  <br/> |Zeitkarteneintrag  <br/> Migration von Projekten zu einem neuen Standort  <br/> Ändern Sie Verwaltungsstatus.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Was dauert es der Entwicklung von Anwendungen für Project Online beginnen?

Die gemeinsame Elemente für das Entwickeln von Project Online-Applikationen erforderlich sind ein Konto mit Project Online und Testdaten – Projekte und projektbezogenen Informationen, die Zuordnungen, Aufgaben, Ressourcen und benutzerdefinierte Felder enthalten. Eine Entwicklungsumgebung ist auch erforderlich, aber Einzelheiten der Development Environment hängt vom Typ der Anwendung und der API-Schnittstelle für die Anwendung erforderlich ist. Die nächsten Abschnitten werden die Entwicklung von Anforderungen für die drei API-Schnittstellen.
  
Referenzdokumentation für die beschreibt das Objektmodell, die für alle drei Schnittstellen als auch eine Entität-Zuordnung, die Beziehungen zwischen den Komponenten der Objekt-Modell anzeigt.
  
## <a name="project-hosted-add-in-development-environment"></a>Projekt-add-in-Entwicklungsumgebung gehostet

Eine gehostete-Add-in ist ein Add-in, die auf dem Server befindet und an einen Browser für die Ausführung zur Laufzeit heruntergeladen wird. Gehostete-add-ins können die JSOM oder REST-Schnittstelle und in JavaScript geschrieben. Project Online enthält Verweise auf die JSOM-Bibliothek für die Ausführung zur Laufzeit. Wird vorausgesetzt Entwicklung befindet sich in einer Windows-Plattform, die benötigten Ressourcen gehen Sie folgendermaßen vor:
  
- Visual Studio 2015 (empfohlen) oder Visual Studio 2013
    
- Office-Entwicklungstools für Visual Studio
    
- JavaScript-Sprache
    
Besuchen Sie https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages für eine beispielanwendung. 
  
Sie können herunterladen und Ausführen des Beispiels in ein paar einfachen Schritten:
  
1. Herunterladen Sie und öffnen Sie die beispielanwendung
    
2. Aktualisieren Sie das SiteURL im Fenster Eigenschaften
    
   Project Online untersucht sowohl die Anwendungsbereich des Add-Ins und die Berechtigungen eines Benutzers mit Zugriff auf Informationen auf dem Project Online-Host gesteuert. Wenn in einer oder beide Einstellungen explizit Zugriff verweigert wird, verweigert Project Online Zugriff auf Informationen. Andernfalls wird der Zugriff gewährt.
    
3. Sideloading auf Ihrer Website zu aktivieren. Finden Sie weitere Informationen im Artikel [Konfigurieren von Project Online für App-Entwicklung ](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx). 
    
4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Projekt-add-in Entwicklung vom Anbieter gehostete Umgebung

Vom Anbieter gehosteten-add-ins sind Applications geschrieben und auf allen Plattformen Web darstellen. Sie können eine Verbindung herstellen und Datenvorgänge mithilfe der REST (oder CSOM für Microsoft-Plattformen) API. Jede Sprache und die Umgebung, die die REST-Schnittstelle unterstützt können für die Entwicklung verwendet werden. 
  
Ein Beispiel für die Windows-Entwicklungsumgebung für diese Art Anwendung umfasst die folgenden Elemente:
  
-  Visual Studio 2015 (empfohlen) oder Visual Studio 2013 
    
- Microsoft Office-Entwicklungstools für Visual Studio (im Lieferumfang von Visual Studio 2015 Professional- und Enterprise Edition)
    
- .NET Framework 4.0 oder höher
    
- [SharePoint Online-CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx) (für CSOM-Aufrufe) 
    
- Eine Programmiersprache wie c# 
    
Besuchen Sie https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations für Beispielskripts arbeiten. 
  
Sie können das Beispiel in wenigen Schritten ausführen:
  
1. Herunterladen Sie und öffnen Sie die beispielanwendung
    
2. Aktualisieren Sie das SiteURL im Fenster Eigenschaften
    
   Project Online untersucht sowohl die Anwendungsbereich des Add-Ins und die Berechtigungen eines Benutzers mit Zugriff auf Informationen auf dem Project Online-Host gesteuert. Wenn in einer oder beide Einstellungen explizit Zugriff verweigert wird, verweigert Project Online Zugriff auf Informationen. Andernfalls wird der Zugriff gewährt.
    
3. Sideloading auf Ihrer Website zu aktivieren. Finden Sie weitere Informationen im Artikel [Konfigurieren von Project Online für App-Entwicklung ](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx). 
    
4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="externalstandalone-application-development-environment"></a>Extern/eigenständige Anwendung-Entwicklungsumgebung

Eine eigenständige Anwendung kann rufen Sie Project Online mit dem Client Side-Objekt Objektmodell (CSOM) oder REST kommunizieren mit Project Online erstellen, abrufen, aktualisieren und Löschen von Informationen, die sich auf dem Server befinden. Dies ist eine eigenständige-Clientanwendung, die Zugriff auf Benutzerebene ausgeführt abhängig ist. 
  
Ein Beispiel für die Windows-Entwicklungsumgebung für diese Art Anwendung umfasst die folgenden Elemente:
  
- Visual Studio 2015 (empfohlen) oder Visual Studio 2013 
    
- Microsoft Office-Entwicklungstools für Visual Studio (im Lieferumfang von Visual Studio 2015 Professional- und Enterprise Edition)
    
- .NET Framework 4.0 oder höher
    
- [SharePoint Online-CSOM-Paket](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx) (für CSOM-Aufrufe) 
    
- Eine Programmiersprache wie c# 
    
Besuchen Sie https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields für eine beispielanwendung. 
  
Sie können das Beispiel in wenigen Schritten ausführen:
  
1. Laden Sie die beispielanwendung aus
    
2. Stellen Sie eine Reihe von Änderungen an Ihrer Project Online-Website zugreifen – den Namen des Standorts, Benutzerkonto und Kennwort.
    
   Stellen Sie sicher, dass der Benutzer Zugriff auf alle Projekte. Project Online verwendet Benutzerberechtigungen zum Zugriff auf Informationen im Datenspeicher steuern.
    
3. Fügen Sie die Verweise mit der Nuget Package Manager-Konsole zur Verfügung, indem Sie Folgendes in der Konsole Nuget eingeben im Menü Extras die SharePoint-Assembly hinzu: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Erstellen Sie das Projekt.
    
5. Führen Sie das Projekt aus.
    
## <a name="next-steps"></a>Nächste Schritte

Jede beispielanwendung verfügt über einen Artikel erläutern die wichtigsten arbeiten mit der einzelnen Project-API. Die Artikel in der folgenden Liste zusammen mit ein paar Artikeln, die entitätsbeziehungen Informationen zu den Abfragesystem und den Zugriff auf benutzerdefinierte Felder angezeigt werden. 
  
- [Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Entwickeln eines Project Online add-Ins mithilfe der JavaScript-Objektmodell (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Zugriff auf benutzerdefinierte Project Online-Unternehmensfelder](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele im Zusammenhang mit Project Online und die Anwendungsentwicklung mithilfe von CSOM finden Sie im [Projekt Development Portal](http://dev.office.com/project.aspx).
    

