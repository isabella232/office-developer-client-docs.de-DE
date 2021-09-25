---
title: Synchronisieren von Freunden und Aktivitäten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Der Outlook Connector für soziale Netzwerke (OSC) unterstützt das Anzeigen von Informationen aus einem sozialen Netzwerk zu einer Person auf der Visitenkarte oder im Outlook Personenbereich. SharePoint Server, SharePoint Workspace, Lync-Client und alle Office-Clientanwendungen, die Anwesenheitsinformationen unterstützen, unterstützen die Visitenkarte.
ms.openlocfilehash: f86441e18697de26fe41cc7b680c85abb28ec27f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604075"
---
# <a name="synchronizing-friends-and-activities"></a>Synchronisieren von Freunden und Aktivitäten

Der Outlook Connector für soziale Netzwerke (OSC) unterstützt das Anzeigen von Informationen aus einem sozialen Netzwerk zu einer Person auf der Visitenkarte oder im Outlook Personenbereich. SharePoint Server, SharePoint Workspace, Lync-Client und alle Office-Clientanwendungen, die Anwesenheitsinformationen unterstützen, unterstützen die Visitenkarte.
  
Sie können die Visitenkarte in Szenarien für die Zusammenarbeit in Office Anwendungen verwenden, um mehr über die Personen zu erfahren, mit denen Sie zusammenarbeiten. Beispiele für diese Szenarien sind Messaging in Outlook und die gemeinsame Dokumenterstellung in Word. Wenn Sie auf die Registerkarte **"Neuigkeiten"** einer Visitenkarte klicken, werden Informationen zu dieser Person angezeigt. 
  
Der Outlook Personenbereich zeigt Informationen zu einer Person an, die ein Absender oder Empfänger eines ausgewählten Outlook Elements sein kann. Wenn Sie eine andere Person im Personenbereich oder ein anderes Element im Outlook Explorer auswählen oder ein Outlook Element in einem Inspektor öffnen, aktualisiert der Outlook Connector für soziale Netzwerke (OSC) den Personenbereich. 
  
Damit die Visitenkarte oder der Personenbereich aktuelle Informationen für die ausgewählte Person anzeigen kann, synchronisiert osc diese Informationen über die OSC-Anbieter und eine Art der Zwischenspeicherung. Diese Synchronisierung hängt von den OSC-Anbietern ab, die auf dem Clientcomputer installiert sind, den sozialen Netzwerken, bei denen Sie sich über ihre OSC-Anbieter angemeldet haben, und dem Synchronisierungsmodus, den jeder OSC-Anbieter für diese sozialen Netzwerke unterstützt.
  
Das OSC unterstützt die Synchronisierung von Freunden, Nicht-Freunden und Aktivitäten für Freunde und Nicht-Freunde auf unterschiedliche Weise: zwischengespeicherte Synchronisierung, Bedarfssynchronisierung und Hybridsynchronisierung. Der Hauptunterschied zwischen diesen Synchronisierungsmodi besteht darin, wo der OSC die Daten speichert– ob sie sich in einem Ordner im Standardspeicher Outlook des Benutzers oder im Arbeitsspeicher auf dem Computer des Benutzers befinden. In jedem Fall, wie in diesem Thema erwähnt, gibt es eine standardmäßige Mindestzeit, in der die Daten im Ordner oder Arbeitsspeicher verbleiben, bevor die Daten aktualisiert werden. In einigen Fällen kann die minimale Zeitdauer durch gruppenrichtlinien angepasst werden. Weitere Informationen zu Gruppenrichtlinien, die das Verhalten des OSC steuern, finden Sie unter [Verwalten des Outlook Connector für soziale Netzwerke mithilfe von Gruppenrichtlinien.](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)
  
Beachten Sie, dass, wenn die ausgewählte Person kein Mitglied des sozialen Netzwerks ist, der OSC keine Personen- oder Aktivitätsinformationen für diese Person in der Visitenkarte oder im Personenbereich anzeigt.
  
## <a name="cached-synchronization"></a>Zwischengespeicherte Synchronisierung

