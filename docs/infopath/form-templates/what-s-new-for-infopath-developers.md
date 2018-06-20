---
title: Neuigkeiten für InfoPath-Entwickler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Neuigkeiten für Entwickler neue [Infopath 2007] [InfoPath 2007] InfoPath 2007, Neuigkeiten features, neue features [InfoPath 2007]
localization_priority: Normal
ms.assetid: d0ad3111-bd41-4f35-8a34-62c17f20fc19
description: InfoPath ist darauf ausgelegt, die umfangreiche formularbasierte Anwendungen auf der Microsoft SharePoint Server-Plattform erstellen erleichtern. Microsoft InfoPath 2013 in Verbindung mit Microsoft SharePoint Server 2013 und InfoPath Forms Services haben viele Funktionen für Entwickler. InfoPath Forms Services in SharePoint Server 2013 verfügbar ist, können Sie eine InfoPath-Formularvorlage in einer SharePoint-Server bereitstellen, damit Benutzer ohne die InfoPath-rich-Client öffnen und InfoPath-Formulare in einem Webbrowser ausfüllen können.
ms.openlocfilehash: a11c6b4018e60a470197ecd7ffdf3b79a13658b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790846"
---
# <a name="whats-new-for-infopath-developers"></a>Neuigkeiten für InfoPath-Entwickler

InfoPath ist darauf ausgelegt, die umfangreiche formularbasierte Anwendungen auf der Microsoft SharePoint Server-Plattform erstellen erleichtern. Microsoft InfoPath 2013 in Verbindung mit Microsoft SharePoint Server 2013 und InfoPath Forms Services haben viele Funktionen für Entwickler. InfoPath Forms Services in SharePoint Server 2013 verfügbar ist, können Sie eine InfoPath-Formularvorlage in einer SharePoint-Server bereitstellen, damit Benutzer ohne die InfoPath-rich-Client öffnen und InfoPath-Formulare in einem Webbrowser ausfüllen können.
  
Formularvorlagen, die mithilfe von InfoPath 2013 erstellt weiterhin unterstützen die Klassen und Member des **Microsoft.Office.InfoPath** -Namespace, der funktioniert die gleiche Weise wie für ein Formular in InfoPath Filler oder in einem Formular in einem Web geöffnet geöffnet verfasste Geschäftslogik Browser. Mithilfe dieser verwalteten Objektmodell geschriebene Geschäftslogik von und Arbeiten mit Design Features im InfoPath-Designer zu überprüfen können Sie eine einzelne Formularvorlage erstellen, die Sie in einer entsprechend konfigurierten Dokumentbibliothek auf SharePoint Server 2013 bereitstellen können, die in beiden InfoPath Filler und in einem Webbrowser ausgeführt werden soll. 
  
## <a name="new-features-and-improvements"></a>Neue Features und Verbesserungen

In den folgenden Abschnitten werden diese Features und Verbesserungen, die InfoPath-Entwickler interessant sind die kurz beschrieben:
  
- Neue Möglichkeiten beim Schreiben und Bearbeiten von Code
    
- SharePoint-Sandkastenlösungen
    
- Veröffentlichen von Formularen mit einem Klick
    
- Optimieren von SharePoint-Listenformularen
    
- Hosten von Formularen auf Portalseiten mithilfe des InfoPath-Formular-Webparts
    
- Webformulare mit umfangreicher Funktionalität
    
- Standardkonforme Browserformulare
    
- Bessere Informationssicherheit und Integrität mit digitalen Signaturen
    
- Neue Steuerelemente
    
## <a name="new-way-to-write-and-edit-code"></a>Neue Möglichkeiten beim Schreiben und Bearbeiten von Code

