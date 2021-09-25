---
title: Nachrichtendienste und Profile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f8f081ea35241f3e57a8cf2345254d24c5032fdc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592053"
---
# <a name="message-services-and-profiles"></a>Nachrichtendienste und Profile
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Benutzer benötigen die Dienste mehrerer Messagingsysteme, die jeweils über einen oder mehrere Dienstanbieter verfügen. Da es umständlich ist, jeden dieser Dienstanbieter einzeln zu installieren und zu konfigurieren, und da ein Messagingserver in der Regel eine Gruppe verwandter Anbieter erfordert, um alle seine Funktionen verfügbar zu machen, umfasst die MAPI das Konzept eines Nachrichtendiensts. Nachrichtendienste helfen Benutzern beim Installieren und Konfigurieren ihrer Dienstanbieter.
  
Um einen Nachrichtendienst zu erstellen, schreibt ein Entwickler ein Einstiegspunktprogramm für den Nachrichtendienst, um die Konfiguration der einzelnen Anbieter im Dienst zu verarbeiten, und ein Setupprogramm, um Folgendes zu tun:
  
- Installieren Sie jeden Anbieter im Dienst.
    
- Erstellen Sie Registrierungs- und Initialisierungsdateieinträge.
    
- Erstellen Sie Einträge in der MAPI-Konfigurationsdatei Mapisvc.inf.
    
Die Datei Mapisvc.inf enthält Informationen, die sich auf die Konfiguration aller auf dem Computer installierten Nachrichtendienste und Dienstanbieter beziehen. Sie ist in hierarchischen Abschnitten organisiert, wobei jede Ebene mit der nächsten ebene verknüpft ist. Oben sind drei Abschnitte aufgeführt, die Folgendes enthalten: 
  
- Eine Liste der Nachrichtendienst-Hilfedateien.
    
- Eine Liste der wichtigsten oder standardmäßigsten Nachrichtendienste.
    
- Eine Liste aller Dienste auf dem Computer.
    
Die nächste Ebene enthält Abschnitte für jeden Nachrichtendienst, und die letzte Ebene enthält Abschnitte für jeden Dienstanbieter in einem Dienst. MapI erfordert, dass Entwickler von Dienstanbietern und Nachrichtendiensten bestimmte Einträge zu Mapisvc.inf hinzufügen; Entwickler können nach eigenem Ermessen andere Einträge hinzufügen. Die meisten Informationen in Mapisvc.inf enden in einem oder mehreren Profilen, einer Sammlung von Konfigurationsinformationen für den bevorzugten Satz von Nachrichtendiensten eines Benutzers. Da ein Computer mehrere Benutzer und ein einzelner Benutzer mehrere Einstellungen haben kann, können auf einem Computer viele Profile vorhanden sein. Jedes Profil beschreibt einen anderen Satz von Nachrichtendiensten. Mit mehreren Profilen kann ein Benutzer arbeiten, z. B. zu Hause mit einer Gruppe von Nachrichtendiensten und im Büro mit einem anderen Satz.
  
Profile werden bei der Installation oder Anmeldung des Nachrichtendiensts von einer Clientanwendung erstellt, die Konfigurationsunterstützung bereitstellt. MAPI stellt zwei solche Clientanwendungen bereit: ein Systemsteuerungselement und den Profil-Assistenten. Das Systemsteuerungselement ist eine Full-Service-Konfigurationsanwendung, mit der Benutzer Profile erstellen, löschen, bearbeiten und kopieren sowie Änderungen an den Einträgen in einem Profil vornehmen können. Der Profil-Assistent ist eine einfache Anwendung, die das Hinzufügen eines Nachrichtendiensts zu einem Profil so einfach wie möglich macht. Der Profil-Assistent besteht aus einer Reihe von Dialogfeldern, die als Eigenschaftenseiten bezeichnet werden und den Benutzer durch den Prozess der Installation und Konfiguration eines Diensts auffordern. Der Benutzer wird nur zur Eingabe von Werten für die wichtigsten Einstellungen aufgefordert. Alle anderen Einstellungen erben Standardwerte. Nachdem das Profil erstellt wurde, dürfen Benutzer keine Änderungen vornehmen. 
  
