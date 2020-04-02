---
title: Überlegungen zur unbeaufsichtigten Automatisierung von Office in der Microsoft 365 für unbeaufsichtigte RPA-Umgebung
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Überlegungen zur unbeaufsichtigten Automatisierung von Office in der Microsoft 365 für unbeaufsichtigte RPA-Umgebung.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103050"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Überlegungen zur unbeaufsichtigten Automatisierung von Office in der Microsoft 365 für unbeaufsichtigte RPA-Umgebung

Obwohl Microsoft 365 für unbeaufsichtigte RPA eine Lizenz zur Verfügung stellt, die die Automatisierung von Office ohne Benutzer ermöglicht, wurden alle aktuellen Versionen von Office so konzipiert und getestet, dass Sie als Endbenutzerprodukte auf einer Clientarbeitsstation ausgeführt werden, wobei ein Benutzer für die Interaktion mit der Anwendungsschnittstelle geeignet ist. Unerwartete Verhaltensweisen, die sich aus der Verwendung von Anwendungen ohne vorhanden sein eines Benutzers ergeben, sind keine Fehler. Wenn Sie Office in dieser Konfiguration ausführen möchten, müssen Sie bereit sein, diese unerwarteten Verhaltensweisen in ihrer Anwendungslogik zu berücksichtigen.

In diesem Artikel werden einige der Überlegungen zur unbeaufsichtigten Automatisierung von Office beschrieben, die Ihnen bei der Verwendung dieses Ansatzes helfen. Beachten Sie jedoch, dass die Verwendung von Office in dieser Konfiguration streng "wie besehen" ist und diese unerwarteten Verhaltensweisen berücksichtigen muss. Die hier bereitgestellten Informationen sind nicht erschöpfend und werden nicht sichergestellt, dass alle Probleme für alle Clients behoben werden. Wir empfehlen Ihnen, Ihre Lösung gründlich zu testen, bevor Sie bereitstellen.

## <a name="common-problems-in-unattended-automation"></a>Häufige Probleme bei der unbeaufsichtigten Automatisierung

Wenn Sie Office ohne einen Benutzer verwenden möchten, beachten Sie die folgenden Bereiche, in denen sich Office anders als erwartet Verhalten kann. Damit Ihre Lösung erfolgreich ausgeführt werden kann, müssen Sie diese Probleme lösen und ihre Auswirkungen so weit wie möglich minimieren. Berücksichtigen Sie diese Probleme sorgfältig, wenn Sie Ihre Anwendung erstellen.

### <a name="interactive-ui-elements"></a>Interaktive Benutzeroberflächenelemente

Office-Anwendungen gehen davon aus, dass Sie interaktiv ausgeführt werden. Wenn ein unerwarteter Fehler auftritt oder ein nicht angegebener Parameter zum Ausführen einer Funktion erforderlich ist, wird Office so konzipiert, dass der Benutzer mit einem Dialogfeld aufgefordert wird, in dem der Benutzer fragt, wie er fortfahren soll. In der unbeaufsichtigten Automatisierung kann dies dazu führen, dass die Anwendung "hängt", während die Anwendung angehalten wird, bis diese Eingabe empfangen wird. Wenn Sie Office über die öffentlichen APIs automatisieren, können Sie viele dieser Warnungen unterdrücken, indem Sie Eigenschaften wie [Application. DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) und [Application. AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) entsprechend konfigurieren. Ihr Code sollte zum Identifizieren und Verarbeiten von Blockierungs Benachrichtigungen jederzeit entwickelt werden.

### <a name="user-identity"></a>Benutzeridentität

Office-Anwendungen erfordern eine Benutzeridentität, wenn die Anwendungen ausgeführt werden, selbst wenn die Anwendung über Automatisierung gestartet wird. Diese Benutzeridentität kann eine oder alle der folgenden Ursachen haben:

