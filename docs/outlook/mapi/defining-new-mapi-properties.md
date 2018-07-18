---
title: Definieren von neuen MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 68e877568565cfcc30b60e9b21f55b7dc1600b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791525"
---
# <a name="defining-new-mapi-properties"></a>Definieren von neuen MAPI-Eigenschaften

  
  
**Betrifft**: Outlook 
  
Trotz der Fülle von Eigenschaften von MAPI für die Verwendung durch Clients und -Dienstanbieter bereitgestellt ermöglicht MAPI neue Eigenschaften bei Bedarf erstellt werden soll. Die gültigen Szenarien für die neue öffentliche Eigenschaften definieren gehören einen Client Erstellen von Eigenschaften zur Unterstützung einer neuen Nachrichtenklasse und einem Dienstanbieter Erstellung neuer Eigenschaften einzigartigen Merkmale von messaging System verfügbar machen.
  
Es ist in der Regel nicht gültig für eine-Dienstanbieters für das neue Eigenschaften für einen vorhandenen MAPI-Objekt oder eine Nachrichtenklasse zu definieren. Einer der wichtigsten Vorteile der Verwendung von MAPI ist, dass der standard-IDs und Formate für eine große Anzahl von messaging-System, die Elemente eingerichtet, werden es Benutzern ermöglichen nahtlos mischen und match-Anbieter. Dienstanbieter, die nicht standardmäßige Eigenschaften verwenden, funktionieren nicht auch mit anderen Dienstanbieter. 
  
Clients können Content-Eigenschaften für neue Nachrichtenklassen durch erstellen:
  
- Verwenden von eigenschaftskennungen in einem bestimmten Bereich für Content-Klasse-spezifischen Nachrichteneigenschaften.
    
    - Oder -
    
- Verwenden von benannten Eigenschaften. 
    
Die erste Option ist vorzuziehen, da nicht alle Dienstanbieter benannte Eigenschaften unterstützen. MAPI definiert zwei separate Bereiche für Clients für neue Nachricht-Klasse spezifische Content-Eigenschaften verwenden:
  
- 0x6800: 0x7BFF für Übertragungseinehit-Eigenschaften
    
- 0x7C00: 0x7FFF für Nontransmittable-Eigenschaften
    
Eigenschaftenbezeichner müssen in vordefinierten Bereichen zu verhindern Konflikte zwischen den Eigenschaften, die von anderen Anbietern oder Benutzern definiert liegen. Benutzer von Eigenschaften in diesen Bereichen können nicht jedoch Annahmen über das Verhalten der Eigenschaften treffen. Jeder Client, der eine neue Nachrichtenklasse erstellt hat Zugriff auf diese Bereiche. eine Eigenschaft mit ID _Xxxx_ kann es sich um eine bestimmte Verhaltensweise für eine Nachrichtenklasse und ein anderes Verhalten für einen anderen Nachrichtenklasse bedeuten. 
  
Benannte Eigenschaften werden verwendet, um sicherzustellen, dass eine bestimmte Eigenschaft für eine Nachrichtenklasse eindeutig ist. Benannte Eigenschaftenbezeichner starten im Bereich von 0 x 8000. Clients definieren einen oder mehrere Namen, und rufen Sie dann den Nachrichtenspeicher [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode, um die einzelnen Namen einen Bezeichner zuordnen. Benannte Eigenschaften können neue Eigenschaften für jedes Objekt gilt nur, wenn der Besitzer des Objekts benannte Eigenschaften unterstützt Definieren von Clients oder -Dienstanbieter verwendet werden. Benutzer dieser Eigenschaften anrufen **GetIDsFromNames** sowie die zugehörigen **IMAPIProp** Methode [GetNamesFromIDs](imapiprop-getnamesfromids.md), Zuordnung zwischen einen Namen und des Bezeichners.
  
Alle Eigenschaften, neue oder vorhandene, müssen die vordefinierte Eigenschaftentypen verwenden. Neue Eigenschaftstypen können nicht hinzugefügt werden, und vorhandene Typen können nicht geändert oder gelöscht werden soll. Einfache kleine Eigenschaften, wie einzelne Zeichen oder 16-Bit Ganzzahleigenschaften in einem entsprechenden gespeichert werden können. Beispielsweise ganzen Zahlen als **ULONG** gespeichert werden können und Zeichenfolgen können als **PT_STRING8**gespeichert werden. 
  
Verwenden Sie den **PT_BINARY** -Typ an, dass gezählte Bytearray zurück. In diesem Eigenschaftentyp eignet sich für erweitern die Datentypen, die in einem Objekt gespeichert werden können. Bytes werden in der Abfolge übertragen und keine Annahmen über die Bedeutung der Daten. Wenn eine Clientanwendung Daten aus einer solchen Eigenschaft liest, sind die Daten unverändert aus, wie sie gespeichert wurden. Der Client muss alle erforderlichen Byte Austausch beim Verschieben von Daten über CPUs ausführen. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