Während das Systemsteuerungselement immer über die Systemsteuerung aufgerufen wird, gibt es eine Vielzahl von Szenarien, die dazu führen können, dass der Profil-Assistent aufgerufen wird. Clientanwendungen können den Profil-Assistenten aufrufen, um ein Standardprofil zum Zeitpunkt der Anmeldung zu erstellen, wenn noch kein Profil erstellt wurde. Anstatt Code zum Hinzufügen eines Profils erneut zu verwenden, kann sich das Systemsteuerungselement oder eine andere Clientanwendung auf die Funktionalität verlassen, die bereits im Profil-Assistenten vorhanden ist. Ein Nachrichtendienst kann in seiner Einstiegspunktfunktion den Profil-Assistenten aufrufen, wenn der Dienst dem Standardprofil hinzugefügt werden muss. Nachrichtendienste, die den Profil-Assistenten verwenden, müssen eine zusätzliche Einstiegspunktfunktion und eine standard Windows Dialogfeldprozedur schreiben. Der Profil-Assistent ruft die Einstiegspunktfunktion auf, um das Konfigurationsdialogfeld des Diensts abzurufen, während die Dialogfeldprozedur die Meldungen verarbeitet, die bei Verwendung dieses Dialogfelds generiert werden. 
  
Profile sind ähnlich organisiert wie die Datei Mapisvc.inf. Profile verfügen über verknüpfte hierarchische Abschnitte; Dienstanbieter besitzen Abschnitte auf der untersten Ebene, Nachrichtendienste eigene Abschnitte auf der mittleren Ebene und MAPI besitzt Abschnitte auf der höchsten Ebene. Jeder Abschnitt wird mit einem eindeutigen Bezeichner identifiziert, der als [MAPIUID](mapiuid.md)bezeichnet wird. Die MAPI-Abschnitte enthalten interne Informationen für die MAPI, z. B. die Bezeichner aller Nachrichtendienstprofilabschnitte und Links zu jedem der anderen Abschnitte. Jeder Nachrichtendienstabschnitt speichert Links zu seinen Anbieterabschnitten, und jeder Anbieterabschnitt speichert einen Link zu seinem Dienstabschnitt. 
  
Die folgende Abbildung zeigt den Inhalt von zwei typischen Profilen. Sam verfügt über zwei Profile auf seinem Computer, eines für die private Nutzung und eines für die Office-Nutzung. Das Startprofil enthält drei Nachrichtendienste. Nachrichtendienst X ist ein einzelner Anbieterdienst für die Adressbuchverwaltung. Message Services Y und Z verfügen über drei Anbieter – einen Adressbuchanbieter, einen Nachrichtenspeicheranbieter und einen Transportanbieter. Sams Arbeitsprofil enthält zwei verschiedene Nachrichtendienste, von denen jeder über einen Adressbuchanbieter, einen Nachrichtenspeicheranbieter und einen Transportanbieter verfügt. 
  
**Profilbeispiel**
  
![Profilbeispiel](media/amapi_56.gif "Profilbeispiel")
  
Die folgende Abbildung zeigt ein Profil, das zwei Nachrichtendienste enthält. Der Code zum Installieren und Konfigurieren der Dienstanbieter, die zum Nachrichtendienst gehören, befindet sich in derselben DLL wie der Code für die Anbieter. Dieser Code liest Informationen zum Zeitpunkt der Anmeldung aus dem Profil, um die Dienstanbieter zu konfigurieren, und fordert den Benutzer, falls möglich und erforderlich, auf fehlende Informationen hin. Anforderungen von einem Client zum Anzeigen oder Ändern von Konfigurationseinstellungen für einen der Anbieter werden auch von diesem allgemeinen Code behandelt.
  
**Installieren und Konfigurieren von Serviceanbietern**
  
![Installieren und Konfigurieren von Serviceanbietern](media/amapi_55.gif "Installieren und Konfigurieren von Serviceanbietern")
  
## <a name="see-also"></a>Siehe auch

- [MAPIUID](mapiuid.md)
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)

