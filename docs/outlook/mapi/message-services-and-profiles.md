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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356960"
---
# <a name="message-services-and-profiles"></a>Nachrichtendienste und Profile
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Benutzer benötigen die Dienste mehrerer Messagingsysteme, die jeweils einen oder mehrere Dienstanbieter aufweisen. Da es umständlich ist, jeden dieser Dienstanbieter einzeln zu installieren und zu konfigurieren, und da ein Messaging Server in der Regel eine Gruppe verwandter Anbieter benötigt, um alle Funktionen verfügbar zu machen, enthält MAPI das Konzept eines Nachrichtendiensts. Nachrichtendienste helfen Benutzern bei der Installation und Konfiguration Ihrer Dienstanbieter.
  
Zum Erstellen eines Nachrichtendiensts schreibt ein Entwickler ein Entry Point-Programm für den Nachrichtendienst, um die Konfiguration der einzelnen Anbieter im Dienst und ein Setupprogramm für Folgendes zu übernehmen:
  
- Installieren Sie jeden Anbieter im Dienst.
    
- Erstellen Sie Registrierungs-und Initialisierungsdatei Einträge.
    
- Erstellen Sie Einträge in der MAPI-Konfigurationsdatei MAPISVC. inf.
    
Die Datei MAPISVC. inf enthält Informationen zur Konfiguration aller Nachrichtendienste und Dienstanbieter, die auf dem Computer installiert sind. Sie ist in hierarchischen Abschnitten gegliedert, wobei jede Ebene mit der nächsten verknüpft ist. Oben befinden sich drei Abschnitte, die Folgendes enthalten: 
  
- Eine Liste der Hilfedateien des Nachrichtendiensts.
    
- Eine Liste der wichtigsten oder standardmäßigen Nachrichtendienste.
    
- Eine Liste aller Dienste auf dem Computer.
    
Die nächste Ebene enthält Abschnitte für jeden Nachrichtendienst, und die letzte Ebene enthält Abschnitte für jeden Dienstanbieter in einem Dienst. MAPI erfordert, dass Entwickler von Dienstanbietern und Nachrichtendiensten bestimmte Einträge zu MAPISVC. inf hinzufügen; Entwickler können weitere Einträge nach eigenem Ermessen hinzufügen. Die meisten Informationen in MAPISVC. inf enden in einem oder mehreren Profilen, einer Sammlung von Konfigurationsinformationen für die bevorzugten Nachrichtendienste eines Benutzers. Da ein Computer mehrere Benutzer haben kann und ein einzelner Benutzer über mehrere Einstellungssätze verfügen kann, können viele Profile auf einem Computer vorhanden sein. Jedes Profil beschreibt einen anderen Satz von Nachrichtendiensten. Durch die Verwendung mehrerer Profile kann ein Benutzer beispielsweise zu Hause mit einem Satz von Nachrichtendiensten und im Büro mit einem anderen Satz arbeiten.
  
Profile werden bei der Installation oder Anmeldezeit des Nachrichtendiensts von einer Clientanwendung erstellt, die Konfigurationsunterstützung bereitstellt. MAPI bietet zwei solcher Clientanwendungen: ein Element der Systemsteuerung und den Profil-Assistenten. Bei dem Element der Systemsteuerung handelt es sich um eine vollständige Konfigurationsanwendung, mit der Benutzerprofile erstellen, löschen, bearbeiten und kopieren sowie Änderungen an den Einträgen in einem Profil vornehmen können. Der Profil-Assistent ist eine einfache Anwendung, die das Hinzufügen eines Nachrichtendiensts zu einem Profil so einfach wie möglich macht. Der Profil-Assistent besteht aus einer Reihe von Dialogfeldern, die als Eigenschaftenseiten bezeichnet werden und den Benutzer bei der Installation und Konfiguration eines Diensts auffordern. Der Benutzer wird nur für Werte für die kritischsten Einstellungen aufgefordert; alle anderen Einstellungen erben die Standardwerte. Nachdem das Profil erstellt wurde, dürfen Benutzer keine Änderungen vornehmen. 
  
