---
title: Synchronisieren von Freunden und Aktivitäten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Das Outlook Social Connector (OSC) unterstützt das Anzeigen von Informationen aus einem sozialen Netzwerk zu einer Person auf der Visitenkarte oder im bereich Outlook Personenbereich. SharePoint Server, SharePoint Arbeitsbereich, Lync-Client und alle Office Clientanwendungen, die Anwesenheitsinformationen unterstützen, unterstützen die Visitenkarte.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329201"
---
# <a name="synchronizing-friends-and-activities"></a>Synchronisieren von Freunden und Aktivitäten

Das Outlook Social Connector (OSC) unterstützt das Anzeigen von Informationen aus einem sozialen Netzwerk zu einer Person auf der Visitenkarte oder im bereich Outlook Personenbereich. SharePoint Server, SharePoint Arbeitsbereich, Lync-Client und alle Office Clientanwendungen, die Anwesenheitsinformationen unterstützen, unterstützen die Visitenkarte.
  
Sie können die Visitenkarte in Szenarien für die Zusammenarbeit in Office verwenden, um mehr über die Personen zu erfahren, mit denen Sie zusammenarbeiten. Beispiele für diese Szenarien sind Messaging in Outlook und die co-Authoring eines Dokuments in Word. Wenn Sie auf die Registerkarte **Neue Informationen** einer Visitenkarte klicken, werden Informationen zu dieser Person angezeigt. 
  
Im Outlook Personenbereich werden Informationen zu einer Person angezeigt, die ein Absender oder Empfänger eines ausgewählten Outlook sein kann. Wenn Sie eine andere Person im Personenbereich oder ein anderes Element im Outlook-Explorer auswählen oder ein Outlook-Element in einem Inspektor öffnen, aktualisiert der Outlook Social Connector (OSC) den Personenbereich. 
  
Damit für die Visitenkarte oder den Personenbereich aktuelle Informationen für die ausgewählte Person angezeigt werden, synchronisiert das OSC diese Informationen über die OSC-Anbieter und eine Art Zwischenspeicherung. Diese Synchronisierung hängt von den auf dem Clientcomputer installierten OSC-Anbietern, den sozialen Netzwerken, die Sie über ihre OSC-Anbieter angemeldet haben, und dem Synchronisierungsmodus ab, den jeder der OSC-Anbieter für diese sozialen Netzwerke unterstützt.
  
