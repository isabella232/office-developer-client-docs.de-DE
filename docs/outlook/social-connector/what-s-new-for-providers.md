---
title: Neues für Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: In diesem Thema werden die wichtigsten Änderungen in Outlook Social Connector 2013 (OSC). Es enthält einen Vergleich zwischen Outlook Social Connector 2013 und Outlook Social Connector 1.1 verfügbaren Features.
ms.openlocfilehash: bdd7f7998f34a0ad096964050543f3f687bd0841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796101"
---
# <a name="whats-new-for-providers"></a>Neues für Anbieter

In diesem Thema werden die wichtigsten Änderungen in Outlook Social Connector 2013 (OSC). Es enthält einen Vergleich zwischen Outlook Social Connector 2013 und Outlook Social Connector 1.1 verfügbaren Features. Außerdem werden Elemente der Benutzeroberfläche und XML-Elemente, die hinzugefügt, geändert, veraltet oder wurden beschrieben. 
  
In Office 2013 funktioniert die OSC mit nicht nur Outlook, aber auch SharePoint Server, SharePoint-Arbeitsbereich Lync-Clients und alle anderen Office-Clientanwendungen, die Anwesenheitsinformationen und der Visitenkarte unterstützen. Ein OSC-Anbieter kann Updates Registerkarte **WHAT's NEW** in Outlook Personen im ebenso wie in der Visitenkarte für soziale Netzwerke Informationen offenlegen. 
  
Einige wesentliche Änderungen in Outlook Social Connector 2013 umfassen Folgendes: 
  
- Wenn ein Anbieter mit Aktivitäten unterstützt, werden der Anbieter, immer synchronisiert Aktivitäten bei Bedarf und nicht mehr zuvor zwischengespeicherten Aktivitäten nutzt. Dies bedeutet, dass der Anbieter Aktivitäten Freunde und nicht Freunde im Arbeitsspeicher zum Anzeigen von aktueller Aktivitäten gespeichert werden.
    
- Aus Sicherheitsgründen sollten Rollenanbieter, die Kommunikation über das Internet mit Servern das Protokoll HTTPS (Hypertext Transfer Protocol (HTTP) mit Secure Socket Layer (SSL)) verwenden. Andernfalls ist ein Risiko dar, die e-Mail-Adressen, Aktivitäten für soziale Netzwerke und anderer Benutzer Daten abgefangen oder unterwegs verfügbar gemacht werden.
    
- Wenn Sie Anbieter, die mit einer früheren Version von Outlook arbeiten verfügen, sollten Sie zur Unterstützung der Office 2013, das Setup-Paket aktualisieren. Weitere Informationen finden Sie unter [Installationsprüfliste](installation-checklist.md) . 
    
Die folgende Tabelle zeigt die Verfügbarkeit der verschiedenen Features in Outlook Social Connector 2013 im Vergleich zu Outlook Social Connector 1.1.
  
|**Funktion**|**Outlook Connector für soziale Netzwerke 2013**|**Outlook Connector für soziale Netzwerke 1.1**|
|:-----|:-----|:-----|
|End-Benutzeroberfläche  <br/> |SharePoint Server, SharePoint-Arbeitsbereich Lync-Client, Visitenkarte in allen Office-Clientanwendungen und Personenbereich in Outlook  <br/> |Personenbereich in Outlook  <br/> |
|Standardauthentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Formularbasierte Authentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Zwischengespeicherte Authentifizierung  <br/> |Ja  <br/> |Ja  <br/> |
|Zwischengespeicherte Sync für Freunde Ordner Kontakte auf Standard speichern  <br/> |Ja  <br/> |Ja  <br/> |
|Zwischengespeicherte Aktivitäten Sync für Freunde in ausgeblendeten **Newsfeed** -Ordner  <br/> |Nein  <br/> |Ja  <br/> |
|Bedarfsgesteuerten Synchronisierung (Bild, Name, Titel) für Freunde und Familie Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Synchronisierung für Freunde und Familie Netzwerk Aktivitäten auf Abruf  <br/> |Ja  <br/> |Ja  <br/> |
|Führen Sie auf Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Führen Sie nicht auf das Netzwerk  <br/> |Ja  <br/> |Ja  <br/> |
|Besuchen Sie die Profilseite des Benutzers  <br/> |Über einen link  <br/> |Über ein Netzwerk-Logo  <br/> |
|Beobachten datenschutzeinstellungen für soziale Netzwerke (z. B. Anzeige Profil und Aktivitäten nicht Freunde ist, die Wiedergabe einer solchen zulassen)  <br/> |Ja  <br/> |Ja  <br/> |
|Hash e-Mail-Adressen an Anbieter übergeben  <br/> |Ja  <br/> |Ja  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Änderungen aus der vorherigen Version der Erweiterbarkeit des OSC-Providers

In der folgenden Tabelle werden die Member, die von der entsprechenden Schnittstelle veraltet oder hinzugefügt wurden.
  
|**Schnittstelle und member**|**Kommentar**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |In Outlook Connector für soziale Netzwerke 2013 veraltet. Beachten Sie, dass **ISocialSession::GetActivities** auch seit Outlook Social Connector 1.1 veraltet ist.  <br/> Zum Synchronisieren von Aktivitätsfeeds, sollten Sie die Methode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) implementieren. Legen Sie **DynamicActivitiesLookupEx** als **true**die OSC **ISocialSession2::GetActivitiesEx** stattdessen aufzurufen aufgefordert wird.  <br/> |
   
Die folgende Tabelle enthält die Schemaelemente, die geändert wurden.
  
|**Schemaelement**|**Kommentar**|
|:-----|:-----|
|**Funktionen** <br/> |In Outlook Social Connector 2013 hinzugefügt: **AllowChangesToAutoConfigure** -Element.  <br/> Veraltet in Outlook Social Connector 2013: **CacheActivities** -Element.  <br/> |
|**Person** <br/> |In Outlook Social Connector 2013 hinzugefügt: **Askmeabout**, **BusinessAddress**, **BusinessCity**, **BusinessCountryOrRegion**, **BusinessState**, **BusinessZip**, **Branchen**, **Interessen**, ** Speicherort**, **OtherAddress**, **OtherCity**, **OtherCountryOrRegion**, **OtherState**, **OtherZip**, **Fähigkeiten**, **Schulen**und **Website** -Elemente.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [XML-Code für Funktionen](xml-for-capabilities.md)
- [XML-Code für Freunde](xml-for-friends.md)
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

