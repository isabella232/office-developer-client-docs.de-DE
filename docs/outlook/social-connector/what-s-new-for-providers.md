---
title: Neues für Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: In diesem Thema werden die wichtigsten Änderungen in Outlook Social Connector 2013 (OSC) aufgeführt. Es enthält einen Vergleich der verfügbaren Features zwischen Outlook Social Connector 2013 und Outlook Social Connector 1.1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435453"
---
# <a name="whats-new-for-providers"></a>Neues für Anbieter

In diesem Thema werden die wichtigsten Änderungen in Outlook Social Connector 2013 (OSC) aufgeführt. Es enthält einen Vergleich der verfügbaren Features zwischen Outlook Social Connector 2013 und Outlook Social Connector 1.1. Außerdem werden Schnittstellenelemente und XML-Elemente beschrieben, die hinzugefügt, geändert oder veraltet sind. 
  
In Office 2013 arbeitet das OSC nicht nur mit Outlook, sondern auch mit SharePoint Server, SharePoint Workspace, Lync-Client und allen anderen Office-Clientanwendungen, die Anwesenheitsinformationen und die Visitenkarte unterstützen. Ein OSC-Anbieter kann Updates  für soziale Informationen auf der Registerkarte NEUIGKEITEN im Bereich Outlook Personen sowie auf der Visitenkarte anzeigen. 
  
Einige wichtige Änderungen in Outlook Social Connector 2013 umfassen Folgendes: 
  
- Wenn ein Anbieter das Anzeigen von Aktivitäten unterstützt, synchronisiert der Anbieter aktivitäten immer nach Bedarf und ist nicht mehr auf zuvor zwischengespeicherte Aktivitäten angewiesen. Das bedeutet, dass der Anbieter Aktivitäten von Freunden und Nicht-Freunden im Speicher speichert, um aktuellere Aktivitäten anzeigen zu können.
    
- Aus Sicherheitsgründen sollten Anbieter, die mit Servern über das Internet kommunizieren, das HTTPS -Protokoll (Hypertext Transfer Protocol, HTTP) mit SSL (Secure Socket Layer) verwenden. Andernfalls besteht das Risiko, dass E-Mail-Adressen, Aktivitäten in sozialen Netzwerken und andere Benutzerdaten während der Übertragung abgefangen oder verfügbar gemacht werden.
    
- Wenn Sie Anbieter haben, die mit einer früheren Version von Outlook arbeiten, sollten Sie das Setuppaket aktualisieren, um Office 2013 zu unterstützen. Weitere [Informationen finden Sie unter Installationscheckliste.](installation-checklist.md) 
    
Die folgende Tabelle zeigt die Verfügbarkeit verschiedener Features in Outlook Connector für soziale Netzwerke 2013 im Vergleich zu Outlook Social Connector 1.1.
  
|**Feature**|**Outlook Connector für soziale Netzwerke 2013**|**Outlook Connector für soziale Netzwerke 1.1**|
|:-----|:-----|:-----|
|Endbenutzerschnittstelle  <br/> |SharePoint Server, SharePoint Arbeitsbereich, Lync-Client, Visitenkarte in Office Clientanwendungen und Personenbereich in Outlook  <br/> |Personenbereich in Outlook  <br/> |
|Standardauthentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Formularbasierte Authentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Zwischengespeicherte Authentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Cached sync for friends to contacts folder on default store  <br/> |Ja  <br/> |Ja  <br/> |
|Synchronisierung zwischengespeicherter Aktivitäten für Freunde mit ausgeblendeten **Newsfeedordnern**  <br/> |Nein  <br/> |Ja  <br/> |
|On-Demand-Synchronisierung (Bild, Name, Titel) für Freunde und Nicht-Freunde im Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Synchronisierung von On-Demand-Aktivitäten für Freunde und Nicht-Freunde im Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Folgen im Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Nicht im Netzwerk folgen  <br/> |Ja  <br/> |Ja  <br/> |
|Benutzerprofilseite besuchen  <br/> |Über einen Link  <br/> |Über ein Netzwerkabzeichen  <br/> |
|Beobachten von Datenschutzeinstellungen in sozialen Netzwerken (z. B. Anzeigen von Profil und Aktivitäten von Nicht-Freunden, die die Anzeige dieser Einstellungen zulassen)  <br/> |Ja  <br/> |Ja  <br/> |
|An den Anbieter übergebene E-Mail-Adressen mit Hash  <br/> |Ja  <br/> |Ja  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Änderungen an der vorherigen Version der Erweiterbarkeit des OSC-Anbieters

In der folgenden Tabelle sind die Elemente aufgeführt, die von der entsprechenden Schnittstelle hinzugefügt oder veraltet sind.
  
|**Schnittstelle und Mitglied**|**Kommentar**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Veraltet in Outlook Social Connector 2013. Beachten **Sie, dass ISocialSession::GetActivities** seit Outlook Social Connector 1.1 veraltet ist.  <br/> Zum Synchronisieren von Aktivitätsfeeds sollten Sie die [ISocialSession2::GetActivitiesEx-Methode](isocialsession2-getactivitiesex.md) implementieren. Legen **Sie dynamicActivitiesLookupEx** als **true** fest, wodurch das OSC **stattdessen ISocialSession2::GetActivitiesEx aufruft.**  <br/> |
   
In der folgenden Tabelle sind die Schemaelemente aufgeführt, die geändert wurden.
  
|**Schemaelement**|**Kommentar**|
|:-----|:-----|
|**capabilities** <br/> |Hinzugefügt in Outlook Social Connector 2013: **allowChangesToAutoConfigure-Element.**  <br/> Veraltet in Outlook Social Connector 2013: **cacheActivities-Element.**  <br/> |
|**Person** <br/> |Hinzugefügt in Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, industries , **interests**, **location**, **otherAddress**, otherCity ,  **otherCountryOrRegion**, **otherState**, **otherZip**, **skills**, **schools** und **website elements.**   <br/> |
   
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [XML für Freunde](xml-for-friends.md)
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