Während das Element der Systemsteuerung immer über die Systemsteuerung aufgerufen wird, gibt es eine Reihe von Szenarien, die dazu führen können, dass der Profil-Assistent aufgerufen wird. Client Anwendungen können den Profil-Assistenten aufrufen, um ein Standardprofil zum Zeitpunkt der Anmeldung zu erstellen, wenn noch keine erstellt wurde. Anstatt Code erneut zu implementieren, um ein Profil hinzuzufügen, kann das Element der Systemsteuerung oder eine andere Clientanwendung die Funktionen verwenden, die sich bereits im Profil-Assistenten befinden. Ein Nachrichtendienst kann in seiner Einstiegspunktfunktion den Profil-Assistenten aufrufen, wenn der Dienst dem Standardprofil hinzugefügt werden muss. Nachrichtendienste, die den Profil-Assistenten verwenden, müssen eine zusätzliche Einstiegspunktfunktion und eine Windows-Standarddialogfelder-Prozedur schreiben. Der Profil-Assistent ruft die Einstiegspunktfunktion auf, um das Konfigurationsdialogfeld des Diensts abzurufen, während die Dialogfeldprozedur die Nachrichten verarbeitet, die bei Verwendung dieses Dialogfelds generiert werden. 
  
Profile werden ähnlich wie die Datei "Mapisvc. inf" organisiert. Profile haben verknüpfte hierarchische Abschnitte; Dienstanbieter eigene Abschnitte in der untersten Ebene, Nachrichtendienste eigene Abschnitte in der mittleren Ebene und MAPI besitzt Abschnitte auf höchster Ebene. Jeder Abschnitt wird mit einem eindeutigen Bezeichner identifiziert, der als [MAPIUID](mapiuid.md)bezeichnet wird. Die MAPI-Abschnitte enthalten interne Informationen zu MAPI, wie die Bezeichner aller Profile des Nachrichtendienst Profils und Links zu den einzelnen Abschnitten. Jeder Nachrichtendienst Abschnitt speichert Links zu seinen Anbieter Abschnitten, und jeder Anbieterabschnitt speichert einen Link zu seinem Dienst Abschnitt. 
  
Die folgende Abbildung zeigt die Inhalte von zwei typischen Profilen. Sam hat zwei Profile auf seinem Computer, eine für die private Nutzung und eine für die Office-Verwendung. Das Startprofil enthält drei Nachrichtendienste. Message Service X ist ein einzelner Anbieterdienst für die Adressbuchverwaltung. Nachrichtendienste Y und Z verfügen über drei Anbieter: einen Adressbuchanbieter, einen Nachrichtenspeicher Anbieter und einen Transportanbieter. Sams Arbeitsprofil enthält zwei verschiedene Nachrichtendienste, von denen jeder einen Adressbuchanbieter, einen Nachrichtenspeicher Anbieter und einen Transportanbieter besitzt. 
  
**Profilbeispiel**
  
![Profil Beispiel] (media/amapi_56.gif "Profil Beispiel")
  
Die folgende Abbildung zeigt ein Profil mit zwei Nachrichtendiensten. Der Code für die Installation und Konfiguration der Dienstanbieter, die zum Nachrichtendienst gehören, befindet sich in derselben DLL wie der Code für die Anbieter. Dieser Code liest Informationen aus dem Profil bei der Anmeldung, um die Dienstanbieter zu konfigurieren, und fordert den Benutzer auf, wenn möglich und erforderlich, fehlende Informationen zu erhalten. Anforderungen von einem Client zum Anzeigen oder Ändern von Konfigurationseinstellungen für einen der Anbieter werden ebenfalls durch diesen gemeinsamen Code behandelt.
  
**Installieren und Konfigurieren von Serviceanbietern**
  
![Installieren und Konfigurieren von Dienstanbietern] (media/amapi_55.gif "Installieren und Konfigurieren von Dienstanbietern")
  
## <a name="see-also"></a>Siehe auch

- [MAPIUID](mapiuid.md)
- [�bersicht �ber die MAPI-Programmierung](mapi-programming-overview.md)

