---
title: Synchronisieren von Freunden und Aktivitäten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Outlook Social Connector (OSC) unterstützt die Anzeige von Informationen aus einem sozialen Netzwerk zu einer Person auf der Visitenkarte oder im Bereich Personen Outlook. SharePoint Server, SharePoint-Arbeitsbereich Lync-Clients und alle Office-Clientanwendungen, die Anwesenheitsinformationen unterstützen-Unterstützung der Visitenkarte.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399158"
---
# <a name="synchronizing-friends-and-activities"></a>Synchronisieren von Freunden und Aktivitäten

Outlook Social Connector (OSC) unterstützt die Anzeige von Informationen aus einem sozialen Netzwerk zu einer Person auf der Visitenkarte oder im Bereich Personen Outlook. SharePoint Server, SharePoint-Arbeitsbereich Lync-Clients und alle Office-Clientanwendungen, die Anwesenheitsinformationen unterstützen-Unterstützung der Visitenkarte.
  
Sie können der Visitenkarte in Szenarien der Zusammenarbeit in Office-Anwendungen, um weitere Informationen zu den Personen zu erhalten, die Sie mit zusammenarbeiten. Beispiele für diese Szenarien sind messaging in Microsoft Outlook und ein Dokument in Word die gemeinsame dokumenterstellung. Wenn Sie auf die Registerkarte **neu** eine Visitenkarte, die zeigt Informationen über die Person klicken. 
  
Bereich Personen Outlook zeigt Informationen über eine Person, die ein Absender oder Empfänger eines Outlook-Elements gewählte werden kann. Wenn Sie wählen Sie im Bereich Personen oder einem anderen Element im Outlook-Explorer eine andere Person oder ein Outlook-Element in einem Inspektor geöffnet, aktualisiert Outlook Social Connector (OSC) Bereich Personen. 
  
Die Visitenkarte oder ein Bereich Personen aktuelle Informationen für die ausgewählte Person anzuzeigen synchronisiert die OSC solche Informationen über den OSC-Anbieter und eine andere Form des Zwischenspeicherns. Diese Synchronisierung hängt die OSC-Anbieter, die auf dem Clientcomputer installiert sind, die für Kommunikation über soziale Netzwerke, dass Sie sich angemeldet haben, über die OSC-Anbieter und der Synchronisierungsmodus, dass aller die OSC-Anbieter für diese sozialen Netzwerken unterstützt.
  
