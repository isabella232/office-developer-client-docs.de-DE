---
title: Überlegungen zur unbeaufsichtigten Automatisierung von Office in Microsoft 365 unbeaufsichtigten RPA-Umgebung
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Überlegungen zur unbeaufsichtigten Automatisierung von Office in Microsoft 365 unbeaufsichtigten RPA-Umgebung.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103050"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Überlegungen zur unbeaufsichtigten Automatisierung von Office in Microsoft 365 unbeaufsichtigten RPA-Umgebung

Obwohl Microsoft 365 für unbeaufsichtigte RPA eine Lizenz bietet, die die Automatisierung von Office ohne Benutzer ermöglicht, wurden alle aktuellen Versionen von Office so entworfen und getestet, dass sie als Endbenutzerprodukte auf einer Clientarbeitsstation ausgeführt werden, wobei ein Benutzer anwesend ist, um mit der Benutzeroberfläche der Anwendung zu interagieren. Unerwartete Verhaltensweisen, die sich aus der Verwendung von Anwendungen ohne vorhandenen Benutzer ergeben, sind keine Fehler. Wenn Sie Office in dieser Konfiguration ausführen möchten, müssen Sie bereit sein, diese unerwarteten Verhaltensweisen in Ihrer Anwendungslogik zu berücksichtigen.

In diesem Artikel werden einige Überlegungen zur unbeaufsichtigten Automatisierung von Office erläutert, die Ihnen bei der Verwendung dieses Ansatzes helfen. Beachten Sie jedoch, dass die Verwendung Office in dieser Konfiguration ausschließlich "AS IS" ist und diese unerwarteten Verhaltensweisen berücksichtigen muss. Die hier bereitgestellten Informationen sind nicht vollständig und können nicht garantiert alle Probleme für alle Clients beheben. Wir empfehlen Ihnen, Ihre Lösung gründlich zu testen, bevor Sie sie bereitstellen.

## <a name="common-problems-in-unattended-automation"></a>Häufige Probleme bei der unbeaufsichtigten Automatisierung

Wenn Sie die Office verwenden möchten, ohne dass ein Benutzer vorhanden ist, beachten Sie die folgenden Bereiche, in denen Office anders als erwartet verhalten können. Damit Ihre Lösung erfolgreich ausgeführt werden kann, muss sie diese Probleme beheben und ihre Auswirkungen so weit wie möglich minimieren. Berücksichtigen Sie diese Probleme beim Erstellen Ihrer Anwendung sorgfältig.

### <a name="interactive-ui-elements"></a>Elemente der interaktiven Benutzeroberfläche

Office Anwendungen gehen davon aus, dass sie interaktiv ausgeführt werden. Wenn ein unerwarteter Fehler auftritt oder ein nicht angegebener Parameter zum Abschließen einer Funktion erforderlich ist, wird Office so konzipiert, dass der Benutzer mit einem Dialogfeld aufgefordert wird, in dem der Benutzer gefragt wird, wie er fortfahren möchte. Bei unbeaufsichtigter Automatisierung kann dies dazu führen, dass die Anwendung "hängen bleibt", wenn die Anwendung beendet wird, bis sie diese Eingabe erhält. Wenn Sie die Office über die öffentlichen APIs automatisieren, können Sie viele dieser Warnungen unterdrücken, indem Sie Eigenschaften wie [Application.DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) und [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) entsprechend konfigurieren. Ihr Code sollte so konzipiert sein, dass blockierende Warnungen jederzeit identifiziert und verarbeiten werden.

### <a name="user-identity"></a>Benutzeridentität

Office anwendungen erfordern eine Benutzeridentität, wenn die Anwendungen ausgeführt werden, auch wenn die Anwendung über automatisierung gestartet wird. Diese Benutzeridentität kann eine oder alle der folgenden Ursachen haben:

