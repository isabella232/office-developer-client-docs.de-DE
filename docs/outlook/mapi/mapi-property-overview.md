---
title: Übersicht über die MAPI-Eigenschaft
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 99887bab2b576e6e6c05414ee9daf1bd6e8d0463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408327"
---
# <a name="mapi-property-overview"></a>Übersicht über die MAPI-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Eigenschaft ist ein Attribut eines MAPI-Objekts. Eigenschaften beschreiben etwas über das Objekt, z. B. die Betreffzeile einer Nachricht oder den Adresstyp eines Messagingbenutzers. MAPI definiert viele Eigenschaften, einige zur Beschreibung vieler Objekte und einige, die nur für ein Objekt eines bestimmten Typs geeignet sind. Clients und Dienstanbieter können den Satz vordefinierter Eigenschaften von MAPI erweitern, indem neue, benutzerdefinierte Eigenschaften erstellt werden. Clients können Eigenschaften definieren, um neue Nachrichtenklassen zu beschreiben, und Dienstanbieter können Eigenschaften definieren, um die eindeutigen Features ihres Messagingsystems verfügbar zu machen.
  
Eigenschaften können dauerhaft oder temporär sein. Eigenschaften, die von Sitzung zu Sitzung beibehalten werden, können mit den Daten ihrer Objekte oder im Profil gespeichert werden. Temporäre Eigenschaften sind nur für die Dauer der aktuellen Sitzung vorhanden. 
  
Clients und Dienstanbieter können Benutzern Eigenschaften mit einer Tabelle oder einem Eigenschaftenblatt anzeigen. Tabellen bieten Benutzern eine schreibgeschützte Ansicht einiger Eigenschaften, die zu mehreren Objekten gehören. Die Daten werden im Zeilen- und Spaltenformat angezeigt, mit jeder Zeile, die ein Objekt darstellt, und jeder Spalte eine Eigenschaft. Eigenschaftenblätter sind Registerkartendialogfelder, die verwandte Eigenschaften für ein einzelnes Objekt anzeigen. Eigenschaftenblätter können schreibgeschützten Oder Lese-/Schreibzugriff auf die Daten ermöglichen. Ob ein Benutzer Änderungen vornehmen darf, liegt am Implementier des Eigenschaftenblatts.
  
Die [IMAPIProp-Schnittstelle](imapipropiunknown.md) ist die primäre Schnittstelle für das Arbeiten mit Eigenschaften. Alle Objekte, die Eigenschaften unterstützen, implementieren **IMAPIProp**. **IMAPIProp** umfasst Methoden zum Abrufen von Eigenschaftswerten, zum Kopieren von Eigenschaften, zum Vornehmen von Änderungen und Speichern dieser Änderungen, zum Zuordnen zwischen Eigenschaftsnamen und ihren Bezeichnern sowie zum Abrufen von Informationen zu einem vorherigen Fehler. 
  
Es gibt mehrere Datenstrukturen zum Beschreiben von Eigenschaften und Informationen zu Eigenschaften. Die am häufigsten verwendeten Strukturen sind [die SPropValue-Struktur](spropvalue.md) und die [SPropTagArray-Struktur.](sproptagarray.md) Die **SPropValue-Struktur** enthält die drei Informationen, die eine Eigenschaft beschreiben: 
  
- Daten oder Werte der Eigenschaft.
    
- Datentyp des Werts der Eigenschaft, z. B. ganze Zahl oder Boolean. 
    
- Numerischer Wert innerhalb eines bestimmten Bereichs, der die Eigenschaft und Komponente eindeutig identifiziert, die für die Verwaltung verantwortlich sind. Beispielsweise gibt es einen Bereich zum Halten von Nachrichteninhaltseigenschaften, die von MAPI definiert sind, und einen anderen Bereich, um Nachrichteninhaltseigenschaften zu enthalten, die von einem Client für eine benutzerdefinierte Nachrichtenklasse definiert wurden. 
    
Der Eigenschaftentyp und der Bezeichner werden in einer einzelnen Komponente kombiniert, die als Eigenschaftstag bezeichnet wird. Eigenschaftstags sind Konstanten, die zum einfachen Verweisen auf die Eigenschaft verwendet werden können. Eigenschaftstags für eigenschaften, die von MAPI definiert sind, sind in den MAPITAGS enthalten. H-Headerdatei und im **ulPropTag-Element** einer **SPropValue-Struktur.** Clients und Dienstanbieter verwenden Eigenschaftstags, um die entsprechenden Eigenschaften zu identifizieren, abzurufen und zu aktualisieren. 
  
Die **SPropTagArray-Struktur** ist ein gezähltes Array von Eigenschaftstags. Viele der Methoden in **IMAPIProp** und anderen Schnittstellen verwenden eine **SPropTagArray-Struktur** zum Beschreiben von Eigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

