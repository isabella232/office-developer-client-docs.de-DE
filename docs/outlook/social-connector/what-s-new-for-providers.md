---
title: Neues für Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: In diesem Thema werden die wichtigsten Änderungen in Outlook Social Connector 2013 (OSC) aufgeführt. Es stellt einen Vergleich der Features bereit, die zwischen Outlook Social Connector 2013 und Outlook Social Connector 1,1 zur Verfügung stehen.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329113"
---
# <a name="whats-new-for-providers"></a>Neues für Anbieter

In diesem Thema werden die wichtigsten Änderungen in Outlook Social Connector 2013 (OSC) aufgeführt. Es stellt einen Vergleich der Features bereit, die zwischen Outlook Social Connector 2013 und Outlook Social Connector 1,1 zur Verfügung stehen. Außerdem werden Schnittstellenmember und XML-Elemente beschrieben, die hinzugefügt, geändert oder veraltet sind. 
  
In Office 2013 funktioniert OSC nicht nur mit Outlook, sondern auch mit SharePoint Server, SharePoint Workspace, lync-Client und allen anderen Office-Clientanwendungen, die Anwesenheitsinformationen und die VisitenKarte unterstützen. Ein OSC-Anbieter kann soziale Informationsaktualisierungen auf der Registerkarte **Neuigkeiten** im Outlook-Personen Bereich sowie in der Visitenkarte anzeigen. 
  
Einige wichtige Änderungen in Outlook Social Connector 2013 sind: 
  
- Wenn ein Anbieter Aktivitäten anzeigen unterstützt, synchronisiert der Anbieter immer Aktivitäten bei Bedarf und verlässt sich nicht mehr auf zuvor zwischengespeicherte Aktivitäten. Das führt dazu, dass der Anbieter Aktivitäten von Freunden und nicht-Freunden im Arbeitsspeicher speichert, um weitere aktuelle Aktivitäten anzuzeigen.
    
- Aus Sicherheitsgründen sollten Anbieter, die mit Servern über das Internet kommunizieren, das HTTPS (Hypertext Transfer Protocol (HTTP) mit Secure Socket Layer (SSL))-Protokoll verwenden. Andernfalls besteht die Gefahr, dass e-Mail-Adressen, Aktivitäten für soziale Netzwerke und andere Benutzerdaten während der Übertragung abgefangen oder ausgesetzt werden.
    
- Wenn Sie Anbieter haben, die mit einer früheren Version von Outlook arbeiten, um Office 2013 zu unterstützen, sollten Sie das Setuppaket aktualisieren. Weitere Informationen finden Sie unter [Installationsprüfliste](installation-checklist.md) . 
    
In der folgenden Tabelle sind die Verfügbarkeit von verschiedenen Features in Outlook Social Connector 2013 im Vergleich zu Outlook Social Connector 1,1.
  
|**Feature**|**Outlook Connector für soziale Netzwerke 2013**|**Outlook Connector für soziale Netzwerke 1,1**|
|:-----|:-----|:-----|
|Endbenutzeroberfläche  <br/> |SharePoint Server, SharePoint Workspace, lync-Client, VisitenKarte in allen Office-Clientanwendungen und Personen Bereich in Outlook  <br/> |Personen Bereich in Outlook  <br/> |
|Standardauthentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Formularbasierte Authentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Zwischengespeicherte Authentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Cached Sync for friends to Contacts Folder on default Store  <br/> |Ja  <br/> |Ja  <br/> |
|Zwischengespeicherte Aktivitäten synchronisieren für Freunde mit ausgeblendetem **Newsfeed** -Ordner  <br/> |Nein  <br/> |Ja  <br/> |
|On-Demand-Synchronisierung (Bild, Name, Titel) für Freunde und nicht-Freunde im Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Synchronisierung von on-Demand-Aktivitäten für Freunde und nicht-Freunde im Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Netzwerk folgen  <br/> |Ja  <br/> |Ja  <br/> |
|Folgen Sie nicht im Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Benutzerprofilseite besuchen  <br/> |Über einen Link  <br/> |Über ein Netzwerk Abzeichen  <br/> |
|Unter Wahrung der Datenschutzeinstellungen für soziale Netzwerke (beispielsweise Anzeigen von Profilen und Aktivitäten von nicht-Freunden, die diese anzeigen können)  <br/> |Ja  <br/> |Ja  <br/> |
|An den Anbieter übergebene Hash-e-Mail-Adressen  <br/> |Ja  <br/> |Ja  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Änderungen aus der vorherigen Version der OSC-Anbieter Erweiterbarkeit

In der folgenden Tabelle sind die Elemente aufgeführt, die der entsprechenden Schnittstelle hinzugefügt oder veraltet sind.
  
|**Schnittstelle und Member**|**Kommentar**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Veraltet in Outlook Connector für soziale Netzwerke 2013. Beachten Sie, dass **ISocialSession:: GetActivities** seit Outlook Social Connector 1,1 auch veraltet ist.  <br/> Um Aktivitätsfeeds zu synchronisieren, sollten Sie die [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode implementieren. Legen Sie **dynamicActivitiesLookupEx** als **true**fest, wodurch der osc aufgefordert wird, **ISocialSession2:: GetActivitiesEx** stattdessen aufzurufen.  <br/> |
   
In der folgenden Tabelle sind die geänderten Schemaelemente aufgeführt.
  
|**Schema-Element**|**Kommentar**|
|:-----|:-----|
|**Funktionen** <br/> |HinzugeFügt in Outlook Social Connector 2013: **allowChangesToAutoConfigure** -Element.  <br/> Veraltet in Outlook Social Connector 2013: **cacheActivities** -Element.  <br/> |
|**Person** <br/> |HinzugeFügt in Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **Industries**, **interests**, ** Location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **Skills**, **Schools**, and **Website** Elements.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [XML für Freunde](xml-for-friends.md)
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

