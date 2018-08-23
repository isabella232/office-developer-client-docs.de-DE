---
title: Message-Dienste und Profile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 60a102a68ee11cd6002be9edf47d0cee93ed2e15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581433"
---
# <a name="message-services-and-profiles"></a>Message-Dienste und Profile
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Einige Benutzer benötigen die Dienste von verschiedenen Messagingsystemen, jeweils mit mindestens einem Dienstanbieter. Da es ist schwierig zu installieren und konfigurieren Sie jeden dieser Dienstanbieter einzeln und messaging-Server in der Regel eine Gruppe von verwandten Anbieter alle seine Funktionen verfügbar machen muss, enthält MAPI das Konzept eines Diensts Nachricht. Message-Dienste unterstützen Benutzer beim Installieren und Konfigurieren von ihren Dienstanbieter.
  
Erstellen eines Diensts Nachricht ein Entwickler schreibt eine Nachricht-Diensteintrag Point-Programm, die Konfiguration der einzelnen Anbieter in der Dienst und ein Setup-Programm für folgende Aufgaben behandelt:
  
- Installieren Sie aller Dienstanbieter im Dienst.
    
- Erstellen Sie Registrierung und Initialisierung Einträge in der Datei.
    
- Erstellen Sie Einträge in der MAPI-Konfigurationsdatei Mapisvc.inf.
    
Die Datei "Mapisvc.inf" enthält Informationen zur Konfiguration aller Message-Dienste und-Dienstanbieter, die auf dem Computer installiert. Es wird mit jeder verknüpft zur nächsten Stufe in hierarchische Abschnitten angeordnet. Klicken Sie oben sind drei Abschnitte, die Folgendes enthalten: 
  
- Eine Liste der Nachricht Service-Hilfedateien.
    
- Eine Liste der wichtigsten oder in der Standardeinstellung Message-Dienste.
    
- Eine Liste aller Dienste auf dem Computer.
    
Die nächste Ebene enthält Abschnitte für jeden Nachrichtendienst und die letzte Ebene enthält Abschnitte für jeden Anbieter in einem Dienst. MAPI erfordert, dass Entwickler der Dienstanbieter und Message Dienste Mapisvc.inf bestimmte Einträge hinzufügen. Entwickler können ihre eigenen Ermessen anderen Einträge hinzufügen. Die meisten Informationen in Mapisvc.inf letztendlich in eine oder mehrere Profile, eine Auflistung von Konfigurationsinformationen für eines Benutzers bevorzugte Satz von Message-Dienste. Da mehrere Benutzer über einen Computer verfügen kann und ein einzelner Benutzer kann mehrere Sätze von Voreinstellungen haben, können auf einem Computer viele Profile vorhanden. Jedes Profil wird eine andere Menge von Message-Dienste beschrieben. Mehrere Profile ermöglicht einen Benutzer, beispielsweise zu Hause einen Satz mit einem anderen Satz von Message-Dienste und sich im Büro entwickelt.
  
Profile werden während der Installation von Message Service oder Anmeldung von einer Clientanwendung erstellt, die Konfiguration unterstützt. MAPI bietet zwei solche Client Applications: eines Systemsteuerungsobjekts und der Profil-Assistent. Das Systemsteuerungselement ist eine kompletter Service Configuration-Anwendung, mit der Benutzer können erstellen, löschen, bearbeiten, und Kopieren von Profilen sowie nehmen Sie Änderungen vor, um die Einträge in einem Profil. Der Profil-Assistent ist eine einfache Anwendung, die mit dem Hinzufügen einer Messagingdiensts zu einem Profil so einfach wie möglich. Der Profil-Assistent besteht aus einer Reihe von Dialogfeldern, aufgerufen, die den Benutzer durch den Prozess der Installation und Konfiguration eines Diensts auffordern Eigenschaftenseiten. Der Benutzer ist nur für Werte für die wichtigsten Einstellungen aufgefordert. Alle anderen Einstellungen erben die Standardwerte. Nachdem das Profil erstellt wurde, sind Benutzer nicht zulässig, um Änderungen vorzunehmen. 
  
