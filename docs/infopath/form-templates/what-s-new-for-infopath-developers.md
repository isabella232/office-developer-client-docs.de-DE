---
title: Neuerungen für InfoPath-Entwickler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Neuigkeiten [Infopath 2007],Entwicklerfeatures [InfoPath 2007],InfoPath 2007, Neuigkeiten,neue Features [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: d0ad3111-bd41-4f35-8a34-62c17f20fc19
description: InfoPath wurde entwickelt, um die Erstellung reichhaltiger, formularbasierter Anwendungen auf der Plattform Microsoft SharePoint Server zu vereinfachen. Microsoft InfoPath 2013 in Verbindung mit Microsoft SharePoint Server 2013 und InfoPath Forms Services bieten zahlreiche Features für Entwickler. Mit InfoPath Forms Services, verfügbar in SharePoint Server 2013, können Sie eine InfoPath-Formularvorlage auf einem SharePoint-Server bereitstellen, damit Benutzer ohne InfoPath Rich Client InfoPath-Formulare in einem Webbrowser öffnen und ausfüllen können.
ms.openlocfilehash: 61bbf2deba2ccaa91873e83c80f0d8385d97dd41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614514"
---
# <a name="whats-new-for-infopath-developers"></a>Neuerungen für InfoPath-Entwickler

InfoPath wurde entwickelt, um die Erstellung reichhaltiger, formularbasierter Anwendungen auf der Plattform Microsoft SharePoint Server zu vereinfachen. Microsoft InfoPath 2013 in Verbindung mit Microsoft SharePoint Server 2013 und InfoPath Forms Services bieten zahlreiche Features für Entwickler. Mit InfoPath Forms Services, verfügbar in SharePoint Server 2013, können Sie eine InfoPath-Formularvorlage auf einem SharePoint-Server bereitstellen, damit Benutzer ohne InfoPath Rich Client InfoPath-Formulare in einem Webbrowser öffnen und ausfüllen können.
  
Mit InfoPath 2013 erstellte Formularvorlagen unterstützen weiterhin für die Klassen und Elemente des **Microsoft.Office.InfoPath**-Namespace geschriebene Geschäftslogik, die auf identische Weise für Formulare funktioniert, die in InfoPath Filler und in einem Webbrowser geöffnet werden. Durch Verwenden von Geschäftslogik, die für dieses verwaltete Objektmodell geschrieben wurde, und Arbeiten mit Entwurfsprüfungsfunktionen in InfoPath Designer können Sie eine zentrale Formularvorlage erstellen. Diese können Sie in einer für SharePoint Server 2013 entsprechend konfigurierten Dokumentbibliothek bereitstellen und sowohl in InfoPath Filler als auch in einem Webbrowser ausführen. 
  
## <a name="new-features-and-improvements"></a>Neue Features und Verbesserungen

In den folgenden Abschnitten werden diese Features und Verbesserungen, die für InfoPath-Entwickler interessant sind, kurz beschrieben:
  
- Neue Möglichkeit zum Schreiben und Bearbeiten von Code
    
- SharePoint-Sandkastenlösungen
    
- Veröffentlichen von Formularen mit einem Klick
    
- Verbessern von SharePoint-Listenformularen
    
- Hosten von Formularen auf Portalseiten mithilfe des InfoPath-Webparts
    
- Funktionsreichere Webformulare
    
- Standardkonforme Browserformulare
    
- Bessere Informationssicherheit und Integrität mit digitalen Signaturen
    
- Neue Steuerelemente
    
## <a name="new-way-to-write-and-edit-code"></a>Neue Möglichkeit zum Schreiben und Bearbeiten von Code

Die IDE Microsoft Visual Studio-Tools für Anwendungen, die in InfoPath 2010 integriert war, wurden in InfoPath 2013 entfernt. Zum Schreiben oder Bearbeiten von Formularcode in InfoPath 2013 wird jetzt Visual Studio 2012 mit installiertem Add-On [Microsoft Visual Studio-Tools für Anwendungen 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) benötigt. Die Programmieroberfläche selbst hat sich nicht wesentlich geändert, aber Sie können beim Schreiben von verwaltetem Code für Ihre InfoPath-Formulare jetzt die komplette Visual Studio-Entwicklungsumgebung nutzen. 
  
In den folgenden Abschnitten werden Features beschrieben, die zuerst in InfoPath 2010 und SharePoint Server 2010 hinzugefügt wurden und weiterhin nützlich für Entwickler sind, die mit InfoPath 2013 und SharePoint Server 2013 arbeiten.
  
## <a name="sharepoint-server-sandboxed-solutions"></a>SharePoint Server-Sandkastenlösungen

Mit InfoPath ist es einfacher denn je, Formulare mit Code für SharePoint Server 2013 bereitzustellen. In Office InfoPath 2007 mussten alle Formulare mit Code genehmigt und von einem SharePoint-Farmadministrator hochgeladen werden. Dank der Unterstützung für Sandkastenlösungen in SharePoint Server 2013 können Formulardesigner mit Administratorberechtigungen für Websitesammlungen nun die meisten Formulare mit Code direkt auf ihren SharePoint-Websites veröffentlichen. Eine Ressourcenkontingenteinstellung auf dem Server begrenzt übermäßigen Ressourceneinsatz. Der Websitesammlungsadministrator behält die Kontrolle und trifft Entscheidungen hinsichtlich Vertrauensstellungen im Zusammenhang mit der Lösung. Der Farmadministrator ist nicht beteiligt. Weitere Informationen zum Veröffentlichen von InfoPath-Formularvorlagen als Sandkastenlösungen finden Sie unter [Veröffentlichen von Formularen mit Code](publishing-forms-with-code.md).
  
## <a name="publish-forms-with-one-click"></a>Veröffentlichen von Formularen mit einem Mausklick

Mit InfoPath ist es einfacher denn je, Updates für Formulare zu veröffentlichen. Nach der ersten Veröffentlichung einer Formularvorlage müssen Sie zum Ausführen dieser Aufgabe nicht mehrere Dialogfelder durch Klicken durchlaufen, sondern Sie müssen nur einmal auf die neue Schaltfläche **Schnellveröffentlichung** klicken. Diese Schaltfläche ist auf der **Symbolleiste für den Schnellzugriff** und in der neuen Komponente Microsoft Office Backstage nach Klicken auf die Registerkarte **Datei** verfügbar. 
  
## <a name="enhance-sharepoint-list-forms"></a>Verbessern von SharePoint-Listenformularen

Mithilfe von InfoPath können Sie jetzt die Formulare, die zum Erstellen, Bearbeiten und Anzeigen von Elementen in einer SharePoint-Liste verwendet werden, erweitern und optimieren. Durch Öffnen einer Liste, Klicken auf die Registerkarte **Liste** unter **Listentools** und anschließendes Klicken auf **Formular anpassen** können Sie automatisch ein InfoPath-Formular generieren, das dem standardmäßigen Out-of-the-Box-SharePoint-Listenformular gleicht. Anschließend können Sie dieses Formular anpassen und verbessern, indem Sie das Layout ändern, weitere Ansichten erstellen sowie Regeln und Datenüberprüfung in InfoPath hinzufügen. Wenn Sie mit den Änderungen Ihres verbesserten Formulars fertig sind, können Sie es mit dem neuen InfoPath-Feature der One-Click-Veröffentlichung in SharePoint veröffentlichen.
  
## <a name="host-forms-on-portal-pages-using-the-infopath-form-web-part"></a>Hosten von Formularen auf Portalseiten mithilfe des InfoPath-Webparts

In SharePoint Server 2013 ist es einfacher denn je, mithilfe des neuen **InfoPath-Webparts** Formulare auf Webseiten zu hosten. In Microsoft Office SharePoint Server 2007 müssen Benutzer, die ihre InfoPath-Formulare auf Webseiten hosten möchten, Code in Visual Studio schreiben. Nun können Sie, ohne eine einzige Zeile Code zu schreiben, auf einer Webparts-Seite das **InfoPath-Webpart** hinzufügen und damit auf das veröffentlichte Formular verweisen. Sie können das **InfoPath-Webpart** zum Hosten jedes InfoPath-Browserformulars verwenden, das in einer SharePoint-Listen- oder Formularbibliothek veröffentlicht ist. Sie können es auch mit anderen Webparts auf der Seite zum Senden oder Empfangen von Daten verbinden. Weitere Informationen zur Verwendung des **InfoPath-Webparts** finden Sie unter [Arbeiten mit dem InfoPath-Webpart](https://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx) im SharePoint 2010-SDK. 
  
## <a name="richer-web-forms"></a>Funktionsreichere Webformulare

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
    
## <a name="standards-compliant-browser-forms"></a>Standardkompatible Browserformulare

InfoPath-Browserformulare entsprechen jetzt WCAG 2.0 AA (Web Content Accessibility Guidelines 2.0), sodass Formulardesigner Formulare erstellen können, die für Benutzer mit Behinderungen zur Verfügung stehen.
  
## <a name="provide-enhanced-information-security-and-integrity-with-digital-signatures"></a>Bessere Informationssicherheit und Integrität mit digitalen Signaturen

InfoPath unterstützt Inhalte, die mit CNG (Cryptography Next Generation) digital signiert werden. Um die Integrität der in Ihren Formularen enthaltenen Informationen sicherzustellen, stellen der InfoPath-Client und SharePoint Server 2013 die Steuerelemente zur Verfügung, die erforderlich sind, um Szenarien mit individueller Signatur, gemeinsamer Signatur und Gegensignatur für das ganze Formular oder Abschnitte des Formulars zu unterstützen. Formulare können in Internet Explorer mithilfe des ActiveX-Signaturzeilen-Steuerelements signiert werden. Signierte Formulare können in jedem beliebigen Browser angezeigt werden, der von SharePoint Server 2013 unterstützt wird.
  
## <a name="new-controls"></a>Neue Steuerelemente

InfoPath bietet eine größere Sammlung an Steuerelementen, die Formularen hinzugefügt werden können. Die folgende Liste bietet eine Kurzbeschreibung der neuen Steuerelemente:
  
- **Bildschaltfläche**: Anstatt eines grauen Rechtecks können Sie ein beliebiges Bild als Schaltfläche im Formular verwenden. 
    
- **Hyperlink**: Ermöglichen Sie Benutzern beim Ausfüllen von Formularen das Eingeben eigener Hyperlinks. 
    
- **Personen-/Gruppenauswahl** – Ermöglichen Sie Benutzern, beim Ausfüllen von Formularen Kontonamen und Gruppen zu überprüfen und abzufragen. 
    
- **Entitätsauswahl** – Ermöglichen Sie Benutzern beim Ausfüllen von Formularen das Auswählen von Werten aus externen Listen auf einem Server mit SharePoint Server 2013. 
    
- **Signaturzeile** – Bieten Sie Benutzern beim digitalen Signieren von Formularen eine Signaturzeile oder ein Stempelbild, z. B. ein (japanisches) Inkan- oder Hanko-Siegel. 
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von InfoPath-Formularvorlagen mit Code](developing-infopath-form-templates-with-code.md)
  
[Entwickeln von Formularvorlagen mit dem InfoPath 2003-Objektmodell](developing-form-templates-using-the-infopath-2003-object-model.md)