- Das Vorhandensein zusätzlicher Anmeldebenutzeroberflächen, die behandelt werden müssen.
- Dateien, die nicht basierend auf benutzerbezogenen Zugriffsberechtigungen geöffnet und/oder bearbeitet werden können.
- Unerwartete Änderungen an den Metadaten der Datei (beispielsweise werden bestimmte Dateieigenschaften basierend auf der Identität der Benutzeridentität der automatisierten Anwendungsinstanz aktualisiert).

Verschiedene Ansätze können dazu beitragen, diese Probleme zu beheben. Beispiel: Ausführen des [Dokumentinspektors](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) zum Entfernen von Metadaten. Überlegen Sie, ob diese Ansätze basierend auf Ihrem Szenario geeignet sind.

### <a name="server-side-security"></a>Serverseitige Sicherheit

Beim Ausführen Office unbeaufsichtigten und verarbeiten beliebigen Dateiinhalts stehen keine zusätzlichen schutzspezifischen In dieser Umgebung zur Verfügung, um zu verhindern, dass in diesen Dateien gespeicherte Makros geladen und ausgeführt werden. Office schützt Sie nicht vor unbeabsichtigt ausgeführten Makros aus Ihrem Code oder vor dem Starten eines anderen Servers, auf dem Makros ausgeführt werden können. Sie können Eigenschaften wie [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) verwenden, um dieses Risiko zu mindern, Sie sollten jedoch sicherstellen, dass Sie nur vertrauenswürdige Inhalte laden.

Darüber hinaus Office viele Komponenten (z. B. Simple MAPI, WinInet und MSDAIPP), die Clientauthentifizierungsinformationen zwischenspeichern können, um die Verarbeitung zu beschleunigen. Wenn Office serverseitig automatisiert wird und mehrere Dateien verarbeitet werden, kann ein Client die zwischengespeicherten Anmeldeinformationen eines anderen Clients verwenden, wenn Authentifizierungsinformationen für diese Sitzung zwischengespeichert wurden. Daher kann der Client nicht erteilte Zugriffsberechtigungen erhalten, indem er andere Benutzer als Identitätswechsel verwendet.

### <a name="ui-changes"></a>Änderungen an der Benutzeroberfläche

Die Benutzeroberflächenelemente in Office sind weitgehend stabil, aber der spezifische Speicherort eines benutzeroberflächenelements ist nicht garantiert und kann sich ändern, wenn das Produktdesign entwickelt wird, um Benutzerfeedback zu integrieren und kundenspezifische Anforderungen zu erfüllen. Dies muss in der Logik jeder Automatisierung berücksichtigt werden. Diese Änderungen können zu Änderungen bei der Benennung von Schaltflächen- oder Gruppenregisterkarten, zum Bewegen von Befehlen zwischen Registerkarten, zum Hinzufügen neuer Registerkarten oder zum Entfernen von Befehlen führen, die sich an unseren Funktionsausdrucksrichtlinien ausrichten. Diese Änderungen können auf der Benutzeroberfläche sowie innerhalb der von der Anwendung bereitgestellten Barrierefreiheitsinformationen vorgenommen werden, da diese Informationen geändert werden, um die Benutzerfreundlichkeit zu verbessern und das fortlaufende Kundenfeedback zu berücksichtigen, und sie können für verschiedene Benutzer zu unterschiedlichen Zeiten bereitgestellt werden.

Auch ohne Produktänderungen können Unterschiede zwischen Systemumgebungen (z. B. Bildschirmgröße/Auflösung/DPI) zu Änderungen an der Position von Elementen auf dem Bildschirm führen. Jeder Ansatz, der zur Simulation von Benutzereingaben auf Bildschirmkoordinaten basiert, muss diese Änderungen berücksichtigen und entsprechend anpassen.

### <a name="single-threading"></a>Singlethreading

