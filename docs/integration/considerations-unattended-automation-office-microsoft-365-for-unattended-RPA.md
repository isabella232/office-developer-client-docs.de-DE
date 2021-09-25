---
title: Überlegungen zur unbeaufsichtigten Automatisierung von Office im Microsoft 365 für unbeaufsichtigte RPA-Umgebungen
ms.date: 03/30/2020
ms.audience: Developer
ms.localizationpriority: medium
description: Überlegungen zur unbeaufsichtigten Automatisierung von Office im Microsoft 365 für eine unbeaufsichtigte RPA-Umgebung.
ms.openlocfilehash: d12d7a4d3eeb2b68425e56c4f98d5c8f7a9dc446
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621185"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Überlegungen zur unbeaufsichtigten Automatisierung von Office im Microsoft 365 für unbeaufsichtigte RPA-Umgebungen

Obwohl Microsoft 365 für unbeaufsichtigte RPA eine Lizenz bereitstellt, die die Automatisierung von Office ohne Benutzer ermöglicht, wurden alle aktuellen Versionen von Office so konzipiert und getestet, dass sie als Endbenutzerprodukte auf einer Clientarbeitsstation mit einem Benutzer ausgeführt werden können, der mit der Benutzeroberfläche der Anwendung interagieren kann. Unerwartete Verhaltensweisen, die sich aus der Verwendung von Anwendungen ohne einen Benutzer ergeben, sind keine Fehler. Wenn Sie Office in dieser Konfiguration ausführen möchten, müssen Sie darauf vorbereitet sein, diese unerwarteten Verhaltensweisen in der Anwendungslogik zu berücksichtigen.

In diesem Artikel werden einige Überlegungen zur unbeaufsichtigten Automatisierung von Office erläutert, die Ihnen bei der Verwendung dieses Ansatzes helfen. Beachten Sie jedoch, dass die Verwendung von Office in dieser Konfiguration streng "AS IS" ist und diese unerwarteten Verhaltensweisen berücksichtigen muss. Die hier bereitgestellten Informationen sind nicht vollständig und können nicht garantiert alle Probleme für alle Clients beheben. Wir empfehlen Ihnen, Ihre Lösung sorgfältig zu testen, bevor Sie sie bereitstellen.

## <a name="common-problems-in-unattended-automation"></a>Häufige Probleme bei der unbeaufsichtigten Automatisierung

Wenn Sie Office verwenden möchten, ohne dass ein Benutzer anwesend ist, beachten Sie die folgenden Bereiche, in denen sich Office anders verhalten können als erwartet. Damit Ihre Lösung erfolgreich ausgeführt werden kann, muss sie diese Probleme beheben und deren Auswirkungen so weit wie möglich minimieren. Berücksichtigen Sie diese Probleme sorgfältig, wenn Sie Ihre Anwendung erstellen.

### <a name="interactive-ui-elements"></a>Interaktive UI-Elemente

Office Anwendungen gehen davon aus, dass sie interaktiv ausgeführt werden. Wenn ein unerwarteter Fehler auftritt oder ein nicht angegebener Parameter zum Abschließen einer Funktion erforderlich ist, dient Office dazu, den Benutzer mit einem Dialogfeld aufzufordern, in dem der Benutzer gefragt wird, wie er fortfahren soll. Bei der unbeaufsichtigten Automatisierung kann dies dazu führen, dass die Anwendung "hängen bleibt", wenn die Anwendung anhält, bis sie diese Eingabe empfängt. Wenn Sie Office über die öffentlichen APIs automatisieren, können Sie viele dieser Warnungen unterdrücken, indem Sie Eigenschaften wie [Application.DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) und [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) entsprechend konfigurieren. Ihr Code sollte so konzipiert sein, dass blockierende Warnungen jederzeit identifiziert und verarbeitet werden.

### <a name="user-identity"></a>Benutzeridentität

Office Anwendungen benötigen eine Benutzeridentität, wenn die Anwendungen ausgeführt werden, auch wenn die Anwendung über die Automatisierung gestartet wird. Diese Benutzeridentität kann eine oder alle der folgenden Ursachen haben:

- Das Vorhandensein zusätzlicher Anmeldebenutzeroberfläche, die verarbeitet werden muss.
- Dateien, die basierend auf Benutzerzugriffsberechtigungen nicht geöffnet und/oder bearbeitet werden können.
- Unerwartete Änderungen an den Metadaten der Datei (beispielsweise werden bestimmte Dateieigenschaften basierend auf der Identität der Benutzeridentität der automatisierten Anwendungsinstanz aktualisiert).

Verschiedene Ansätze können dazu beitragen, diese Probleme zu beheben. Führen Sie beispielsweise den [Dokumentinspektor](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) aus, um Metadaten zu entfernen. Überlegen Sie, ob diese Ansätze basierend auf Ihrem Szenario geeignet sind.

### <a name="server-side-security"></a>Serverseitige Sicherheit

Wenn Sie Office unbeaufsichtigt ausführen und beliebige Dateiinhalte verarbeiten, sind keine zusätzlichen spezifischen Schutzmaßnahmen in dieser Umgebung verfügbar, um zu verhindern, dass in diesen Dateien gespeicherte Makros geladen und ausgeführt werden. Office schützt Sie nicht davor, versehentlich Makros aus Ihrem Code auszuführen oder einen anderen Server zu starten, auf dem Makros ausgeführt werden können. Sie können Eigenschaften wie [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) verwenden, um dieses Risiko zu verringern, aber Sie sollten sicherstellen, dass Nur vertrauenswürdige Inhalte geladen werden.

Darüber hinaus verwendet Office viele Komponenten (z. B. simple MAPI, WinInet und MSDAIPP), die Clientauthentifizierungsinformationen zwischenspeichern können, um die Verarbeitung zu beschleunigen. Wenn Office serverseitig automatisiert wird und mehrere Dateien verarbeitet, kann ein Client die zwischengespeicherten Anmeldeinformationen eines anderen Clients verwenden, wenn Authentifizierungsinformationen für diese Sitzung zwischengespeichert wurden. Daher kann der Client nicht gewährte Zugriffsberechtigungen erhalten, indem er andere Benutzer imitiert.

### <a name="ui-changes"></a>Änderungen an der Benutzeroberfläche

Die Ui-Elemente in Office sind weitgehend stabil, aber die spezifische Position eines UI-Elements ist nicht garantiert und kann sich ändern, wenn sich das Produktdesign weiterentwickelt, um Benutzerfeedback zu integrieren und die Kundenanforderungen zu erfüllen. Die Logik jeder Automatisierung muss dies berücksichtigen. Diese Änderungen können zu Änderungen bei der Benennung von Schaltflächen oder Gruppenregisterkarten, zum Verschieben von Befehlen zwischen Registerkarten, zum Hinzufügen neuer Registerkarten oder zum Entfernen von Befehlen in Übereinstimmung mit unseren Feature-Veraltet-Richtlinien führen. Diese Änderungen können sowohl in der Benutzeroberfläche als auch in den von der Anwendung bereitgestellten Barrierefreiheitsinformationen erfolgen, da diese Informationen geändert werden, um die Benutzerfreundlichkeit zu verbessern und fortlaufendes Kundenfeedback zu berücksichtigen, und möglicherweise für verschiedene Benutzer zu unterschiedlichen Zeiten bereitgestellt werden.

Auch ohne Produktänderungen können Unterschiede zwischen Systemumgebungen (z. B. Bildschirmgröße/Auflösung/DPI) zu Änderungen an der Position von Elementen auf dem Bildschirm führen. Jeder Ansatz, bei dem Bildschirmkoordinaten zum Simulieren der Benutzereingabe verwendet werden, muss diese Änderungen berücksichtigen und sich entsprechend anpassen.

### <a name="single-threading"></a>Singlethreading

