---
title: Synchronisieren von Freunden und Aktivitäten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Der Outlook Connector für soziale Netzwerke (OSC) unterstützt die Anzeige von Informationen aus einem sozialen Netzwerk über eine Person in der VisitenKarte oder im Outlook-Personen Bereich. SharePoint Server, SharePoint Workspace, lync-Client und alle Office-Clientanwendungen, die Anwesenheitsinformationen unterstützen, unterstützen die VisitenKarte.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329201"
---
# <a name="synchronizing-friends-and-activities"></a>Synchronisieren von Freunden und Aktivitäten

Der Outlook Connector für soziale Netzwerke (OSC) unterstützt die Anzeige von Informationen aus einem sozialen Netzwerk über eine Person in der VisitenKarte oder im Outlook-Personen Bereich. SharePoint Server, SharePoint Workspace, lync-Client und alle Office-Clientanwendungen, die Anwesenheitsinformationen unterstützen, unterstützen die VisitenKarte.
  
Sie können die VisitenKarte in Zusammenarbeitsszenarien in Office-Anwendungen verwenden, um mehr über die Personen zu erfahren, mit denen Sie zusammenarbeiten. Beispiele für diese Szenarien sind Messaging in Outlook und die gemeinsame Dokumenterstellung in Word. Wenn Sie auf die **** Registerkarte Neuerungen einer Visitenkarte klicken, werden Informationen zu dieser Person angezeigt. 
  
Im Bereich Outlook-Personen werden Informationen zu einer Person angezeigt, die ein Absender oder Empfänger eines Outlook-Elements sein kann, das Sie ausgewählt haben. Wenn Sie eine andere Person im Personen Bereich oder ein anderes Element im Outlook-Explorer auswählen oder ein Outlook-Element in einem Inspektor öffnen, aktualisiert der Outlook Connector für soziale Netzwerke den Bereich Personen. 
  
Damit die Kontaktkarte oder der Personen Bereich aktuelle Informationen für die ausgewählte Person anzeigt, synchronisiert der OSC diese Informationen über die OSC-Anbieter und eine Art Zwischenspeicherung. Diese Synchronisierung hängt von den OSC-Anbietern ab, die auf dem Clientcomputer installiert sind, den sozialen Netzwerken, die Sie über Ihre OSC-Anbieter angemeldet haben, und dem Synchronisierungsmodus, den jeder OSC-Anbieter für diese sozialen Netzwerke unterstützt.
  