Microsoft Visual Studio Tools for Applications-IDE, die in InfoPath 2010 integriert wurde wurde in InfoPath 2013 entfernt. Zum Schreiben oder Bearbeitungsformular erfordert Code in InfoPath 2013 Visual Studio 2012 jetzt mit dem [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) Add-on installiert. Der Erfahrung im Programmieren selbst nicht grundlegend geändert hat, aber nun können Sie die vollständige Visual Studio-Entwicklung beim Schreiben von verwaltetem Code für InfoPath-Formulare. 
  
In den folgenden Abschnitten wird beschrieben, Features, die zuerst in InfoPath 2010 und SharePoint Server 2010 hinzugefügt wurden und weiterhin, Mehrwert für Entwickler von InfoPath 2013 und SharePoint Server 2013.
  
## <a name="sharepoint-server-sandboxed-solutions"></a>SharePoint Server-Sandkastenlösungen

Mit InfoPath ist es einfacher denn je auf auf SharePoint Server 2013-Formularen mit Code bereitstellen. In Office InfoPath 2007 mussten alle Formulare mit Code von einem SharePoint-Farmadministrator hochgeladen und genehmigt werden. Mit der Unterstützung für sandkastenlösungen in SharePoint Server 2013 können Formulardesigner, die Berechtigungen der Websitesammlung Verwaltung haben jetzt die meisten Formularen mit Code, direkt auf die SharePoint-Websites veröffentlichen. Eine Ressource Kontingent Einstellung auf dem Server beschränkt übermäßiger Ressourceneinsatz. Der Administrator der Websitesammlung im Steuerelement bleibt und macht Vertrauensstellung Entscheidungen im Hinblick auf die Lösung. Der Farmadministrator kann automatische sein. Weitere Informationen zum Veröffentlichen von InfoPath-Formularvorlagen als sandkastenlösungen finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md).
  
## <a name="publish-forms-with-one-click"></a>Veröffentlichen von Formularen mit einem Klick

InfoPath ist darauf ausgelegt, um als jemals zum Veröffentlichen von aktualisierten von Formularen zu vereinfachen. Nach der ersten, die Sie eine Formularvorlage veröffentlichen, anstatt über mehrere Dialogfelder, können Sie Abschließen dieser Aufgabe mit nur einem Mausklick von der neuen Schaltfläche **Schnell veröffentlichen** , klicken Sie auf der **Symbolleiste für den Schnellzugriff**und in der neuen verfügbar ist Microsoft Office Backstage, die zur Verfügung steht, indem Sie auf der Registerkarte **Datei** . 
  
## <a name="enhance-sharepoint-list-forms"></a>Optimieren von SharePoint-Listenformularen

Mithilfe von InfoPath, können Sie jetzt erweitert und verbessert die Formulare zum Erstellen, bearbeiten und Anzeigen von Elementen in einer SharePoint-Liste verwendet. Öffnen einer Liste und dann auf **Formular anpassen**auf der Registerkarte **Liste** unter **Listentools**, können Sie automatisch generieren eines InfoPath-Formulars die Standardeinstellung ähnelt, Out-of-Box-SharePoint-Listenformular. Sie können dann anpassen und Erweitern dieses Formulars durch Bearbeiten des Layouts, zusätzliche Ansichten erstellen und Hinzufügen von Regeln und die datenüberprüfung in InfoPath. Wenn Sie ändern die verbesserte Listenformular abgeschlossen haben, können Sie ihn veröffentlichen in SharePoint mithilfe der neuen Mausklick Feature in InfoPath veröffentlichen.
  
## <a name="host-forms-on-portal-pages-using-the-infopath-form-web-part"></a>Hosten von Formularen auf Portalseiten mithilfe des InfoPath-Formular-Webparts