Office anwendungen sind nicht entrante, STA-basierte Anwendungen, die verschiedene, aber ressourcenintensive Funktionen für einen einzelnen Client bereitstellen sollen. Die Anwendungen verwenden globale Ressourcen wie zugeordnete Speicherdateien, globale Add-Ins oder Vorlagen und freigegebene Automatisierungsserver. Dies kann die Anzahl der Instanzen begrenzen, die gleichzeitig ausgeführt werden können, und kann zu Racebedingungen führen, wenn die Anwendungen in einer Multiclientumgebung konfiguriert sind. Wenn Sie planen, mehrere Instanzen einer Office-Anwendung ausführen, sollten Sie sie auf ebene des virtuellen Computers isolieren, um die Stabilität der resultierenden Lösung sicherzustellen.

### <a name="resiliency-and-stability"></a>Ausfallsicherheit und Stabilität

Selbst wenn die Anwendungen auf eine Weise automatisiert werden, die Benutzereingaben simuliert, oder bei Sitzungslängen, die die interaktive Nutzung erheblich überschreiten, können probleme auftreten, die beim interaktiven Ausführen nicht vorhanden sind. Lösungen, die Office in diesem Kontext verwenden, sollten proaktiv Mechanismen erstellen, um den Status der Anwendung zu überwachen und sie (und/oder den virtuellen Computer, auf dem sie ausgeführt werden) bei Bedarf neu zu starten.

## <a name="suggested-alternatives"></a>Vorgeschlagene Alternativen

Microsoft empfiehlt dringend einige Alternativen, für die Office installiert und serverseitig ausgeführt werden müssen und die häufige Aufgaben effizienter und schneller ausführen können als die Automatisierung in dieser Konfiguration. Bevor Sie eine Office als serverseitige Komponente in Ihrem Projekt verwenden, sollten Sie Alternativen in Betracht ziehen.

### <a name="microsoft-graph"></a>Microsoft Graph

Die Microsoft Graph-API bietet Zugriff auf die Dienste, Daten und Informationen, die Benutzern und Lösungen als Teil der Microsoft-Cloud zur Verfügung stehen, einschließlich vieler Dienste, die die Anforderungen der unbeaufsichtigten Automatisierung unterstützen: Zugriff auf E-Mails/ Kalender/Kontakte/Dateien, Dokumentkonvertierung, Excel Arbeitsmappenberechnung und vieles mehr. Diese Dienste sind für die unbeaufsichtigte Verwendung und den zugriff in hohem Umfang konzipiert und verwenden eine standardmäßige RESTful-API-Syntax. Weitere Informationen zu Microsoft Graph und wie sie für die Verwendung mit Benutzerdaten verwendet werden, finden Sie unter:

- [Übersicht über Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Erste Schritte mit Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Herunterladen einer Datei in einem anderen Format](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (Dateikonvertierung)
- [Arbeiten mit Excel in Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (Arbeitsmappendetails)

### <a name="open-xml-file-formats"></a>Open XML-Dateiformate

Viele Automatisierungsaufgaben umfassen das Erstellen oder Bearbeiten von Dokumenten. Office unterstützt Open XML-Dateiformate, mit deren Hilfe Entwickler Dateiinhalte mithilfe der standardmäßigen XML- und ZIP-Technologien erstellen, bearbeiten, lesen und transformieren können, die im ISO 29500 International Standard definiert sind. Diese Dateiformate können über beliebige ZIP/XML-Tools bearbeitet werden, einschließlich System.IO.Package.IO namespace im Microsoft .NET 3.x Framework. Die direkte Bearbeitung der Dateiformate ist die empfohlene und unterstützte Methode für die Behandlung von Änderungen Office Dateien aus einem Dienst.

Microsoft stellt ein SDK zum Bearbeiten von Open XML-Dateiformaten aus dem .NET 3.x Framework zur Verfügung. Weitere Informationen zum SDK und zur Verwendung des SDK zum Erstellen oder Bearbeiten von Open XML-Dateien finden Sie unter:

- [Grundlegendes zu den Open XML-Dateiformaten](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Willkommen beim Open XML SDK 2.5 for Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