Office Anwendungen sind nicht reaktive STA-basierte Anwendungen, die unterschiedliche, aber ressourcenintensive Funktionen für einen einzelnen Client bereitstellen. Die Anwendungen verwenden globale Ressourcen wie zugeordnete Speicherdateien, globale Add-Ins oder Vorlagen und freigegebene Automatisierungsserver. Dies kann die Anzahl der Instanzen einschränken, die gleichzeitig ausgeführt werden können, und zu Racebedingungen führen, wenn die Anwendungen in einer Multiclientumgebung konfiguriert sind. Wenn Sie mehrere Instanzen einer beliebigen Office-Anwendung ausführen möchten, sollten Sie planen, sie auf der Ebene des virtuellen Computers zu isolieren, um die Stabilität der resultierenden Lösung sicherzustellen.

### <a name="resiliency-and-stability"></a>Resilienz und Stabilität

Auch wenn die Anwendungen auf eine Art und Weise automatisiert werden, die Benutzereingaben simuliert, oder sitzungslängen, die die interaktive Nutzung erheblich überschreiten, können probleme auftreten, die beim interaktiven Ausführen nicht vorhanden sind. Lösungen, die Office in diesem Kontext nutzen, sollten proaktiv Mechanismen erstellen, um den Status der Anwendung zu überwachen und sie (und/oder den virtuellen Computer, auf dem sie ausgeführt werden) bei Bedarf neu zu starten.

## <a name="suggested-alternatives"></a>Vorgeschlagene Alternativen

Microsoft empfiehlt dringend einige Alternativen, für die Office nicht installiert und serverseitig ausgeführt werden müssen und allgemeine Aufgaben effizienter und schneller ausführen können als die Automatisierung in dieser Konfiguration. Bevor Sie Office als serverseitige Komponente in Ihr Projekt einbeziehen, sollten Sie Alternativen in Betracht ziehen.

### <a name="microsoft-graph"></a>Microsoft Graph

Die Microsoft Graph-API bietet Zugriff auf die Dienste, Daten und Informationen, die Benutzern und Lösungen als Teil der Microsoft-Cloud zur Verfügung stehen, einschließlich vieler Dienste, die die Anforderungen der unbeaufsichtigten Automatisierung unterstützen: Zugriff auf E-Mails/Kalender/Kontakte/Dateien von Benutzern, Dokumentkonvertierung, Excel Arbeitsmappenberechnung und vieles mehr. Diese Dienste sind für die unbeaufsichtigte Verwendung und den zugriff in großem Maßstab konzipiert und verwenden eine standardmäßige RESTful-API-Syntax. Weitere Informationen zu Microsoft Graph und deren Verwendung für die Arbeit mit Benutzerdaten finden Sie unter:

- [Übersicht über Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Erste Schritte mit Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Herunterladen einer Datei in einem anderen Format](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (Dateikonvertierung)
- [Arbeiten mit Excel in Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (Arbeitsmappendetails)

### <a name="open-xml-file-formats"></a>Open XML-Dateiformate

Viele Automatisierungsaufgaben umfassen das Erstellen oder Bearbeiten von Dokumenten. Office unterstützt Open XML-Dateiformate, mit denen Entwickler Dateiinhalte mithilfe standardmäßiger XML- und ZIP-Technologien erstellen, bearbeiten, lesen und transformieren können, die im ISO 29500 International Standard definiert sind. Diese Dateiformate können über alle ZIP-/XML-Tools bearbeitet werden, einschließlich des System.IO.Package.IO Namespaces im Microsoft .NET 3.x Framework. Die direkte Bearbeitung der Dateiformate ist die empfohlene und unterstützte Methode zum Behandeln von Änderungen an Office Dateien aus einem Dienst.

Microsoft bietet ein SDK zum Bearbeiten von Open XML-Dateiformaten aus .NET 3.x Framework. Weitere Informationen zum SDK und zur Verwendung des SDK zum Erstellen oder Bearbeiten von Open XML-Dateien finden Sie unter:

- [Grundlegendes zu den Open XML-Dateiformaten](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Willkommen beim Open XML SDK 2.5 für Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
