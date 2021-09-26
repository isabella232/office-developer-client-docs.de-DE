---
title: Neues für Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: In diesem Thema werden die wichtigsten Änderungen in Outlook Connector für soziale Netzwerke 2013 (OSC) aufgeführt. Es stellt einen Vergleich der verfügbaren Features zwischen Outlook Connector für soziale Netzwerke 2013 und Outlook Connector für soziale Netzwerke 1.1 dar.
ms.openlocfilehash: a9f8836313ee49e0e3d7fa18ffcf1ee7e2babb75
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598962"
---
# <a name="whats-new-for-providers"></a>Neues für Anbieter

In diesem Thema werden die wichtigsten Änderungen in Outlook Connector für soziale Netzwerke 2013 (OSC) aufgeführt. Es stellt einen Vergleich der verfügbaren Features zwischen Outlook Connector für soziale Netzwerke 2013 und Outlook Connector für soziale Netzwerke 1.1 dar. Außerdem werden Schnittstellenelemente und XML-Elemente beschrieben, die hinzugefügt, geändert oder veraltet sind. 
  
In Office 2013 funktioniert osc nicht nur mit Outlook, sondern auch mit SharePoint Server, SharePoint Workspace, Lync-Client und allen anderen Office Clientanwendungen, die Anwesenheitsinformationen und die Visitenkarte unterstützen. Ein OSC-Anbieter kann Updates für soziale Netzwerke auf der Registerkarte **"NEUIGKEITEN"** im Bereich "Outlook Personen" sowie auf der Visitenkarte anzeigen. 
  
Einige wichtige Änderungen in Outlook Connector für soziale Netzwerke 2013 umfassen Folgendes: 
  
- Wenn ein Anbieter das Anzeigen von Aktivitäten unterstützt, synchronisiert der Anbieter Aktivitäten immer bei Bedarf und basiert nicht mehr auf zuvor zwischengespeicherten Aktivitäten. Das bedeutet, dass der Anbieter Aktivitäten von Freunden und Nicht-Freunden im Speicher speichert, um mehr aktuelle Aktivitäten anzuzeigen.
    
- Aus Sicherheitsgründen sollten Anbieter, die über das Internet mit Servern kommunizieren, das HTTPS-Protokoll (Hypertext Transfer Protocol, HTTP) mit SSL (Secure Socket Layer) verwenden. Andernfalls besteht das Risiko, dass E-Mail-Adressen, Aktivitäten in sozialen Netzwerken und andere Benutzerdaten während der Übertragung abgefangen oder offengelegt werden.
    
- Wenn Sie Anbieter haben, die mit einer früheren Version von Outlook arbeiten, sollten Sie zur Unterstützung von Office 2013 das Setuppaket aktualisieren. Weitere Informationen finden Sie in der [Installationsprüfliste.](installation-checklist.md) 
    
Die folgende Tabelle zeigt die Verfügbarkeit verschiedener Features in Outlook Connector für soziale Netzwerke 2013 im Vergleich zu Outlook Connector für soziale Netzwerke 1.1.
  
|**Feature**|**Outlook Connector für soziale Netzwerke 2013**|**Outlook Connector für soziale Netzwerke 1.1**|
|:-----|:-----|:-----|
|Benutzeroberfläche für Endbenutzer  <br/> |SharePoint Server, SharePoint Workspace, Lync-Client, Visitenkarte in allen Office Clientanwendungen und Personenbereich in Outlook  <br/> |Personenbereich in Outlook  <br/> |
|Standardauthentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Formularbasierte Authentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Zwischengespeicherte Authentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Zwischengespeicherte Synchronisierung für Freunde im Kontaktordner im Standardspeicher  <br/> |Ja  <br/> |Ja  <br/> |
|Synchronisierung zwischengespeicherter Aktivitäten für Freunde in **ausgeblendeten Newsfeed-Ordner**  <br/> |Nein  <br/> |Ja  <br/> |
|On-Demand-Synchronisierung (Bild, Name, Titel) für Freunde und Nicht-Freunde im Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|On-Demand-Aktivitäten werden für Freunde und Nicht-Freunde im Netzwerk synchronisiert  <br/> |Ja  <br/> |Ja  <br/> |
|Folgen im Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Nicht im Netzwerk folgen  <br/> |Ja  <br/> |Ja  <br/> |
|Seite "Benutzerprofil besuchen"  <br/> |Über einen Link  <br/> |Über ein Netzwerksignal  <br/> |
|Beobachten der Datenschutzeinstellungen in sozialen Netzwerken (z. B. Anzeigen des Profils und der Aktivitäten von Nicht-Freunden, die die Anzeige dieser Einstellungen zulassen)  <br/> |Ja  <br/> |Ja  <br/> |
|An Anbieter übergebene Hash-E-Mail-Adressen  <br/> |Ja  <br/> |Ja  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Änderungen aus der vorherigen Version der OSC-Anbietererweiterung

In der folgenden Tabelle sind die Elemente aufgeführt, die über die entsprechende Schnittstelle hinzugefügt oder veraltet sind.
  
|**Schnittstelle und Mitglied**|**Kommentar**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Veraltet in Outlook Connector für soziale Netzwerke 2013. Beachten Sie, dass **ISocialSession::GetActivities** seit Outlook Connector für soziale Netzwerke 1.1 ebenfalls veraltet ist.  <br/> Um Aktivitätsfeeds zu synchronisieren, sollten Sie die [ISocialSession2::GetActivitiesEx-Methode](isocialsession2-getactivitiesex.md) implementieren. Legen Sie **dynamicActivitiesLookupEx** auf **"true"** fest, wodurch der OSC aufgefordert **wird, stattdessen ISocialSession2::GetActivitiesEx** aufzurufen.  <br/> |
   
In der folgenden Tabelle sind die Schemaelemente aufgeführt, die geändert wurden.
  
|**Schema-Element**|**Kommentar**|
|:-----|:-----|
|**capabilities** <br/> |Hinzugefügt in Outlook Connector für soziale Netzwerke 2013: **allowChangesToAutoConfigure-Element.**  <br/> Veraltet in Outlook Connector für soziale Netzwerke 2013: **cacheActivities-Element.**  <br/> |
|**person** <br/> |Hinzugefügt in Outlook Connector für soziale Netzwerke 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **industries**, **interests**, **location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **skills**, **schools** und **website** elements.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [XML für Freunde](xml-for-friends.md)
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

