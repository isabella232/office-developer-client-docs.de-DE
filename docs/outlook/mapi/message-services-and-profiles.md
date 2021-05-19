---
title: Nachrichtendienste und Profile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 78a13bacf13b019bbf9436830ad66db7fdfaf425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415467"
---
# <a name="message-services-and-profiles"></a>Nachrichtendienste und Profile
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Benutzer benötigen die Dienste mehrerer Messagingsysteme mit jeweils einem oder mehreren Dienstanbietern. Da es umständlich ist, jeden dieser Dienstanbieter einzeln zu installieren und zu konfigurieren, und da ein Messagingserver in der Regel eine Gruppe verwandter Anbieter benötigt, um alle funktionen verfügbar zu machen, umfasst MAPI das Konzept eines Nachrichtendiensts. Nachrichtendienste helfen Benutzern beim Installieren und Konfigurieren ihrer Dienstanbieter.
  
Um einen Nachrichtendienst zu erstellen, schreibt ein Entwickler ein Nachrichtendienst-Einstiegspunktprogramm, um die Konfiguration der einzelnen Anbieter im Dienst zu behandeln, und ein Setupprogramm, um folgendes zu tun:
  
- Installieren Sie jeden Anbieter im Dienst.
    
- Erstellen sie Registrierungs- und Initialisierungsdateieinträge.
    
- Erstellen Sie Einträge in der MAPI-Konfigurationsdatei Mapisvc.inf.
    
Die Datei Mapisvc.inf enthält Informationen zur Konfiguration aller auf dem Computer installierten Nachrichtendienste und Dienstanbieter. Sie ist in hierarchischen Abschnitten organisiert, und jede Ebene ist mit der nächsten verknüpft. Oben finden Sie drei Abschnitte, die Folgendes enthalten: 
  
- Eine Liste der Hilfedateien für den Nachrichtendienst.
    
- Eine Liste der wichtigsten Oder Standardnachrichtendienste.
    
- Eine Liste aller Dienste auf dem Computer.
    
Die nächste Ebene enthält Abschnitte für jeden Nachrichtendienst, und die letzte Ebene enthält Abschnitte für jeden Dienstanbieter in einem Dienst. MAPI erfordert, dass Entwickler von Dienstanbietern und Nachrichtendiensten bestimmte Einträge zu Mapisvc.inf hinzufügen. Entwickler können andere Einträge nach eigenem Ermessen hinzufügen. Die meisten Informationen in Mapisvc.inf landen in einem oder mehreren Profilen, einer Sammlung von Konfigurationsinformationen für den bevorzugten Satz von Nachrichtendiensten eines Benutzers. Da ein Computer mehrere Benutzer haben kann und ein einzelner Benutzer mehrere Einstellungssätze haben kann, können viele Profile auf einem Computer vorhanden sein. Jedes Profil beschreibt einen anderen Satz von Nachrichtendiensten. Mit mehreren Profilen kann ein Benutzer z. B. zu Hause mit einem Satz von Nachrichtendiensten und im Büro mit einem anderen Satz arbeiten.
  
Profile werden bei der Installation oder Anmeldung des Nachrichtendiensts von einer Clientanwendung erstellt, die Konfigurationsunterstützung bietet. MAPI stellt zwei solche Clientanwendungen zur Verfügung: ein Systemsteuerungselement und den Profil-Assistenten. Das Systemsteuerungselement ist eine Volldienstkonfigurationsanwendung, mit der Benutzer Profile erstellen, löschen, bearbeiten und kopieren sowie Änderungen an den Einträgen in einem Profil vorgenommen können. Der Profil-Assistent ist eine einfache Anwendung, die das Hinzufügen eines Nachrichtendiensts zu einem Profil so einfach wie möglich macht. Der Profil-Assistent besteht aus einer Reihe von Dialogfelder, sogenannten Eigenschaftenseiten, in der der Benutzer aufgefordert wird, einen Dienst zu installieren und zu konfigurieren. Der Benutzer wird nur zur Eingabe von Werten für die kritischsten Einstellungen aufgefordert. Alle anderen Einstellungen erben Standardwerte. Nachdem das Profil erstellt wurde, können Benutzer keine Änderungen vornehmen. 
  