Ein OSC-Anbieter kann Informationen für Freunde im sozialen Netzwerk in einem bestimmten Ordner im Standardspeicher Outlook des Benutzers speichern und diesen Cache nach Ablauf einer bestimmten Zeit regelmäßig aktualisieren. Das Zwischenspeichern von Informationen in einem Ordner hat den Vorteil, dass der Datenverkehr zum sozialen Netzwerk reduziert wird.
  
> [!NOTE]
> Ab Outlook Connector für soziale Netzwerke 2013 unterstützt osc die zwischengespeicherte Synchronisierung von Aktivitäten nicht mehr. 
  
### <a name="cached-synchronization-of-friends"></a>Zwischengespeicherte Synchronisierung von Freunden

Wenn ein OSC-Anbieter die zwischengespeicherte Synchronisierung für Freunde unterstützt, speichert der OSC Informationen für Freunde des angemeldeten Benutzers im sozialen Netzwerk zwischen. Die Informationen werden in einem Outlook Kontaktordner zwischengespeichert, der für dieses soziale Netzwerk im Standardspeicher Outlook Benutzers spezifisch ist. Der Name des Kontaktordners basiert auf dem Namen des sozialen Netzwerks, den der OSC mithilfe der [ISocialProvider::SocialNetworkName-Eigenschaft abruft.](isocialprovider-socialnetworkname.md) 
  
Bei der zwischengespeicherten Synchronisierung speichert osc Informationen nur für die Freunde des angemeldeten Benutzers im sozialen Netzwerk. Der OSC greift nicht auf Informationen für Nicht-Freunde zu.
  
Das Standardintervall für osc zum Aktualisieren des Kontaktordners für Informationen von Freunden aus dem sozialen Netzwerk ist einmal pro Tag (oder einmal pro 1440 Minuten). Dieses Aktualisierungsintervall kann auch nach Gruppenrichtlinie festgelegt werden, wie zu Beginn dieses Themas erläutert.
  
Wenn während einer Aktualisierung ein Fehler auftritt, versucht osc erneut, in einem Intervall zu suchen, das vom **contactSyncRestartInterval-Element** in der **Funktions-XML** angegeben wird. Dieses Wiederholungsintervall hat einen Standardwert von 30 Minuten und kann auch durch gruppenrichtlinien festgelegt werden. 
  
Wenn ein Benutzer eine Visitenkarte öffnet und die Registerkarte **"Neuigkeiten"** auswählt, wird die **Registerkarte "Neuigkeiten"** aktualisiert. Ebenso wird der Personenbereich aktualisiert, wenn ein Outlook Benutzer ein Element in Outlook erneut auswählt oder eine Person im Personenbereich erneut auswählt. Wenn das Cacheaktualisierungsintervall nicht abgelaufen ist, wechselt der OSC zum Cache, um Informationen für den ausgewählten Benutzer abzurufen. Dadurch wird der Aufwand für die Verwendung der OSC-Anbietererweiterung für den Zugriff auf das soziale Netzwerk vermieden. Wenn das Aktualisierungsintervall abgelaufen ist, ruft der OSC die [ISocialPerson::GetFriendsAndColleagues-Methode](isocialperson-getfriendsandcolleagues.md) auf, um die aktuellen Freundesinformationen für den angemeldeten Benutzer abzurufen, und aktualisiert den Cache im Kontaktordner. 
  
Der OSC-Anbieter informiert den OSC, dass er die zwischengespeicherte Synchronisierung von Freunden unterstützt, indem er die folgenden Elemente in der **FUNKTIONS-XML** angibt: 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **false**
    
## <a name="on-demand-synchronization"></a>On-Demand-Synchronisierung

Wenn ein Benutzer die Registerkarte **"Neuigkeiten"** in einer Visitenkarte auswählt oder ein anderes Outlook Element oder eine andere Person im Personenbereich in Outlook auswählt, aktualisiert osc die Visitenkarte bzw. den Personenbereich. Wenn ein OSC-Anbieter die On-Demand-Synchronisierung von Personen oder Aktivitäten unterstützt, wird der OSC mit einem Cache im Speicher synchronisiert und aktualisiert Details wie Name, Titel, Bild und Aktivitätsstreams auf der Visitenkarte oder im Personenbereich. Bei der Synchronisierung bei Bedarf versucht der OSC im Gegensatz zur zwischengespeicherten Synchronisierung, die Informationen für die Person zu aktualisieren, unabhängig davon, ob es sich bei dieser Person um einen Freund oder einen Nichtfreund des angemeldeten Benutzers im sozialen Netzwerk handelt. 
  
