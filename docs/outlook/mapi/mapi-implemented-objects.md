---
title: MAPI-implementierte Objekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 230b7483f284d57a9473502c9c8f21f0f7d85160
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556182"
---
# <a name="mapi-implemented-objects"></a>MAPI-implementierte Objekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI implementiert mehrere Objekte zur Verwendung durch Clientanwendungen und Dienstanbieter. Das Sitzungsobjekt ermöglicht Clients die Verwendung von Sitzungsdiensten, den Zugriff auf Tabellen und die Kommunikation mit Dienstanbietern. Das Adressbuchobjekt bietet Clients integrierten Zugriff auf alle verschiedenen Adressbuchanbieter. 
  
MAPI stellt mehrere Tabellen- und Statusobjekte für Clients bereit, die zum Anzeigen und Überwachen von Sitzungs- und Dienstanbieterinformationen verwendet werden können. Die MAPI stellt beispielsweise eine Profiltabelle mit Informationen zu allen profilen bereit, die auf dem Computer installiert sind, und eine Nachrichtendiensttabelle mit Informationen zu allen Nachrichtendiensten im aktuellen Profil. MAPI stellt drei verschiedene Statusobjekte bereit: eines, das das gesamte Subsystem darstellt, eines für den MAPI-Spooler und eines für das integrierte Adressbuch. 
  
MAPI implementiert vier verschiedene Objekte zum Verwalten der Konfiguration von Nachrichtendiensten, Dienstanbietern und Profilen. Sowohl Clients als auch Dienstanbieter verwenden Anbieterverwaltungs- und Profilabschnittsobjekte. Diese Objekte ermöglichen es ihnen, Dienstanbieter zu konfigurieren und auf Profileigenschaften zuzugreifen. Clients verwenden nur Nachrichtendienst- und Profilverwaltungsobjekte, die Objekte, die die Verwaltung von Nachrichtendiensten und -profilen unterstützen. 
  
MAPI stellt zwei Objekte für Dienstanbieter bereit: ein Supportobjekt und ein TNEF-Objekt. Alle Dienstanbieter verwenden ein oder mehrere Supportobjekte. Es gibt vier verschiedene Unterstützungsobjektimplementierungen. MAPI stellt eine Implementierung zur Unterstützung der Konfiguration sowie spezifische Implementierungen zur Unterstützung von Adressbuch-, Nachrichtenspeicher- und Transportanbietern bereit. Das TNEF-Objekt wird von Transportanbietern verwendet, die das Transport Neutral Encapsulation Format (TNEF) unterstützen.
  
Zwei Hilfsprogrammobjekte, Tabellendaten und Eigenschaftendaten, werden in der Regel von Dienstanbietern verwendet. Tabellendatenobjekte helfen bei der Implementierung von Tabellenobjekten. Eigenschaftsdatenobjekte helfen beim Festlegen und Anzeigen des Eigenschaftszugriffs und bei der Implementierung von [IMAPIProp : IUnknown](imapipropiunknown.md), der Basiseigenschaftsschnittstelle. 
  
In der folgenden Tabelle wird der Zweck der einzelnen Objekte zusammengefasst, die mapi implementiert.
  
|**MAPI-Objekt**|**Beschreibung**|
|:-----|:-----|
|Adressbuch  <br/> |Bietet Zugriff auf die integrierte Ansicht von Empfängerinformationen, die zu allen Adressbuchanbietern im aktiven Profil gehören.  <br/> |
|Nachrichtendienstverwaltung  <br/> |Ermöglicht den Zugriff auf Nachrichtendienstinformationen für die Konfiguration.  <br/> |
|Profilverwaltung  <br/> |Ermöglicht den Zugriff auf Profilinformationen für die Konfiguration.  <br/> |
|Profilabschnitt  <br/> |Ein Teil eines Profils, das verwendet wird, um einen bestimmten Nachrichtendienst oder Dienstanbieter zu beschreiben.  <br/> |
|Eigenschaftendaten  <br/> |Verwaltet den Zugriff auf Eigenschaften und hilft bei der Implementierung von **IMAPIProp.**  <br/> |
|Anbieterverwaltung  <br/> |Ermöglicht den Zugriff auf Dienstanbieterinformationen für die Konfiguration.  <br/> |
|Sitzung  <br/> |Stellt eine Verbindung mit zugrunde liegenden Messagingsystemen dar und bietet Clients Zugriff auf MAPI-Ressourcen.  <br/> |
|Status  <br/> |Bietet Zugriff auf den Status des MAPI-Subsystems, des Adressbuchs oder des MAPI-Spoolers.  <br/> |
|Support  <br/> |Hilft Dienstanbietern bei der Verarbeitung von Clientanforderungen.  <br/> |
|Tabelle  <br/> |Bietet Zugriff auf eine Zusammenfassungsansicht der Objektdaten im Zeilen- und Spaltenformat, ähnlich einer Datenbanktabelle.  <br/> |
|Tabellendaten  <br/> |Behält den Zugriff auf zugrunde liegende Tabellendaten bei und implementiert Tabellenobjekte.  <br/> |
|TNEF  <br/> |Unterstützt die Verwendung des Transport Neutral Encapsulation Format (TNEF).  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen den von MAPI implementierten Objekten, den Schnittstellen, von denen sie erben, und den Komponenten, die sie verwenden. 
  
**Von MAPI implementierte Objekte**
  
![Von MAPI implementierte Objekte](media/amapi_68.gif "Von MAPI implementierte Objekte")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

