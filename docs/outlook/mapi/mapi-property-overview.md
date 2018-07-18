---
title: Übersicht über die MAPI-Eigenschaft
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ed11677d09ae5acacced77373b2bca783d1ec0b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793055"
---
# <a name="mapi-property-overview"></a>Übersicht über die MAPI-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Eine Eigenschaft ist ein Attribut eines MAPI-Objekts. Eigenschaften beschreiben etwas über das Objekt, wie etwa der Betreffzeile einer Nachricht oder Adresstyp ein messaging-Benutzer. MAPI definiert viele Eigenschaften, einige viele Objekte beschreiben und einige, die nur für ein Objekt eines bestimmten Typs geeignet sind. Clients und Dienstanbieter können Satz vordefinierter Eigenschaften des MAPI-erweitern, indem Sie neue, benutzerdefinierte Eigenschaften erstellen. Clients können Eigenschaften, um neue Nachrichtenklassen beschreiben definieren, und Dienstanbieter können definieren, Eigenschaften, um die eindeutigen Features messaging-System verfügbar zu machen.
  
Eigenschaften können beständige oder temporäre sein. Eigenschaften, die Sitzung beibehalten können mit ihren Objekten Daten oder im Profil gespeichert werden. Temporäre Eigenschaften sind nur für die Dauer der aktuellen Sitzung vorhanden. 
  
Clients und Dienstanbieter können Eigenschaften für Benutzer mit einer Tabelle oder einem Eigenschaftenfenster anzuzeigen. Tabellen bieten den Benutzern eine schreibgeschützte Ansicht einiger der Eigenschaften von mehreren Objekten. Die Daten werden in der Zeile und Spalte-Format mit jeder Zeile, die ein Objekt, und jeder Spalte eine Eigenschaft darstellt angezeigt. Eigenschaftenseiten sind Dialogfelder mit Registerkarten, die zugehörige Eigenschaften für ein einzelnes Objekt angezeigt werden. Eigenschaftenseiten können bieten schreibgeschützten oder Lese-/Schreibzugriff auf die Daten. Die Implementierung des Eigenschaftenblatts ist unabhängig davon, ob ein Benutzer berechtigt ist, um Änderungen vorzunehmen.
  
Die Schnittstelle [IMAPIProp](imapipropiunknown.md) ist die primäre Schnittstelle zum Arbeiten mit Eigenschaften. Alle Objekte, Eigenschaften unterstützen, implementieren Sie **IMAPIProp**. **IMAPIProp** enthält Methoden zum Abrufen von Eigenschaftswerten, Kopieren von Eigenschaften, ändern und speichern diese Änderungen zwischen Eigenschaftennamen und deren Bezeichner zuordnen und Abrufen von Informationen zu einem früheren Fehler. 
  
Es gibt mehrere Datenstrukturen zum Beschreiben Eigenschaften und Informationen zu Eigenschaften. Die am häufigsten verwendeten Strukturen sind die [SPropValue](spropvalue.md) -Struktur und die [SPropTagArray](sproptagarray.md) -Struktur. Die **SPropValue** -Datenstruktur enthält die drei Teile der Informationen, die eine Eigenschaft beschrieben: 
  
- Daten, oder den Wert, der-Eigenschaft.
    
- Der Datentyp der der Wert der Eigenschaft, wie etwa ganze Zahl oder einen booleschen Wert. 
    
- Der numerische Wert innerhalb eines bestimmten Bereichs, die die Eigenschaft und die Komponente verantwortlich für die Verwaltung von es eindeutig identifizieren. Es ist beispielsweise ein Bereich, halten die Nachricht von Eigenschaften von MAPI und einem anderen Bereich Content Nachrichteneigenschaften gehalten definierten von einem Client für eine benutzerdefinierte Nachrichtenklasse definiert. 
    
Der Eigenschaftentyp und Bezeichner werden in einer einzelnen Komponente aufgerufen, das Eigenschafts-Tag kombiniert. Eigenschaftentags werden Konstanten, mit die auf einfache Weise verweisen auf die Eigenschaft verwendet werden können. Eigenschaftentags für MAPI definierten Eigenschaften sind in der MAPITAGS enthalten. H-Headerdatei und im **UlPropTag** Mitglied einer **SPropValue** Struktur. Clients und -Dienstanbieter verwenden Eigenschaftentags identifizieren, abrufen, und aktualisieren die entsprechenden Eigenschaften an. 
  
Die **SPropTagArray** -Struktur ist ein gezählte Eigenschaftentags-Array. Viele der Methoden in **IMAPIProp** und andere Schnittstellen verwenden eine **SPropTagArray** -Struktur für die Beschreibung von Eigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konzepte (engl.)](mapi-concepts.md)