- Das vorhanden sein zusätzlicher Anmeldebenutzeroberfläche, die verarbeitet werden muss.
- Dateien, die basierend auf den Zugriffsberechtigungen pro Benutzer nicht geöffnet und/oder bearbeitet werden können.
- Unerwartete Änderungen an den Metadaten der Datei (beispielsweise werden bestimmte Dateieigenschaften basierend auf der Identität der Benutzeridentität der automatisierten Anwendungsinstanz aktualisiert).

Verschiedene Ansätze können dazu beitragen, diese Probleme zu verringern. beispielsweise das Durchführen des [Dokumentinspektors](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) zum Entfernen von Metadaten. Prüfen Sie, ob diese Ansätze basierend auf Ihrem Szenario geeignet sind.

### <a name="server-side-security"></a>Server seitige Sicherheit

Wenn Sie Office ohne Beaufsichtigung und Verarbeitung beliebiger Dateiinhalte durchführen, stehen keine zusätzlichen Schutzmaßnahmen in dieser Umgebung zur Verfügung, um zu verhindern, dass in diesen Dateien gespeicherte Makros geladen und in Betrieb genommen werden. Office schützt Sie nicht vor versehentlich ausgeführten Makros aus Ihrem Code oder aus dem Starten eines anderen Servers, der möglicherweise Makros ausführt. Sie können Eigenschaften wie [Application. AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) verwenden, um dieses Risiko zu minimieren, aber Sie sollten sicherstellen, dass Sie nur vertrauenswürdige Inhalte laden.

Darüber hinaus verwendet Office viele Komponenten (wie Simple MAPI, WinInet und MSDAIPP), mit denen Client Authentifizierungsinformationen zwischengespeichert werden können, um die Verarbeitung zu beschleunigen. Wenn Office serverseitig automatisiert wird und mehrere Dateien verarbeitet, kann ein Client die zwischengespeicherten Anmeldeinformationen eines anderen Clients verwenden, wenn Authentifizierungsinformationen für diese Sitzung zwischengespeichert wurden. Der Client kann daher nicht gewährte Zugriffsberechtigungen erhalten, indem er andere Benutzer imitiert.

### <a name="ui-changes"></a>Änderungen an der Benutzeroberfläche

Die Benutzeroberflächenelemente in Office sind weitgehend stabil, aber die spezifische Position eines beliebigen Benutzeroberflächenelements ist nicht garantiert und kann sich ändern, wenn sich das Produktdesign entwickelt, um Benutzer Feedback zu integrieren und die Kundenanforderungen zu erfüllen. Dabei muss die Logik jeder Automatisierung berücksichtigt werden. Diese Änderungen können dazu führen, dass Schaltflächen-oder Gruppenregisterkarten Namensänderungen, die Verschiebung von Befehlen zwischen Registerkarten, das Hinzufügen neuer Registerkarten oder das Entfernen von Befehlen in Übereinstimmung mit unseren Feature-veraltet-Richtlinien resultieren. Diese Änderungen können sowohl in der Benutzeroberfläche als auch in den von der Anwendung bereitgestellten Informationen zur Barrierefreiheit stattfinden, da diese Informationen geändert werden, um die Benutzerfreundlichkeit zu verbessern und das laufende Kundenfeedback zu berücksichtigen, und möglicherweise zu unterschiedlichen Zeiten für verschiedene Benutzer eingeführt werden.

Selbst ohne Produktänderungen können Unterschiede zwischen Systemumgebungen (wie Bildschirmgröße/Auflösung/dpi) zu Änderungen am Speicherort von Elementen auf dem Bildschirm führen. Jeder Ansatz, der auf Bildschirmkoordinaten zum Simulieren der Benutzereingabe angewiesen ist, muss diese Änderungen berücksichtigen und entsprechend anpassen.

### <a name="single-threading"></a>Einzel Threading