In SharePoint Server 2013 ist es einfacher denn je zum Hosten von Formularen auf Webseiten mithilfe des neuen **InfoPath-Webpart**. In Microsoft Office SharePoint Server 2007 können Benutzer, die ihre InfoPath-Formularen auf Webseiten hosten soll zum Schreiben von Code in Visual Studio. Nun können Sie ohne eine einzige Codezeile schreiben, den **InfoPath-Webpart** auf einer Webpartseite hinzufügen und verweisen sie auf Ihr veröffentlichtes Formular. Das **InfoPath-Webpart** können Sie alle InfoPath-Browser-Formular hosten, die in einer SharePoint-Liste oder Bibliothek veröffentlicht wird. Sie können auch verbinden ihn mit anderen Webparts auf der Seite senden oder Empfangen von Daten. Weitere Informationen dazu, wie Sie den **InfoPath-Webpart**verwenden finden Sie unter [Arbeiten mit dem InfoPath-Formularwebpart](http://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx) in SharePoint 2010 SDK. 
  
## <a name="richer-web-forms"></a>Webformulare mit umfangreicher Funktionalität

Die Lücke zwischen den Features für Client- und Browserformulare schließt sich weiter. Das heißt, das Ausfüllen von Formularen wurde für alle Benutzer konsistenter gestaltet. Beispiele für Steuerelemente und Funktionen, die jetzt in Browserformularen unterstützt werden:
  
- Aufzählungen, nummerierte Listen und einfache Listen
    
- Listenfelder mit Mehrfachauswahl
    
- Kombinationsfelder
    
- Bildschaltflächen
    
- Linkfunktionalität
    
- Auswahlgruppe und -abschnitt 
    
- Datums- und Uhrzeitsteuerelemente
    
- Personen-/Gruppenauswahl
    
- Filterfunktionalität
    
## <a name="standards-compliant-browser-forms"></a>Standardkonforme Browserformulare

InfoPath-Browser-Formulare sind jetzt kompatibel mit Web Content Accessibility Guidelines 2.0 (WCAG 2.0) AA, wodurch Formular-Designer zum Erstellen von Formularen, die für Benutzer mit behinderungen verfügbar sind.
  
## <a name="provide-enhanced-information-security-and-integrity-with-digital-signatures"></a>Bessere Informationssicherheit und Integrität mit digitalen Signaturen

InfoPath unterstützt die nächste Generation CNG (Cryptography) digital signierten Inhalt. Um Ihnen die Integrität der Informationen beitragen, der in Formularen enthalten ist, geben Sie die InfoPath-Client und SharePoint Server 2013 die Steuerelemente, die erforderlich sind, um einzelne aktivieren, gemeinsame melden Sie sich, und gegen den Szenarien für das vollständige Formular oder der Abschnitte des Formulars. Formulare können in Internet Explorer mithilfe des Signaturzeilen ActiveX-Steuerelements signiert werden. Signierte Formulare können in jeder von SharePoint Server 2013 unterstützten Browser angezeigt werden.
  
## <a name="new-controls"></a>Neue Steuerelemente

InfoPath bietet eine umfassende Reihe von Steuerelementen, die von Formularen hinzugefügt werden können. Die folgende Liste beschreibt kurz einige der neuen Steuerelemente:
  
- **Bildschaltfläche** – anstelle einer grauen Rechtecks können; Verwenden Sie ein Bild als Schaltfläche im Formular. 
    
- **Hyperlink** – Benutzer eingeben eigener Hyperlinks beim Ausfüllen von Formularen aktivieren. 
    
- **Personen-/Gruppenauswahl** – Benutzer überprüfen und Abfragen von Kontonamen und Gruppen beim Ausfüllen von Formularen aktivieren. 
    
- **Entitätsauswahl** – aktivieren Sie Benutzer auswählen von Werten aus externen Listen auf einem Server mit der SharePoint Server 2013 bei Formularen. 
    
- **Signaturzeile** – bieten den Benutzern beim digitalen Signieren von Formularen mit einer Signaturzeile oder Signaturbild, beispielsweise ein inkan- oder Hanko-Siegel. 
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von InfoPath-Formularvorlagen mit Code](developing-infopath-form-templates-with-code.md)
  
[Entwickeln von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](developing-form-templates-using-the-infopath-2003-object-model.md)