OSC unterstützt die Synchronisierung von Freunden, nicht-Freunden und Aktivitäten für Freunde und nicht-Freunde auf unterschiedliche Art und Weise: zwischengespeicherte Synchronisierung, on-Demand-Synchronisierung und Hybrid Synchronisierung. Der Hauptunterschied zwischen diesen Synchronisierungs Modi besteht darin, dass OSC die Daten speichert, unabhängig davon, ob Sie sich in einem Ordner im Outlook-Standardspeicher des Benutzers oder im Arbeitsspeicher auf dem Computer des Benutzers befinden. In jedem Fall, wie in diesem Thema beschrieben, gibt es eine standardmäßige Mindestzeit, die die Daten im Ordner oder im Arbeitsspeicher verbleiben, bevor die Daten aktualisiert werden. In einigen Fällen kann die minimale Zeitdauer durch Gruppenrichtlinien angepasst werden. Weitere Informationen zu Gruppenrichtlinien, die das Verhalten des OSC steuern, finden Sie unter [Verwalten des Outlook Connectors für soziale Netzwerke mithilfe von Gruppenrichtlinien](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Beachten Sie, dass der OSC keine Personen-oder Aktivitätsinformationen für diese Person auf der VisitenKarte oder im Personen Bereich anzeigt, wenn die ausgewählte Person kein Mitglied des sozialen Netzwerks ist.
  
## <a name="cached-synchronization"></a>Zwischengespeicherte Synchronisierung

Ein OSC-Anbieter kann Informationen für Freunde im sozialen Netzwerk in einem bestimmten Ordner im Outlook-Standardspeicher des Benutzers speichern und diesen Cache in regelmäßigen Abständen nach Ablauf einer bestimmten Zeitspanne aktualisieren. Das Zwischenspeichern von Informationen in einem Ordner hat den Vorteil, dass der Datenverkehr zum sozialen Netzwerk reduziert wird.
  
> [!NOTE]
> Beginnend mit Outlook Social Connector 2013 unterstützt OSC die zwischengespeicherte Synchronisierung von Aktivitäten nicht mehr. 
  
### <a name="cached-synchronization-of-friends"></a>Zwischengespeicherte Synchronisierung von Freunden

Wenn ein OSC-Anbieter die zwischengespeicherte Synchronisierung für Freunde unterstützt, speichert der OSC Informationen für Freunde des angemeldeten Benutzers im sozialen Netzwerk. Die Informationen werden in einem Outlook-Kontakteordner zwischengespeichert, der für das soziale Netzwerk im Outlook-Standardspeicher des Benutzers spezifisch ist. Der Name des Ordners "Kontakte" basiert auf dem Namen des sozialen Netzwerks, das der OSC mithilfe der [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) -Eigenschaft abruft. 
  
In der zwischengespeicherten Synchronisierung speichert OSC Informationen nur für die Freunde des angemeldeten Benutzers im sozialen Netzwerk. Der OSC greift nicht auf Informationen für nicht-Freunde zu.
  
Das Standardintervall für OSC zum Aktualisieren des Kontakteordners für die Informationen der Freunde aus dem sozialen Netzwerk ist einmal pro Tag (oder einmal pro 1440 Minuten). Dieses Aktualisierungsintervall kann auch mithilfe von Gruppenrichtlinien festgelegt werden, wie am Anfang dieses Themas erläutert.
  
Wenn während einer Aktualisierung ein Fehler auftritt, versucht der OSC in einem Intervall, das vom **contactSyncRestartInterval** -Element im **Capabilities** -XML angegeben wird, erneut. Dieses Wiederholungsintervall hat den Standardwert 30 Minuten und kann auch durch Gruppenrichtlinien festgelegt werden. 
  
Wenn ein Benutzer eine VisitenKarte öffnet und die Registerkarte **Neuerungen** auswählt, **** wird die Registerkarte Neuigkeiten aktualisiert. Wenn ein Outlook-Benutzer ein Element in Outlook erneut wählt oder eine Person im Personen Bereich erneut ausgewählt wird, wird der Bereich Personen aktualisiert. Wenn das Cacheaktualisierungsintervall nicht abgelaufen ist, wechselt der OSC zum Cache, um Informationen für den ausgewählten Benutzer abzurufen. Dadurch wird der Aufwand bei der Verwendung der OSC-Anbieter Erweiterbarkeit für den Zugriff auf das soziale Netzwerk vermieden. Wenn das Aktualisierungsintervall abgelaufen ist, ruft der OSC die [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode auf, um aktuelle Freundes Informationen für den angemeldeten Benutzer abzurufen, und aktualisiert den Cache im Ordner Kontakte. 
  
Der OSC-Anbieter informiert OSC, dass er die zwischengespeicherte Synchronisierung von Freunden unterstützt, indem er die folgenden Elemente im **Capabilities** -XML angibt: 
  
- **** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **false**
    
## <a name="on-demand-synchronization"></a>Bedarfsgesteuerte Synchronisierung

Wenn ein Benutzer die Register **** Karte Neuerungen in einer Visitenkarte auswählt oder ein anderes Outlook-Element oder eine andere Person im Personen Bereich in Outlook auswählt, aktualisiert der osc die Visitenkarte oder den Personen Bereich. Wenn ein OSC-Anbieter die on-Demand-Synchronisierung von Personen oder Aktivitäten unterstützt, synchronisiert der OSC mit einem Cache im Arbeitsspeicher und aktualisiert Details wie Name, Titel, Bild und Aktivitätsdaten Ströme im Kontakt-oder Personen Bereich. Für die on-Demand-Synchronisierung versucht der OSC im Gegensatz zur zwischengespeicherten Synchronisierung, die Informationen für die Person zu aktualisieren, unabhängig davon, ob es sich um einen Freund oder nicht-Freund des angemeldeten Benutzers im sozialen Netzwerk handelt. 
  
On-Demand-Person (oder Activity)-Daten werden nur im Arbeitsspeicher gespeichert. Die speicherresidenten Daten werden gelöscht, wenn die Office-Clientanwendung heruntergefahren wird, oder der Benutzer bewirkt eine Aktualisierung der VisitenKarte oder des Personen Bereichs, und die Daten sind länger im Speicher als das Aktualisierungsintervall. Beachten Sie, dass die Aktualisierung aus dem sozialen Netzwerk immer von einem Benutzer initiiert wird, der die VisitenKarte oder den Personen Bereich aktualisiert (beispielsweisedurch auswählen eines anderen Benutzers im Personen Bereich oder Auswählen eines anderen Elements im Outlook-Explorer-Fenster). 

Allerdings ist die umgekehrte nicht immer true-nicht jede Aktualisierung der VisitenKarte oder des Personen Bereichs zwangsläufig eine Aktualisierung aus dem sozialen Netzwerk. Wenn der Benutzer die VisitenKarte oder den Personen Bereich aktualisiert und die Person (oder die Aktivitätsdaten) länger im Speicher als das Aktualisierungsintervall verstrichen ist, ruft OSC [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) (oder [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)) auf Aktualisieren Sie die Informationen im Arbeitsspeicher aus dem sozialen Netzwerk. Der zulässige Zeitraum für Freundes-und nicht-Friend-Informationen im Arbeitsspeicher beträgt 24 Stunden und für Aktivitäten 30 Minuten. 
  
Ein wichtiger Unterschied zwischen zwischengespeicherter und on-Demand-Synchronisierung besteht darin, dass die bedarfsgesteuerte Synchronisierung Personen-und Aktivitätsinformationen für Freunde und nicht-Freunde im Netzwerk abrufen kann. Wenn die ausgewählte Person ein nicht-Friend ist, aktualisiert der OSC Informationen und Aktivitäten für diese Person, wenn eine der folgenden Anforderungen erfüllt ist: 
  
- Die Person ist ein Benutzer im sozialen Netzwerk und ermöglicht die öffentliche Anzeige von Profil-und Aktivitätsinformationen.
    
- Die Person befindet sich im selben Netzwerk wie der angemeldete Benutzer in diesem sozialen Netzwerk (beispielsweise im gleichen Netzwerk für Hochschulabsolventen).
    
Die on-Demand-Synchronisierung von Personen und Aktivitäten führt zu weiteren anrufen des Anbieters vom OSC-Kern Modul. Soziale Netzwerke müssen in der Lage sein, die erhöhten Bandbreitenanforderungen bei der bedarfsgesteuerten Synchronisierung zu bewältigen.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Angeben von XML-Elementen für die bedarfsgesteuerte Synchronisierung

Der OSC-Anbieter informiert den OSC, dass er die bedarfsgesteuerte Synchronisierung von Freunden und nicht-Freunden unterstützt, indem er die folgenden Elemente im **Capabilities** -XML angibt: 
  
- **** = **true**
    
- **cacheFriends** = **false**
    
- **dynamicContactsLookup** = **true**
    
Der OSC-Anbieter informiert OSC, dass die bedarfsgesteuerte Synchronisierung von Aktivitäten unterstützt wird, indem die folgenden Elemente im XML- **Funktions** Umfang angegeben werden: 
  
- **GetActivities** = (**true** )
    
- **cacheActivities** = **false**
    
- **dynamicActivitiesLookupEx** = **true**
    
## <a name="hybrid-synchronization"></a>Hybrid Synchronisierung

Ein OSC-Anbieter kann die Hybrid Synchronisierung von Freunden und nicht-Freunden unterstützen. Dies kann die Aufrufe zwischen dem OSC-Kern Modul und dem OSC-Anbieter, den Anrufen an das soziale Netzwerk für die bedarfsgesteuerte Synchronisierung von Freunden und der Währung der Freundes Daten optimieren. Die Mindestzeitdauer, die die Daten in einem Ordner oder Arbeitsspeicher verbleiben können, ist identisch mit den Grenzwerten im zwischengespeicherten Modus oder bei Anforderungs Synchronisierungs Modi.
  
> [!NOTE]
> Beginnend mit Outlook Social Connector 2013 unterstützt OSC nur die bedarfsgesteuerte Synchronisierung von Aktivitäten und unterstützt nicht mehr die Hybrid Synchronisierung von Aktivitäten. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Hybrid Synchronisierung von Freunden und nicht-Freunden

Wenn ein OSC-Anbieter die Hybrid Synchronisierung von Freunden und nicht-Freunden unterstützt, führt der OSC folgende Aktionen aus: 
  
- OSC speichert Informationen für Freunde des angemeldeten Benutzers im sozialen netzwerkspezifischen Kontaktordner.
    
- OSC speichert Informationen für nicht-Freunde des angemeldeten Benutzers im Arbeitsspeicher.
    
Der OSC-Anbieter informiert OSC, dass er die Hybrid Synchronisierung von Freunden und nicht-Freunden unterstützt, indem er die folgenden Elemente im **Capabilities** -XML angibt: 
  
- **** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **true**
    
## <a name="synchronization-intervals"></a>Synchronisierungsintervalle

In der folgenden Tabelle werden die Synchronisierungsintervalle für Freunde und nicht-Freunde-Informationen zwischen dem entsprechenden Cache (Ordner oder Arbeitsspeicher) und dem sozialen Netzwerk in Abhängigkeit vom unterstützten Synchronisierungsmodus zusammengefasst. Informationen für den Modus für die Hybrid Synchronisierung finden Sie in den Zeilen für den Cache-Modus für Freunde und die Zeile für den on-Demand-Modus für nicht-Freunde.
  
|**Synchronisierungsmodus für Personen**|**Aktualisierungsintervall festgelegt**|**Standard Mindestzeit vor der Aktualisierung**|**Überschreibung von Gruppenrichtlinien**|
|:-----|:-----|:-----|:-----|
|Cached  <br/> |In OSC festlegen  <br/> |1440 Minuten (24 Stunden)  <br/> |Windows-Registrierungswert **NetContactSyncInterval** <br/> |
|Cached  <br/> |**contactSyncRestartInterval** -Element in **Capabilities** -XML  <br/> |30 Minuten, wenn **contactSyncRestartInterval** nicht festgelegt ist  <br/> |Windows-Registrierungswert **contactSyncRestartInterval** <br/> |
|Bei Bedarf  <br/> |In OSC festlegen  <br/> |1440 Minuten (24 Stunden)  <br/> |Windows-Registrierungswert **OnlineSearchExpiryTime** <br/> |
   
In der folgenden Tabelle werden die Synchronisierungsintervalle für Aktivitäten von Freunden und nicht-Freunden zwischen dem entsprechenden Cache (Ordner oder Arbeitsspeicher) und dem sozialen Netzwerk in Abhängigkeit von den unterstützten Synchronisierungs Modi zusammengefasst. 
  
|**Synchronisierungsmodus für Aktivitäten**|**Aktualisierungsintervall festgelegt**|**Standard Mindestzeit vor der Aktualisierung**|**Überschreibung von Gruppenrichtlinien**|
|:-----|:-----|:-----|:-----|
|Bei Bedarf  <br/> |In OSC festlegen  <br/> |30 Minuten  <br/> |Windows-Registrierungswert **OnlineSearchExpiryTime** <br/> |
   
Die folgenden Informationen gelten für die in den beiden Tabellen aufgeführten Windows-Registrierungswerte:
  
- Schlüssel`HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Wert: DWORD-Wert zwischen 1 und 10080
    
## <a name="see-also"></a>Siehe auch

- [XML-Beispiel für Funktionen](capabilities-xml-example.md)  
- [XML für Funktionen](xml-for-capabilities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [So verwalten Sie den Outlook Connector für soziale Netzwerke mithilfe von Gruppenrichtlinien](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