Während das Systemsteuerungselement immer über die Systemsteuerung aufgerufen wird, gibt es eine Vielzahl von Szenarien, die dazu führen können, dass der Profil-Assistent aufgerufen wird. Clientanwendungen können den Profil-Assistenten aufrufen, um ein Standardprofil zum Zeitpunkt der Anmeldung zu erstellen, wenn noch kein Profil erstellt wurde. Anstatt Code erneut zuimplementieren, um ein Profil hinzuzufügen, kann sich das Systemsteuerungselement oder eine andere Clientanwendung auf die bereits im Profil-Assistenten vorhandenen Funktionen verlassen. Ein Nachrichtendienst kann in seiner Einstiegspunktfunktion den Profil-Assistenten aufrufen, wenn der Dienst dem Standardprofil hinzugefügt werden muss. Nachrichtendienste, die den Profil-Assistenten verwenden, müssen eine zusätzliche Einstiegspunktfunktion und eine standard-Windows schreiben. Der Profil-Assistent ruft die Einstiegspunktfunktion auf, um das Konfigurationsdialogfeld des Diensts abzurufen, während die Dialogfeldprozedur die Nachrichten verarbeitet, die generiert werden, wenn dieses Dialogfeld verwendet wird. 
  
Profile sind ähnlich wie die Datei Mapisvc.inf organisiert. Profile haben verknüpfte hierarchische Abschnitte; Dienstanbieter besitzen Abschnitte auf der niedrigsten Ebene, Nachrichtendienste eigene Abschnitte auf der mittleren Ebene, und MAPI besitzt Abschnitte auf der höchsten Ebene. Jeder Abschnitt wird mit einem eindeutigen Bezeichner identifiziert, der als [MAPIUID bezeichnet wird.](mapiuid.md) Die MAPI-Abschnitte enthalten interne Informationen für MAPI, z. B. die Bezeichner aller Abschnitte des Nachrichtendienstprofils und Links zu jedem der anderen Abschnitte. In jedem Abschnitt des Nachrichtendiensts werden Links zu den jeweiligen Anbieterabschnitten und in jedem Anbieterabschnitt ein Link zu seinem Dienstabschnitt speichert. 
  
Die folgende Abbildung zeigt den Inhalt von zwei typischen Profilen. Sam verfügt über zwei Profile auf seinem Computer, eines für die Heimnutzung und eines für die Verwendung im Büro. Das Startprofil enthält drei Nachrichtendienste. Message Service X ist ein einzelner Anbieterdienst für die Adressbuchverwaltung. Nachrichtendienste Y und Z verfügen über drei Anbieter – einen Adressbuchanbieter, einen Nachrichtenspeicheranbieter und einen Transportanbieter. Sams Arbeitsprofil enthält zwei verschiedene Nachrichtendienste, von denen jeder über einen Adressbuchanbieter, einen Nachrichtenspeicheranbieter und einen Transportanbieter verfügt. 
  
**Profilbeispiel**
  
![Profilbeispiel](media/amapi_56.gif "Profilbeispiel")
  
Die folgende Abbildung zeigt ein Profil, das zwei Nachrichtendienste enthält. Der Code zum Installieren und Konfigurieren der Dienstanbieter, die zum Nachrichtendienst gehören, befindet sich in derselben DLL wie der Code für die Anbieter. Dieser Code liest Informationen aus dem Profil zur Anmeldezeit, um die Dienstanbieter zu konfigurieren, und fordert den Benutzer auf, wenn möglich und erforderlich, fehlende Informationen zu erhalten. Anforderungen eines Clients zum Anzeigen oder Ändern von Konfigurationseinstellungen für einen der Anbieter werden ebenfalls durch diesen allgemeinen Code behandelt.
  
**Installieren und Konfigurieren von Serviceanbietern**
  
![Installieren und Konfigurieren von Dienstanbietern](media/amapi_55.gif "Installieren und Konfigurieren von Dienstanbietern")
  
## <a name="see-also"></a>Siehe auch

- [MAPIUID](mapiuid.md)
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)

