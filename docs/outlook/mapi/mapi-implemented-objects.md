---
title: MAPI-implementierte Objekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 86aa8451b5b127764134f1a3a905366fd014d0c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346855"
---
# <a name="mapi-implemented-objects"></a>MAPI-implementierte Objekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI implementiert mehrere Objekte für die Verwendung durch Clientanwendungen und Dienstanbieter. Mit dem Session-Objekt können Clients Sitzungsdienste verwenden, auf Tabellen zugreifen und mit Dienstanbietern kommunizieren. Das Address Book-Objekt bietet Clients einen integrierten Zugriff auf alle unterschiedlichen Adressbuchanbieter. 
  
MAPI stellt mehrere Table-und Status-Objekte für Clients bereit, die zum Anzeigen und Überwachen von Sitzungs-und Dienstanbieterinformationen verwendet werden können. MAPI stellt beispielsweise eine Profiltabelle mit Informationen zu allen Profilen bereit, die auf dem Computer installiert sind, und eine Nachrichtendienst Tabelle mit Informationen zu allen Nachrichtendiensten im aktuellen Profil. MAPI bietet drei verschiedene Statusobjekte: eine, die das Gesamt Subsystem, eine für den MAPI-Spooler und eine für das integrierte Adressbuch darstellt. 
  
MAPI implementiert vier verschiedene Objekte zum Verwalten der Konfiguration von Nachrichtendiensten, Dienstanbietern und Profilen. Sowohl Clients als auch Dienstanbieter verwenden Anbieterverwaltung und Profil Abschnitts Objekte; mit diesen Objekten können Sie Dienstanbieter konfigurieren und auf Profileigenschaften zugreifen. Clients verwenden nur Nachrichtendienst-und Profil Verwaltungsobjekte, die Objekte, die die Verwaltung von Nachrichtendiensten und-Profilen unterstützen. 
  
MAPI stellt zwei Objekte für Dienstanbieter bereit: ein Support-Objekt und ein TNEF-Objekt. Alle Dienstanbieter verwenden ein oder mehrere Support-Objekte; Es gibt vier verschiedene Unterstützungsobjekt Implementierungen. MAPI bietet eine Implementierung zur Unterstützung der Konfiguration sowie spezifische Implementierungen zur Unterstützung von Adressbuch-, Nachrichtenspeicher-und Transportanbietern. Das TNEF-Objekt wird von Transportanbietern verwendet, die das TNEF (Transport Neutral Encapsulation Format) unterstützen.
  
Zwei Hilfsobjekte, Tabellendaten und Eigenschaftsdaten werden in der Regel von Dienstanbietern verwendet. Tabellendaten Objekte helfen bei der Implementierung von table-Objekten; Eigenschaftendaten Objekte helfen beim Festlegen und Anzeigen von Eigenschaftenzugriff und Hilfe bei der Implementierung von [IMAPIProp: IUnknown](imapipropiunknown.md), die Schnittstelle der Basiseigenschaft. 
  
In der folgenden Tabelle wird der Zweck der einzelnen von MAPI implementierten Objekte zusammengefasst.
  
|**MAPI-Objekt**|**Beschreibung**|
|:-----|:-----|
|Adressbuch  <br/> |Ermöglicht den Zugriff auf die integrierte Ansicht von Empfängerinformationen, die zu allen Adressbuch Anbietern im aktiven Profil gehört.  <br/> |
|Nachrichtendienst Verwaltung  <br/> |Ermöglicht den Zugriff auf Nachrichtendienst Informationen für die Konfiguration.  <br/> |
|Profilverwaltung  <br/> |Ermöglicht den Zugriff auf Profilinformationen für die Konfiguration.  <br/> |
|Profil Abschnitt  <br/> |Ein Teil eines Profils, mit dem ein bestimmter Nachrichtendienst oder Dienstanbieter beschrieben wird.  <br/> |
|Eigenschaftendaten  <br/> |Verwaltet den Zugriff auf Eigenschaften und hilft bei der Implementierung von **IMAPIProp**.  <br/> |
|Anbieterverwaltung  <br/> |Ermöglicht den Zugriff auf Dienstanbieterinformationen für die Konfiguration.  <br/> |
|Sitzung  <br/> |Stellt eine Verbindung zu zugrunde liegenden Messagingsystemen dar und bietet Clients Zugriff auf MAPI-Ressourcen.  <br/> |
|Status  <br/> |Ermöglicht den Zugriff auf den Status des MAPI-Subsystems, des Adressbuchs oder des MAPI-Spoolers.  <br/> |
|Support  <br/> |UnterStützt Dienstanbieter beim Verarbeiten von Clientanforderungen.  <br/> |
|Tabelle  <br/> |Ermöglicht den Zugriff auf eine Zusammenfassungsansicht von Objektdaten im Zeilen-und Spaltenformat, ähnlich wie bei einer Datenbanktabelle.  <br/> |
|Tabellendaten  <br/> |Verwaltet den Zugriff auf zugrunde liegende Tabellendaten und implementiert Table-Objekte.  <br/> |
|TNEF  <br/> |Unterstützt die Verwendung des Transport Neutral Encapsulation Format (TNEF).  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen den Objekten, die MAPI implementiert, den Schnittstellen, von denen Sie erben, und den Komponenten, die Sie verwenden. 
  
**Von MAPI implementierte Objekte**
  
Von ![MAPI implementierte Objekte] Von (media/amapi_68.gif "MAPI implementierte Objekte")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Übersicht über MAPI-Objekte und-Schnittstellen](mapi-object-and-interface-overview.md)

