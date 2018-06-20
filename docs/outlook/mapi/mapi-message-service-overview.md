---
title: Übersicht über den MAPI-Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fc444725aae20e7321fa287a90cf7d3e13b7ffb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793010"
---
# <a name="mapi-message-service-overview"></a>Übersicht über den MAPI-Nachricht
  
**Betrifft**: Outlook 
  
Eine Message Service definiert eine Gruppe von verwandten Dienstanbieter in der Regel selben Nachrichtensystem entwickelt Dienstanbieter. Während der Dienstanbieter die Arbeit der Kommunikation zwischen Messagingsystemen und MAPI-Subsystems auszuführen, führen Sie Message Dienste die Arbeit der Interaktion zwischen dem Benutzer und dem Dienstanbieter, die mit einem gemeinsamen Messagingsystem arbeiten.  
  
Message-Dienste vorhanden sein, um die Installation und Konfiguration der Dienstanbieter für Benutzer zu vereinfachen. Benutzer nie direkt installieren oder Konfigurieren von einem Dienstanbieter; Message-Dienst verarbeitet vollständig die Installation und Konfiguration der einzelnen-Dienstanbieter, die mit dem Dienst gehören. Aufgrund dieser Funktion müssen Benutzer nicht mit bestimmten Service Provider konfigurationsanforderungen vertraut sein. 
  
Die folgende Abbildung zeigt die Beziehung zwischen einem messaging-basierte Clientanwendung und zwei Message-Dienste.
  
**Nachricht Installation und Konfiguration des**
  
![Nachricht Installation und Konfiguration des] (media/amapi_44.gif "Nachricht Installation und Konfiguration des")
  
Der Benutzer ruft den Installationscode über die verschiedenen Dienste Nachricht an den Dienst und dessen Dienstanbieter zu einem Profil hinzufügen. In einer Nachricht Dienste in der Abbildung dargestellt gibt es drei-Dienstanbieter. in den anderen Messagingdiensts sind zwei-Dienstanbieter. Zu einem späteren Zeitpunkt nach Abschluss der Installation werden in der Regel bei der Anmeldung die-Dienstanbieter in jeder Nachrichtendienst konfiguriert. Konfigurationscode für jeden Nachrichtendienst behandelt die Konfiguration der Anbieter im Dienst.
  
Wenn ein Nachrichtendienst installiert ist, dessen Installationsprogramm erforderliche Dateien aus der Installationsquelle auf den lokalen Datenträger des Benutzers kopiert und eine Konfigurationsdatei Mapisvc.inf aktualisiert. Die Datei "Mapisvc.inf" enthält die Konfigurationseinstellungen für alle Message-Dienste und Dienstanbieter, die auf dem Computer installiert werden können. Es ist in hierarchische Abschnitte mit Verknüpfungen zwischen jedem Abschnitt auf jeder Ebene angeordnet. Der Abschnitt auf der obersten Ebene enthält Informationen, die für die MAPI-Subsystems, wie eine Liste aller verfügbaren Nachricht Dienste, und der online-Hilfe-Installation relevant sind. Die nächste Ebene weist Abschnitte für jeden Nachrichtendienst mit Informationen wie der Name der DLL-Datei des Dienstes Nachricht und den Namen der Funktion Punkt Eintrag Konfiguration. Die dritte Ebene weist Abschnitte mit Konfigurationsdaten für jede Dienstanbieter in den Dienst. 
  
Behandeln Sie Konfiguration implementiert eine Message Service eine Eintrag Point-Funktion, die mit einem Prototyp von MAPI und ein Dialogfeld bekannt als ein Eigenschaftenblatt definierten entspricht. MAPI-Aufrufen der Einstiegspunkt zu Service-Anfragen, die mit profilverwaltung und die Verwaltung der Dienstanbieter in der Nachrichtendienst verknüpft sind. Eigenschaftenseiten dienen zum Anzeigen und Ändern von Messagingdiensts und Service Provider Konfigurationseigenschaften. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und die Architektur](mapi-features-and-architecture.md)