Die OSC unterstützt Synchronisieren von Freunden, nicht Freunde und Aktivitäten für Freunde und nicht Freunde auf unterschiedliche Weise: Synchronisierung, bedarfsgesteuerten Synchronisierung und hybride Synchronisierung zwischengespeichert. Der Hauptunterschied zwischen diesen Modi der Synchronisierung ist, wo das osc bilden die Daten gespeichert werden, ob sie in einem Ordner in Outlook-Standardspeicher des Benutzers oder im Arbeitsspeicher auf dem Computer des Benutzers ist. In jedem Fall wie in diesem Thema erwähnt besteht eine Standard-Zeit, die die Daten in den Arbeitsspeicher bleiben, bevor die Daten aktualisiert werden. In einigen Fällen kann die minimale Zeitspanne mithilfe von Gruppenrichtlinien angepasst werden. Weitere Informationen zu Gruppenrichtlinien, die das Verhalten der die OSC steuern, finden Sie unter [Gewusst wie: Verwalten der Outlook Connector für soziale Netzwerke mithilfe von Gruppenrichtlinien](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Beachten Sie, dass ist die ausgewählte Person nicht Mitglied für soziale Netzwerke, die OSC keine Person oder neue Aktivität Informationen für diese Person in der Visitenkarte oder Bereich Personen angezeigt wird.
  
## <a name="cached-synchronization"></a>Cache-Synchronisierung

Ein OSC-Anbieter kann Informationen für Freunde im sozialen Netzwerk in einen bestimmten Ordner auf Outlook-Standardspeicher des Benutzers gespeichert, und diesem Cache in regelmäßigen Abständen zu aktualisieren, nachdem eine angegebene Zeitspanne abgelaufen ist. Zwischenspeichern von Informationen in einem Ordner hat den Vorteil der Reduzierung des Datenverkehrs in sozialen Netzwerken.
  
> [!NOTE]
> Ab Outlook Social Connector 2013 unterstützt die OSC nicht mehr Cache Synchronisierung von Aktivitäten. 
  
### <a name="cached-synchronization-of-friends"></a>Zwischengespeicherte Synchronisierung von Freunden

Wenn ein OSC-Anbieter für Freunde zwischengespeicherten Synchronisierung unterstützt, wird die OSC Informationen für Freunde des angemeldeten Benutzers im sozialen Netzwerk zwischengespeichert. Die Informationen in einem Outlook-Kontakteordner zwischengespeichert, die speziell für das soziale Netzwerk in Outlook-Standardspeicher des Benutzers ist. Der Name des Ordners Kontakte basiert auf den Namen des sozialen Netzwerks, der die OSC mithilfe der [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) -Eigenschaft abgerufen. 
  
Im Cache Synchronisierung speichert die OSC Informationen für nur des angemeldeten Benutzers Freunde im sozialen Netzwerk. Die OSC greifen nicht auf Informationen für nicht-Freunde.
  
Das standardmäßige Intervall für das osc bilden den Kontakteordner Freunde Informationen aus dem sozialen Netzwerk aktualisiert wird einmal pro Tag (oder einmal pro 1440 Minuten). Dieses Aktualisierungsintervall kann auch durch eine Gruppenrichtlinie, festgelegt werden, wie am Anfang dieses Themas erläutert.
  
Wenn während einer Aktualisierung ein Fehler auftritt, versucht der OSC Intervallen, die durch das **ContactSyncRestartInterval** -Element in die **Funktionen** XML angegeben ist. Diese Wiederholungsintervall hat einen Standardwert von 30 Minuten, und kann auch mithilfe von Gruppenrichtlinien festgelegt werden. 
  
Wenn ein Benutzer eine Visitenkarte öffnet und die Registerkarte **neu wählt** , wird die Registerkarte **neu** aktualisiert. Wenn ein Outlook-Benutzer ein Element in Outlook reselects oder reselects eine Person im Bereich Personen, wird entsprechend den Personenbereich aktualisiert. Wenn das Cacheaktualisierungsintervall nicht abgelaufen ist, geht die OSC im Cache, um alle Informationen für den ausgewählten Benutzer abzurufen. Vermeiden des Verarbeitungsaufwands OSC-anbietererweiterung Zugriff auf das soziale Netzwerk verwenden. Wenn das Aktualisierungsintervall abgelaufen ist, das osc bilden die [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode zum Abrufen von Informationen für den angemeldeten Benutzer aktuelle Freunde und aktualisiert den Cache in den Kontakteordner. 
  
Der OSC-Anbieter die OSC informiert werden, dass es sich um zwischengespeicherte Synchronisierung von Freunden unterstützt, indem Sie die folgenden Elemente in die **Funktionen** XML angeben: 
  
- **GetFriends** = **true**
    
- **CacheFriends** = **true**
    
- **DynamicContactsLookup** = **"false"**
    
## <a name="on-demand-synchronization"></a>Bedarfsgesteuerte Synchronisierung

Wenn ein Benutzer die Registerkarte **What's new** in einer Visitenkarte wählt oder eines anderen Outlook-Elements oder einer anderen Person im Bereich Personen in Outlook markiert, wird das osc bilden die Visitenkarte oder Personenbereich aktualisiert. Wenn ein OSC-Anbieter bedarfsgesteuerten Synchronisierung von Personen oder Aktivitäten unterstützt, die OSC synchronisiert mit einem Cache im Arbeitsspeicher und Details wie etwa Name, Titel, Bild und Datenströme Aktivität, auf der Visitenkarte oder Personenbereich aktualisiert. Die OSC versucht, für bedarfsgesteuerten Synchronisierung im Gegensatz zu zwischengespeicherten Synchronisierung aktualisiert die Informationen für die Person, unabhängig davon, ob diese Person einen Freund oder Friend des angemeldeten Benutzers im sozialen Netzwerk ist. 
  
Bei Bedarf Person (oder neue Aktivität) Daten werden nur im Speicher gespeichert. Die Daten im Speicher werden gelöscht, wenn die Office-Clientanwendung heruntergefahren, oder der Benutzer eine Aktualisierung der Visitenkarte oder Personenbereich löst und die Daten wurde im Arbeitsspeicher länger als Aktualisierungsintervalls nicht wesentlich. Beachten Sie, dass die Aktualisierung aus dem sozialen Netzwerk immer von einem Benutzer aktualisieren die Visitenkarte oder Personenbereich, (beispielsweise durch einen anderen Benutzer im Bereich Personen, oder wählen Sie ein anderes Element in Outlook Explorer-Fenster) initiiert wird. 

Der Reverseproxy ist jedoch nicht immer true – nicht bei jedem Aktualisieren der Visitenkarte oder Personenbereich unbedingt eine Aktualisierung aus dem sozialen Netzwerk entstehen. Wenn der Benutzer die Visitenkarte aktualisiert oder Personenbereich, und die Person (oder neue Aktivität) Daten im Arbeitsspeicher länger als Aktualisierungsintervalls blieb hat, ruft der OSC [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (oder [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)) Aktualisieren Sie die Informationen im Speicher aus dem sozialen Netzwerk. Die zulässige Periode Friend und nicht-Friend Informationen im Speicher ist 24 Stunden, und für Aktivitäten, 30 Minuten. 
  
Ein wichtiger Unterschied zwischen zwischengespeicherten und bedarfsgesteuerten Synchronisierung ist, dass bedarfsgesteuerten Synchronisierung Person und Aktivitätsinformationen für Freunde und nicht Freunde im Netzwerk abgerufen werden kann. Ist die ausgewählte Person einen nicht-Freund, aktualisiert das osc bilden Informationen und Aktivitäten für diese Person, wenn eine der folgenden Anforderungen erfüllt ist: 
  
- Die Person ist ein Benutzer für das soziale Netzwerk und ermöglicht das öffentliche Profil-und anzeigen.
    
- Die Person befindet sich in demselben Netzwerk wie der angemeldete Benutzer auf das sozialen Netzwerk (beispielsweise im gleichen Netzwerk für Eltern University).
    
Bedarfsgesteuerten Synchronisierung von Personen und Aktivitäten führt weitere Aufrufe an den Anbieter aus dem OSC-Kern-Modul. Soziale Netzwerken müssen die Anforderungen erhöhte Bandbreite der bedarfsgesteuerten Synchronisierung behandeln können.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Angeben von XML-Elemente für die Synchronisierung auf Abruf

Der OSC-Anbieter die OSC informiert werden, dass es bedarfsgesteuerten Synchronisierung Freunde und nicht Freunde unterstützt, indem Sie die folgenden Elemente in die **Funktionen** XML angeben: 
  
- **GetFriends** = **true**
    
- **CacheFriends** = **"false"**
    
- **DynamicContactsLookup** = **true**
    
Der OSC-Anbieter informiert den OSC bedarfsgesteuerten Synchronisierung von Aktivitäten unterstützt wird, indem Sie die folgenden Elemente in die **Funktionen** XML angeben: 
  
- **GetActivities** = **true**
    
- **CacheActivities** = **"false"**
    
- **DynamicActivitiesLookupEx** = **true**
    
## <a name="hybrid-synchronization"></a>Hybrid-Synchronisierung

Ein OSC-Anbieter kann Hybrid Synchronisierung von Freunde und nicht Freunde unterstützen. Dadurch kann die Anrufe zwischen OSC zentralen Modul und der OSC-Anbieter, der Anrufe für das soziale Netzwerk für die bedarfsgesteuerten Synchronisierung von Freunden und die Währung der Freunde Datengruppe optimieren. Die minimale Zeit, die die Daten in einem Ordner oder Arbeitsspeicher, verbleiben können, sofern zutreffend, ist die gleiche wie die Beschränkungen in zwischengespeicherten oder bedarfsgesteuerten Synchronisierungsmodi.
  
> [!NOTE]
> Ab Outlook Social Connector 2013, die OSC unterstützt nur bedarfsgesteuerten Synchronisierung von Aktivitäten und Hybrid-Synchronisierung von Aktivitäten nicht mehr unterstützt. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Hybrid-Synchronisierung von Freunde und nicht-Freunde

Wenn ein OSC-Anbieter Hybrid Synchronisierung von Freunde und Freunde-nicht unterstützt, führt der OSC Folgendes aus: 
  
- Die OSC speichert Informationen für Freunde des angemeldeten Benutzers in der sozialen Netzwerk-spezifische Kontaktordner.
    
- Die OSC werden Informationen für nicht-Freunde des angemeldeten Benutzers im Arbeitsspeicher gespeichert.
    
Der OSC-Anbieter die OSC informiert werden, dass es Hybrid Synchronisierung Freunde und nicht Freunde unterstützt, indem Sie die folgenden Elemente in die **Funktionen** XML angeben: 
  
- **GetFriends** = **true**
    
- **CacheFriends** = **true**
    
- **DynamicContactsLookup** = **true**
    
## <a name="synchronization-intervals"></a>Synchronisierung Intervallen

In der folgenden Tabelle werden die Intervalle Synchronisierung nicht Freunde-Informationen zwischen dem entsprechenden Cache (Ordner oder Speicher) und dem sozialen Netzwerk, je nach den unterstützten Synchronisierungsmodus und Freunde zusammengefasst. Hybride Synchronisierungsmodus finden Sie die Zeilen für die Cache-Modus für Freunde und die Zeile für bedarfsgesteuerten Modus für nicht-Freunde.
  
|**Synchronisierungsmodus für Personen**|**Wobei Aktualisierungsintervall festgelegt ist**|**Minimale Standardzeit vor der Aktualisierung**|**Gruppenrichtlinie außer Kraft setzen**|
|:-----|:-----|:-----|:-----|
|Cached  <br/> |Legen Sie innerhalb der OSC  <br/> |1440 Minuten (24 Stunden)  <br/> |Windows-Registrierungswert **NetContactSyncInterval** <br/> |
|Cached  <br/> |**ContactSyncRestartInterval** -Element im XML- **Funktionen**  <br/> |30 Minuten, wenn **ContactSyncRestartInterval** nicht festgelegt ist  <br/> |Windows-Registrierung Wert **contactSyncRestartInterval** <br/> |
|Bei Bedarf  <br/> |Legen Sie innerhalb der OSC  <br/> |1440 Minuten (24 Stunden)  <br/> |Windows-Registrierungswert **OnlineSearchExpiryTime** <br/> |
   
In der folgenden Tabelle werden die Synchronisierung von Intervallen für Aktivitäten Freunde und Freunde zwischen dem entsprechenden Cache (Ordner oder Speicher) und dem sozialen Netzwerk, je nach den unterstützten Synchronisierung Modi zusammengefasst. 
  
|**Synchronisierungsmodus für Aktivitäten**|**Wobei Aktualisierungsintervall festgelegt ist**|**Minimale Standardzeit vor der Aktualisierung**|**Gruppenrichtlinie außer Kraft setzen**|
|:-----|:-----|:-----|:-----|
|Bei Bedarf  <br/> |Legen Sie innerhalb der OSC  <br/> |30 Minuten  <br/> |Windows-Registrierungswert **OnlineSearchExpiryTime** <br/> |
   
Die folgenden Informationen gelten für die Windows-Registrierungswerte, die in den beiden Tabellen aufgelistet:
  
- Wichtige Punkte:`HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Wert: DWORD-Wert zwischen 1 und 10080
    
## <a name="see-also"></a>Siehe auch

- [Funktionen XML-Beispiel](capabilities-xml-example.md)  
- [XML-Code für Funktionen](xml-for-capabilities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Gewusst wie: Verwalten von Outlook Social Connector mithilfe von Gruppenrichtlinien](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