Während der das Systemsteuerungselement immer über die Systemsteuerung aufgerufen wird, sind eine Vielzahl von Szenarien, in denen der Profil-Assistent aus aufgerufen werden. Clientanwendungen können Aufrufen der Profil-Assistent zum Erstellen eines Standardprofils bei der Anmeldung, wenn eine nicht noch erstellt wurde. Statt die Implementierung von Code zum Hinzufügen eines Profils, kann das Systemsteuerungselement oder einer anderen Clientanwendung auf die Funktionalität bereits in der Profil-Assistent verlassen. Ein Nachrichtendienst kann im zugehörigen Eintrag Punkt der Profil-Assistent beim Aufrufen der Dienst muss das Standardprofil hinzugefügt werden. Message-Dienste, die den Profil-Assistenten verwenden, müssen ein zusätzlicher Eintrag-Funktion und standardmäßigen Windows-Dialogfeld Feld Prozedur schreiben. Der Profil-Assistent Ruft die Eintrags-Funktion, um im Dialogfeld Konfiguration des Dienstes abzurufen, während das Dialogfeld Feld Verfahren die Nachrichten, die generiert werden verarbeitet, wenn das Dialogfeld verwendet wird. 
  
Profile sind in der Datei "Mapisvc.inf" ähnlich wie organisiert. Profile haben hierarchische Abschnitte verknüpft. Service Provider eigenen Abschnitte in der untersten Ebene, Message Dienste besitzen Abschnitte in der mittleren Ebene, und MAPI Abschnitte in der höchsten Ebene besitzt. Jeder Abschnitt wird durch eine eindeutige ID, die als eine [MAPIUID](mapiuid.md)bezeichnet identifiziert. Die MAPI-Abschnitte enthalten Informationen, die interne MAPI, wie die IDs aller die Nachricht Service Profil Abschnitte und Links zu den anderen Abschnitten. Jeder Abschnitt Nachricht Service speichert Links zu den Abschnitten Anbieter und jede Anbieterabschnitt speichert einen Link zu einem Abschnitt Service. 
  
Die folgende Abbildung zeigt den Inhalt der beiden typische Profile. SAM hat zwei Profile auf seinem Computer, einen für die private Nutzung und einen für die Verwendung von Office. Das private Profil enthält drei Message-Dienste. Nachricht Service X ist ein einzelner Anbieterdienst für die adressbuchverwaltung. Nachricht Services Y und Z haben drei Anbieter – Adressbuch-Dienstanbieter, eine Nachricht Speicheranbieter und eines Transportdienstes. SAM Arbeit Profil enthält zwei unterschiedlichen Nachrichten, die Dienste, von die jedes Adressbuch-Dienstanbieter, eine Nachricht Speicheranbieter und eines Transportdienstes hat. 
  
**Profilbeispiel**
  
![Profilbeispiel] (media/amapi_56.gif "Profilbeispiel")
  
Die folgende Abbildung zeigt ein Profil, das zwei Nachrichtendienste enthält. Der Code zum Installieren und Konfigurieren der Dienstanbieter, die den Dienst angehören, befindet sich in derselben DLL-Datei wie der Code für den Anbieter. Dieser Code liest Informationen aus dem Profil bei der Anmeldung die-Dienstanbieter zu konfigurieren, und sie werden aufgefordert, den Benutzer, wenn möglich und gegebenenfalls fehlende Informationen. Durch diesen Code allgemeine gekennzeichnete auch Anfragen von einem Client anzeigen oder Ändern von Konfigurationseinstellungen für den Anbieter.
  
**Installieren und Konfigurieren von Serviceanbietern**
  
![Installieren und Konfigurieren von Dienstanbietern] (media/amapi_55.gif "Installieren und Konfigurieren von Dienstanbietern")
  
## <a name="see-also"></a>Siehe auch

- [MAPIUID](mapiuid.md)
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)

