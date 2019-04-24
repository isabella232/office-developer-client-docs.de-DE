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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328201"
---
# <a name="mapi-property-overview"></a>Übersicht über die MAPI-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Eigenschaft ist ein Attribut eines MAPI-Objekts. Eigenschaften beschreiben etwas über das Objekt, beispielsweise die Betreffzeile einer Nachricht oder den Adresstyp eines Messaging Benutzers. MAPI definiert viele Eigenschaften, einige zur Beschreibung vieler Objekte und einige, die nur für ein Objekt eines bestimmten Typs geeignet sind. Clients und Dienstanbieter können die vordefinierten Eigenschaften von MAPI erweitern, indem Sie neue, benutzerdefinierte Eigenschaften erstellen. Clients können Eigenschaften definieren, um neue Nachrichtenklassen zu beschreiben, und Dienstanbieter können Eigenschaften definieren, um die eindeutigen Features Ihres Messagingsystems verfügbar zu machen.
  
Eigenschaften können persistent oder temporär sein. Eigenschaften, die von Sitzung zu Sitzung beibehalten werden, können mit den Daten Ihrer Objekte oder im Profil gespeichert werden. Temporäre Eigenschaften sind nur für die Dauer der aktuellen Sitzung vorhanden. 
  
Clients und Dienstanbieter können Eigenschaften für Benutzer mit einer Tabelle oder einem Eigenschaftenblatt anzeigen. Tabellen bieten Benutzern eine schreibgeschützte Ansicht einiger der Eigenschaften, die zu mehreren Objekten gehören. Die Daten werden im Zeilen-und Spaltenformat angezeigt, wobei jede Zeile ein Objekt und jede Spalte eine Eigenschaft darstellt. Eigenschaftenblätter sind Dialogfelder mit Registerkarten, die verwandte Eigenschaften für ein einzelnes Objekt anzeigen. Eigenschaftenblätter können Lese-oder Lese-/Schreibzugriff auf die Daten bereitstellen. Ob ein Benutzer Änderungen vornehmen darf, liegt beim Implementierer des Eigenschaftenblatts.
  
Die [IMAPIProp](imapipropiunknown.md) -Schnittstelle ist die primäre Schnittstelle für das Arbeiten mit Eigenschaften. Alle Objekte, die Eigenschaften unterstützen, implementieren **IMAPIProp**. **IMAPIProp** enthält Methoden zum Abrufen von Eigenschaftswerten, Kopieren von Eigenschaften, vornehmen von Änderungen und Speichern dieser Änderungen, zuordnen zwischen Eigenschaftennamen und ihren Bezeichnern und Abrufen von Informationen zu einem vorherigen Fehler. 
  
Es gibt mehrere Datenstrukturen zum Beschreiben von Eigenschaften und Informationen zu Eigenschaften. Die am häufigsten verwendeten Strukturen sind die [SPropValue](spropvalue.md) -Struktur und die [SPropTagArray](sproptagarray.md) -Struktur. Die **SPropValue** -Struktur enthält die drei Informationen, die eine Eigenschaft beschreiben: 
  
- Daten oder Wert der Eigenschaft.
    
- Datentyp des Werts der Eigenschaft, beispielsweise Integer oder Boolean. 
    
- Numerischer Wert in einem bestimmten Bereich, der die für die Verwaltung verantwortliche Eigenschaft und Komponente eindeutig identifiziert. Beispielsweise gibt es einen Bereich für Nachrichteninhalts Eigenschaften, die von MAPI definiert werden, und einen weiteren Bereich für Nachrichteninhalts Eigenschaften, die von einem Client für eine benutzerdefinierte Nachrichtenklasse definiert werden. 
    
Der Eigenschaftentyp und der Bezeichner werden in einer einzigen Komponente mit dem Namen Property-Tag kombiniert. Eigenschaftstags sind Konstanten, die verwendet werden können, um auf einfache Weise auf die Eigenschaft zu verweisen. Eigenschaftstags für von MAPI definierte Eigenschaften sind in der MAPITAGS enthalten. H-Headerdatei und im **ulPropTag** -Element einer **SPropValue** -Struktur. Clients und Dienstanbieter verwenden Eigenschaftstags, um die entsprechenden Eigenschaften zu identifizieren, abzurufen und zu aktualisieren. 
  
Die **SPropTagArray** -Struktur ist ein Gezähltes Array von Property-Tags. Viele der Methoden in **IMAPIProp** und anderen Schnittstellen verwenden eine **SPropTagArray** -Struktur zur Beschreibung von Eigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