Das OSC unterstützt die Synchronisierung von Freunden, Nicht-Freunden und Aktivitäten für Freunde und Nicht-Freunde auf unterschiedliche Weise: zwischengespeicherte Synchronisierung, Bedarfssynchronisierung und Hybridsynchronisierung. Der Hauptunterschied zwischen diesen Synchronisierungsmodi besteht in der Speicherung der Daten durch das OSC – sei es in einem Ordner im Standardspeicher des Benutzers Outlook oder im Arbeitsspeicher auf dem Computer des Benutzers. Wie in diesem Thema erwähnt, gibt es in jedem Fall eine standardmäßige Mindestzeit, bis die Daten im Ordner oder Speicher bleiben, bevor die Daten aktualisiert werden. In einigen Fällen kann die Mindestzeit durch Gruppenrichtlinien angepasst werden. Weitere Informationen zu Gruppenrichtlinien, die das Verhalten des Betriebssystems steuern, finden Sie unter [How to manage the Outlook Social Connector by using Group Policy](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Beachten Sie, dass, wenn die ausgewählte Person kein Mitglied des sozialen Netzwerks ist, vom OSC keine Personen- oder Aktivitätsinformationen für diese Person im Bereich Visitenkarte oder Personen angezeigt werden.
  
## <a name="cached-synchronization"></a>Zwischengespeicherte Synchronisierung

Ein OsC-Anbieter kann Informationen für Freunde im sozialen Netzwerk in einem bestimmten Ordner im standard-Outlook-Speicher des Benutzers speichern und diesen Cache regelmäßig aktualisieren, nachdem eine bestimmte Zeit abgelaufen ist. Das Zwischenspeichern von Informationen in einem Ordner hat den Vorteil, dass der Datenverkehr zum sozialen Netzwerk reduziert wird.
  
> [!NOTE]
> Ab Outlook Social Connector 2013 unterstützt das OSC keine zwischengespeicherte Synchronisierung von Aktivitäten mehr. 
  
### <a name="cached-synchronization-of-friends"></a>Zwischengespeicherte Synchronisierung von Freunden

Wenn ein OSC-Anbieter die zwischengespeicherte Synchronisierung für Freunde unterstützt, speichert das OSC Informationen für Freunde des angemeldeten Benutzers im sozialen Netzwerk zwischen. Die Informationen werden in einem Outlook zwischengespeichert, der für dieses soziale Netzwerk im Standardspeicher des Benutzers Outlook ist. Der Name des Kontaktordners basiert auf dem Namen des sozialen Netzwerks, das das OSC mithilfe der [ISocialProvider::SocialNetworkName-Eigenschaft](isocialprovider-socialnetworkname.md) erhält. 
  
In der zwischengespeicherten Synchronisierung speichert das OSC Informationen nur für die Freunde des angemeldeten Benutzers im sozialen Netzwerk. Das OSC hat keinen Zugriff auf Informationen für Nicht-Freunde.
  
Das Standardintervall für das OSC zum Aktualisieren des Kontaktordners für Freundesinformationen aus dem sozialen Netzwerk ist einmal pro Tag (oder einmal pro 1440 Minuten). Dieses Aktualisierungsintervall kann auch nach Gruppenrichtlinien festgelegt werden, wie am Anfang dieses Themas erläutert.
  
Wenn während einer Aktualisierung ein Fehler auftritt, wird der OsC in einem Intervall erneut ausgeführt,  das durch das **contactSyncRestartInterval-Element** in der Funktionen-XML angegeben wird. Dieses Wiederholungsintervall hat einen Standardwert von 30 Minuten und kann auch durch Gruppenrichtlinien festgelegt werden. 
  
Wenn ein Benutzer eine Visitenkarte öffnet  und die Registerkarte  Neues auswählt, wird die Registerkarte Neues aktualisiert. Wenn ein Benutzer Outlook ein Element in Outlook oder eine Person im Personenbereich erneut auswählt, wird der Personenbereich aktualisiert. Wenn das Cacheaktualisierungsintervall nicht abgelaufen ist, ruft das Betriebssystem den Cache auf, um Informationen für den ausgewählten Benutzer zu erhalten. Dadurch wird der Aufwand für den Zugriff auf das soziale Netzwerk durch die Verwendung der Erweiterbarkeit des OSC-Anbieters vermieden. Wenn das Aktualisierungsintervall abgelaufen ist, ruft das OSC die [ISocialPerson::GetFriendsAndColleagues-Methode](isocialperson-getfriendsandcolleagues.md) auf, um aktuelle Freundesinformationen für den angemeldeten Benutzer zu erhalten, und aktualisiert den Cache im Kontaktordner. 
  
Der OSC-Anbieter informiert das OSC darüber, dass er die zwischengespeicherte Synchronisierung von Freunden unterstützt, indem er die folgenden Elemente in der Xml-Funktion **der Funktionen** an gibt: 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **false**
    
## <a name="on-demand-synchronization"></a>On-Demand-Synchronisierung

Wenn ein Benutzer  die Registerkarte Neues in einer Visitenkarte auswählt oder ein anderes Outlook-Element oder eine andere Person im Personenbereich in Outlook auswählt, aktualisiert das OSC die Visitenkarte bzw. den Personenbereich. Wenn ein OSC-Anbieter die on-demand-Synchronisierung von Personen oder Aktivitäten unterstützt, synchronisiert sich das OSC mit einem Cache im Arbeitsspeicher und aktualisiert Details wie Name, Titel, Bild und Aktivitätsstreams auf der Visitenkarte oder im Personenbereich. Bei der On-Demand-Synchronisierung versucht das OSC im Gegensatz zur zwischengespeicherten Synchronisierung, die Informationen für die Person zu aktualisieren, unabhängig davon, ob es sich bei dieser Person um einen Freund oder einen Nichtfreund des angemeldeten Benutzers im sozialen Netzwerk handelt. 
  
On-Demand Person (or activity) data is stored in memory only. Die Speicherdaten werden beim Herunterfahren der Office-Clientanwendung oder beim Aktualisieren der Visitenkarte oder des Personenbereichs durch den Benutzer geräumt, und die Daten bleiben länger als das Aktualisierungsintervall im Arbeitsspeicher. Beachten Sie, dass die Aktualisierung aus dem sozialen Netzwerk immer von einem Benutzer initiiert wird, der die Visitenkarte oder den Personenbereich aktualisiert (z. B. durch Auswählen eines anderen Benutzers im Personenbereich oder Durch auswählen eines anderen Elements im Outlook Explorerfenster). 

Das Gegenteil ist jedoch nicht immer der Fall, da nicht bei jeder Aktualisierung der Visitenkarte oder des Personenbereichs eine Aktualisierung aus dem sozialen Netzwerk notwendig ist. Wenn der Benutzer die Visitenkarte oder den Personenbereich aktualisiert und die Personendaten (oder Aktivitätsdaten) länger als das Aktualisierungsintervall im Arbeitsspeicher gespeichert sind, ruft das OSC [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (oder [ISocialSession2::GetActivitiesEx)](isocialsession2-getactivitiesex.md)auf, um die Informationen im Arbeitsspeicher aus dem sozialen Netzwerk zu aktualisieren. Der zulässige Zeitraum für Freundes- und Freundesinformationen im Arbeitsspeicher beträgt 24 Stunden und für Aktivitäten 30 Minuten. 
  
Ein wichtiger Unterschied zwischen zwischengespeicherter und on-Demand-Synchronisierung ist, dass die On-Demand-Synchronisierung Personen- und Aktivitätsinformationen für Freunde und Nicht-Freunde im Netzwerk abrufen kann. Wenn die ausgewählte Person kein Freund ist, aktualisiert das OSC Informationen und Aktivitäten für diese Person, wenn eine der folgenden Anforderungen erfüllt ist: 
  
- Die Person ist ein Benutzer im sozialen Netzwerk und ermöglicht die öffentliche Anzeige von Profil- und Aktivitätsinformationen.
    
- Die Person befindet sich im selben Netzwerk wie der angemeldete Benutzer in diesem sozialen Netzwerk (z. B. im gleichen Netzwerk für Uni-Absolventen).
    
Die On-Demand-Synchronisierung von Personen und Aktivitäten führt zu weiteren Anrufen an den Anbieter aus dem OSC-Kernmodul. Soziale Netzwerke müssen in der Lage sein, die erhöhten Bandbreitenanforderungen der On-Demand-Synchronisierung zu bewältigen.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Angeben von XML-Elementen für die Bedarfssynchronisierung

Der OSC-Anbieter informiert das OSC darüber, dass er die On-Demand-Synchronisierung  von Freunden und Nicht-Freunden unterstützt, indem er die folgenden Elemente in der Funktionen-XML anfordert: 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **false**
    
- **dynamicContactsLookup**  =  **true**
    
Der OSC-Anbieter informiert das OSC darüber, dass es die On-Demand-Synchronisierung von Aktivitäten unterstützt, indem die folgenden Elemente in der Xml-Funktion **angegeben** werden: 
  
- **getActivities**  =  **true**
    
- **cacheActivities**  =  **false**
    
- **dynamicActivitiesLookupEx**  =  **true**
    
## <a name="hybrid-synchronization"></a>Hybridsynchronisierung

Ein OSC-Anbieter kann die Hybridsynchronisierung von Freunden und Nicht-Freunden unterstützen. Dies kann die Anrufe zwischen dem OSC-Kernmodul und dem OSC-Anbieter, die Anrufe an das soziale Netzwerk für die on-demand-Synchronisierung von Freunden und die Währung der Freundesdaten optimieren. Die Mindestzeit, für die die Daten in einem Ordner oder Speicher verbleiben können, ist ggf. identisch mit den Grenzwerten in zwischengespeicherten Synchronisierungsmodi oder bei Bedarf.
  
> [!NOTE]
> Ab Outlook Social Connector 2013 unterstützt das OSC nur die On-Demand-Synchronisierung von Aktivitäten und keine Hybridsynchronisierung von Aktivitäten mehr. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Hybridsynchronisierung von Freunden und Nicht-Freunden

Wenn ein OSC-Anbieter die Hybridsynchronisierung von Freunden und Nicht-Freunden unterstützt, führt das OSC die folgenden Schritte aus: 
  
- Das OSC speichert Informationen für Freunde des angemeldeten Benutzers im kontaktspezifischen Kontaktordner für soziale Netzwerke.
    
- Das OSC speichert Informationen für Nicht-Freunde des angemeldeten Benutzers im Arbeitsspeicher.
    
Der OSC-Anbieter informiert das OSC darüber, dass er die Hybridsynchronisierung von Freunden und Nicht-Freunden unterstützt, indem er die folgenden Elemente in der Xml-Funktion der Funktionen an die folgenden Elemente ankn?nnen:  
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **true**
    
## <a name="synchronization-intervals"></a>Synchronisierungsintervalle

In der folgenden Tabelle sind die Synchronisierungsintervalle für Freunde und Nicht-Freunde-Informationen zwischen dem entsprechenden Cache (Ordner oder Arbeitsspeicher) und dem sozialen Netzwerk in Abhängigkeit vom unterstützten Synchronisierungsmodus zusammengefasst. Informationen zum Hybridsynchronisierungsmodus finden Sie in den Zeilen für den zwischengespeicherten Modus für Freunde und in der Zeile für den On-Demand-Modus für Nicht-Freunde.
  
|**Synchronisierungsmodus für Personen**|**Festlegen des Aktualisierungsintervalls**|**Standardmäßige Mindestzeit vor der Aktualisierung**|**Außerkraftsetzung von Gruppenrichtlinien**|
|:-----|:-----|:-----|:-----|
|Cached  <br/> |Innerhalb von OSC festgelegt  <br/> |1440 Minuten (24 Stunden)  <br/> |Windows Registrierungswert **NetContactSyncInterval** <br/> |
|Cached  <br/> |**contactSyncRestartInterval-Element** in **Capabilities** XML  <br/> |30 Minuten, **wenn contactSyncRestartInterval** nicht festgelegt ist  <br/> |Windows Registrierungswert **contactSyncRestartInterval** <br/> |
|On-Demand  <br/> |Innerhalb von OSC festgelegt  <br/> |1440 Minuten (24 Stunden)  <br/> |Windows Registrierungswert **OnlineSearchExpiryTime** <br/> |
   
In der folgenden Tabelle sind die Synchronisierungsintervalle für Aktivitäten von Freunden und Nicht-Freunden zwischen dem entsprechenden Cache (Ordner oder Arbeitsspeicher) und dem sozialen Netzwerk in Abhängigkeit von den unterstützten Synchronisierungsmodi zusammengefasst. 
  
|**Synchronisierungsmodus für Aktivitäten**|**Festlegen des Aktualisierungsintervalls**|**Standardmäßige Mindestzeit vor der Aktualisierung**|**Außerkraftsetzung von Gruppenrichtlinien**|
|:-----|:-----|:-----|:-----|
|On-Demand  <br/> |Innerhalb von OSC festgelegt  <br/> |30 Minuten  <br/> |Windows Registrierungswert **OnlineSearchExpiryTime** <br/> |
   
Die folgenden Informationen gelten für die Windows registrierungswerte, die in den beiden Tabellen aufgeführt sind:
  
- Schlüssel:  `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Wert: DWORD-Wert zwischen 1 und 10080
    
## <a name="see-also"></a>Siehe auch

- [Capabilities XML(Beispiel)](capabilities-xml-example.md)  
- [XML für Funktionen](xml-for-capabilities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [So verwalten Sie den Outlook Connector für soziale Netzwerke mithilfe von Gruppenrichtlinien](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

