---
title: Übersicht über die MAPI-Eigenschaft
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0f214cf8fab62850620b012b2cfd017b340dc013
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579516"
---
# <a name="mapi-property-overview"></a>Übersicht über die MAPI-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Eigenschaft ist ein Attribut eines MAPI-Objekts. Eigenschaften beschreiben etwas über das Objekt, z. B. die Betreffzeile einer Nachricht oder den Adresstyp eines Messagingbenutzers. MAPI definiert viele Eigenschaften, von denen einige viele Objekte beschreiben, und einige, die nur für ein Objekt eines bestimmten Typs geeignet sind. Clients und Dienstanbieter können die MAPI-Gruppe vordefinierter Eigenschaften erweitern, indem sie neue, benutzerdefinierte Eigenschaften erstellen. Clients können Eigenschaften definieren, um neue Nachrichtenklassen zu beschreiben, und Dienstanbieter können Eigenschaften definieren, um die einzigartigen Features ihres Messagingsystems verfügbar zu machen.
  
Eigenschaften können dauerhaft oder temporär sein. Eigenschaften, die von Sitzung zu Sitzung beibehalten werden, können mit den Daten ihrer Objekte oder im Profil gespeichert werden. Temporäre Eigenschaften sind nur für die Dauer der aktuellen Sitzung vorhanden. 
  
Clients und Dienstanbieter können Benutzern Eigenschaften mit einer Tabelle oder einem Eigenschaftenblatt anzeigen. Tabellen bieten Benutzern eine schreibgeschützte Ansicht einiger Eigenschaften, die zu mehreren Objekten gehören. Die Daten werden im Zeilen- und Spaltenformat angezeigt, wobei jede Zeile ein Objekt und jede Spalte eine Eigenschaft darstellt. Eigenschaftenblätter sind Dialogfelder mit Registerkarten, in denen verwandte Eigenschaften für ein einzelnes Objekt angezeigt werden. Eigenschaftenblätter können schreibgeschützt oder Lese-/Schreibzugriff auf die Daten bieten. Ob ein Benutzer Änderungen vornehmen darf, hängt vom Implementierer des Eigenschaftenblatts ab.
  
Die [IMAPIProp-Schnittstelle](imapipropiunknown.md) ist die primäre Schnittstelle zum Arbeiten mit Eigenschaften. Alle Objekte, die Eigenschaften unterstützen, implementieren **IMAPIProp.** **IMAPIProp** enthält Methoden zum Abrufen von Eigenschaftswerten, Kopieren von Eigenschaften, Vornehmen von Änderungen und Speichern dieser Änderungen, Zuordnen zwischen Eigenschaftennamen und deren Bezeichnern und Abrufen von Informationen zu einem vorherigen Fehler. 
  
Es gibt mehrere Datenstrukturen zum Beschreiben von Eigenschaften und Informationen zu Eigenschaften. Die am häufigsten verwendeten Strukturen sind die [SPropValue-Struktur](spropvalue.md) und die [SPropTagArray-Struktur.](sproptagarray.md) Die **SPropValue-Struktur** enthält die drei Informationen, die eine Eigenschaft beschreiben: 
  
- Daten oder Wert der Eigenschaft.
    
- Datentyp des Eigenschaftswerts, z. B. ganze Zahl oder Boolescher Wert. 
    
- Numerischer Wert innerhalb eines bestimmten Bereichs, der die Eigenschaft und Komponente eindeutig identifiziert, die für deren Verwaltung verantwortlich ist. Beispielsweise gibt es einen Bereich für nachrichteninhaltseigenschaften, die von MAPI definiert wurden, und einen anderen Bereich für Nachrichteninhaltseigenschaften, die von einem Client für eine benutzerdefinierte Nachrichtenklasse definiert wurden. 
    
Der Eigenschaftstyp und der Bezeichner werden in einer einzigen Komponente zusammengefasst, die als Eigenschaftstag bezeichnet wird. Eigenschaftstags sind Konstanten, mit denen auf einfache Weise auf die Eigenschaft verwiesen werden kann. Eigenschaftstags für von MAPI definierte Eigenschaften sind in MAPITAGS enthalten. H-Headerdatei und im **ulPropTag-Element** einer **SPropValue-Struktur.** Clients und Dienstanbieter verwenden Eigenschaftstags, um die entsprechenden Eigenschaften zu identifizieren, abzurufen und zu aktualisieren. 
  
Die **SPropTagArray-Struktur** ist ein gezähltes Array von Eigenschaftstags. Viele der Methoden in **IMAPIProp** und anderen Schnittstellen verwenden eine **SPropTagArray-Struktur** zum Beschreiben von Eigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