On-Demand-Personendaten (oder Aktivitätsdaten) werden nur im Arbeitsspeicher gespeichert. Die speicherinternen Daten werden gelöscht, wenn die Office Clientanwendung heruntergefahren wird oder der Benutzer eine Aktualisierung der Visitenkarte oder des Personenbereichs verursacht und die Daten länger als das Aktualisierungsintervall im Speicher verblieben sind. Beachten Sie, dass die Aktualisierung aus dem sozialen Netzwerk immer von einem Benutzer initiiert wird, der die Visitenkarte oder den Personenbereich aktualisiert (z. B. indem er einen anderen Benutzer im Personenbereich auswählt oder ein anderes Element in Outlook Explorer-Fenster auswählt). 

Das Gegenteil ist jedoch nicht immer der Fall– nicht bei jeder Aktualisierung der Visitenkarte oder des Personenbereichs wird notwendigerweise eine Aktualisierung aus dem sozialen Netzwerk ausgeführt. Wenn der Benutzer die Visitenkarte oder den Personenbereich aktualisiert und die Daten der Person (oder Aktivität) länger als das Aktualisierungsintervall im Speicher verblieben sind, ruft der OSC [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (oder [ISocialSession2::GetActivitiesEx)](isocialsession2-getactivitiesex.md)auf, um die Informationen im Speicher aus dem sozialen Netzwerk zu aktualisieren. Der zulässige Zeitraum für Informationen zu Freunden und Nicht-Freunden im Speicher beträgt 24 Stunden und für Aktivitäten 30 Minuten. 
  
Ein wichtiger Unterschied zwischen zwischengespeicherter und bedarfsgesteuerter Synchronisierung besteht darin, dass die Synchronisierung bei Bedarf Personen- und Aktivitätsinformationen für Freunde und Nicht-Freunde im Netzwerk abrufen kann. Wenn die ausgewählte Person kein Freund ist, aktualisiert der OSC Informationen und Aktivitäten für diese Person, wenn eine der folgenden Anforderungen erfüllt ist: 
  
- Die Person ist ein Benutzer im sozialen Netzwerk und ermöglicht die öffentliche Anzeige von Profil- und Aktivitätsinformationen.
    
- Die Person befindet sich im selben Netzwerk wie der angemeldete Benutzer in diesem sozialen Netzwerk (z. B. im selben Netzwerk für die Uni).
    
Die On-Demand-Synchronisierung von Personen und Aktivitäten führt zu weiteren Aufrufen des Anbieters aus dem OSC-Kernmodul. Soziale Netzwerke müssen in der Lage sein, die erhöhten Bandbreitenanforderungen der On-Demand-Synchronisierung zu verarbeiten.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Angeben von XML-Elementen für die Bedarfssynchronisierung

Der OSC-Anbieter informiert den OSC, dass er die On-Demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt, indem er die folgenden Elemente in der **FUNKTIONS-XML** angibt: 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **false**
    
- **dynamicContactsLookup**  =  **true**
    
Der OSC-Anbieter informiert den OSC, dass er die On-Demand-Synchronisierung von Aktivitäten unterstützt, indem er die folgenden Elemente in der **FUNKTIONS-XML** angibt: 
  
- **getActivities**  =  **true**
    
- **cacheActivities**  =  **false**
    
- **dynamicActivitiesLookupEx**  =  **true**
    
## <a name="hybrid-synchronization"></a>Hybridsynchronisierung

Ein OSC-Anbieter kann die Hybridsynchronisierung von Freunden und Nicht-Freunden unterstützen. Dies kann die Anrufe zwischen dem OSC-Kernmodul und dem OSC-Anbieter, die Aufrufe an das soziale Netzwerk für die On-Demand-Synchronisierung von Freunden und die Währung der Freundesdaten optimieren. Die mindeste Zeit, in der die Daten in einem Ordner oder Speicher verbleiben können, entspricht gegebenenfalls den Grenzwerten in zwischengespeicherten oder bedarfsgesteuerten Synchronisierungsmodi.
  
> [!NOTE]
> Ab Outlook Connector für soziale Netzwerke 2013 unterstützt OSC nur die Synchronisierung von Aktivitäten bei Bedarf und keine hybride Synchronisierung von Aktivitäten mehr. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Hybridsynchronisierung von Freunden und Nicht-Freunden

Wenn ein OSC-Anbieter die hybride Synchronisierung von Freunden und Nicht-Freunden unterstützt, führt osc Folgendes aus: 
  
- Der OSC speichert Informationen für Freunde des angemeldeten Benutzers im kontaktspezifischen Kontaktordner für soziale Netzwerke.
    
- Der OSC speichert Informationen für Nicht-Freunde des angemeldeten Benutzers im Arbeitsspeicher.
    
Der OSC-Anbieter informiert den OSC, dass er die hybride Synchronisierung von Freunden und Nicht-Freunden unterstützt, indem er die folgenden Elemente in **der** FUNKTIONS-XML angibt: 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **true**
    
## <a name="synchronization-intervals"></a>Synchronisierungsintervalle

In der folgenden Tabelle werden die Synchronisierungsintervalle für Freunde und Nicht-Freunde-Informationen zwischen dem entsprechenden Cache (Ordner oder Speicher) und dem sozialen Netzwerk zusammengefasst, je nach unterstütztem Synchronisierungsmodus. Informationen zum Hybridsynchronisierungsmodus finden Sie in den Zeilen für den zwischengespeicherten Modus für Freunde und in der Zeile für den On-Demand-Modus für Nicht-Freunde.
  
|**Synchronisierungsmodus für Personen**|**Festlegen des Aktualisierungsintervalls**|**Standard-Mindestzeit vor der Aktualisierung**|**Außerkraftsetzung von Gruppenrichtlinien**|
|:-----|:-----|:-----|:-----|
|Cached  <br/> |Festlegen innerhalb von OSC  <br/> |1440 Minuten (24 Stunden)  <br/> |Windows Registrierungswert **NetContactSyncInterval** <br/> |
|Cached  <br/> |**contactSyncRestartInterval-Element** in **Funktions-XML**  <br/> |30 Minuten, wenn **contactSyncRestartInterval** nicht festgelegt ist  <br/> |Windows Registrierungswert **contactSyncRestartInterval** <br/> |
|Bei Bedarf  <br/> |Festlegen innerhalb von OSC  <br/> |1440 Minuten (24 Stunden)  <br/> |Windows Registrierungswert **OnlineSearchExpiryTime** <br/> |
   
In der folgenden Tabelle werden die Synchronisierungsintervalle für Aktivitäten von Freunden und Nicht-Freunden zwischen dem entsprechenden Cache (Ordner oder Speicher) und dem sozialen Netzwerk zusammengefasst, je nach unterstützten Synchronisierungsmodi. 
  
|**Synchronisierungsmodus für Aktivitäten**|**Festlegen des Aktualisierungsintervalls**|**Standard-Mindestzeit vor der Aktualisierung**|**Außerkraftsetzung von Gruppenrichtlinien**|
|:-----|:-----|:-----|:-----|
|Bei Bedarf  <br/> |Festlegen innerhalb von OSC  <br/> |30 Minuten  <br/> |Windows Registrierungswert **OnlineSearchExpiryTime** <br/> |
   
Die folgenden Informationen gelten für die in den beiden Tabellen aufgeführten Windows Registrierungswerte:
  
- Schlüssel:  `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Wert: DWORD-Wert zwischen 1 und 10080
    
## <a name="see-also"></a>Siehe auch

- [Xml-Beispiel für Funktionen](capabilities-xml-example.md)  
- [XML für Funktionen](xml-for-capabilities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Verwalten des Outlook Connector für soziale Netzwerke mithilfe von Gruppenrichtlinien](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