Office-Anwendungen sind nicht-Einsteiger, STA-basierte Anwendungen, die für die Bereitstellung unterschiedlicher, aber ressourcenintensiver Funktionen für einen einzelnen Client ausgelegt sind. Die Anwendungen verwenden globale Ressourcen wie Speicher zugeordnete Dateien, globale Add-Ins oder Vorlagen sowie freigegebene Automatisierungsserver. Dies kann die Anzahl von Instanzen begrenzen, die gleichzeitig ausgeführt werden können, und kann zu Racebedingungen führen, wenn die Anwendungen in einer Multiclient-Umgebung konfiguriert sind. Wenn Sie mehr als eine Instanz einer Office-Anwendung ausführen möchten, sollten Sie diese auf der Ebene des virtuellen Computers isolieren, um die Stabilität der resultierenden Lösung sicherzustellen.

### <a name="resiliency-and-stability"></a>Ausfallsicherheit und Stabilität

Selbst mit den obigen Überlegungen, wenn die Anwendungen auf eine Art und Weise automatisiert werden, die Benutzereingaben simuliert, oder um Sitzungs Längen, die die interaktive Nutzung dramatisch übersteigen, können Probleme auftreten, die bei der interaktiven Ausführung nicht vorhanden sind. Lösungen, die Office in diesem Kontext verwenden, sollten proaktiv Mechanismen zum Überwachen des Status der Anwendung erstellen und diese (und/oder den virtuellen Computer, auf dem Sie laufen) nach Bedarf neu starten.

## <a name="suggested-alternatives"></a>Vorgeschlagene Alternativen

Microsoft empfiehlt dringend einige Alternativen, die nicht erforderlich sind, dass Office installiert wird und serverseitig ausgeführt wird, und die allgemeine Aufgaben effizienter und schneller ausführen können als die Automatisierung in dieser Konfiguration. Bevor Sie Office als serverseitige Komponente in Ihr Projekt einbeziehen, sollten Sie Alternativen in Frage stellen.

### <a name="microsoft-graph"></a>Microsoft Graph

Die Microsoft Graph-API bietet Zugriff auf die Dienste, Daten und Informationen, die Benutzern und Lösungen im Rahmen der Microsoft-Cloud zur Verfügung stehen, einschließlich zahlreicher Dienste, die die Anforderungen der unbeaufsichtigten Automatisierung unterstützen: Zugriff auf e-Mails/Kalender/Kontakte/Dateien von Benutzern, Dokumentkonvertierung, Excel-Arbeitsmappen-Berechnung und vieles mehr. Diese Dienste sind für die unbeaufsichtigte Verwendung und den umfassenden Zugriff konzipiert und verwenden eine standardmäßige Rest-API-Syntax. Weitere Informationen zu Microsoft Graph und seiner Verwendung zum Arbeiten mit den Daten von Benutzern finden Sie in den folgenden Themen:

- [Übersicht über Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Erste Schritte mit Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Herunterladen einer Datei in einem anderen Format](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (Dateikonvertierung)
- [Arbeiten mit Excel in Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (Details zur Arbeitsmappe)

### <a name="open-xml-file-formats"></a>Open XML-Dateiformate

Viele Automatisierungsaufgaben umfassen das Erstellen oder Bearbeiten von Dokumenten. Office unterstützt Open XML-Dateiformate, mit denen Entwickler Dateiinhalte mithilfe von Standard-XML-und ZIP-Technologien erstellen, bearbeiten, lesen und transformieren können, die im internationalen ISO 29500-Standard definiert sind. Diese Dateiformate können über alle zip/XML-Tools, einschließlich des System.IO.Package.IO-Namespaces im Microsoft .NET 3. x-Framework, manipuliert werden. Die direkte Bearbeitung der Dateiformate ist die empfohlene und unterstützte Methode zum Behandeln von Änderungen an Office-Dateien von einem Dienst.

Microsoft stellt ein SDK zum Bearbeiten von Open XML-Dateiformaten aus dem .NET 3. x-Framework bereit. Weitere Informationen zum SDK und zur Verwendung des SDK zum Erstellen oder Bearbeiten von Open XML-Dateien finden Sie in den folgenden Themen:

- [Grundlegendes zu den Open XML-Dateiformaten](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Willkommen beim Open XML SDK 2.5 für Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
