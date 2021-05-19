---
title: Definieren neuer MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 666ee413319765e39e25d586208f764afc93ae6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425015"
---
# <a name="defining-new-mapi-properties"></a>Definieren neuer MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Trotz der Vielzahl von Eigenschaften, die von MAPI für die Verwendung durch Clients und Dienstanbieter bereitgestellt werden, ermöglicht MAPI bei Bedarf das Erstellen neuer Eigenschaften. Zu den gültigen Szenarien zum Definieren neuer öffentlicher Eigenschaften gehören ein Client, der Eigenschaften zur Unterstützung einer neuen Nachrichtenklasse erstellt, und ein Dienstanbieter, der neue Eigenschaften zum Verfügbar machen von eindeutigen Messagingsystemfeatures erstellt.
  
Es ist in der Regel ungültig, dass ein Dienstanbieter neue Eigenschaften für ein vorhandenes MAPI-Objekt oder eine vorhandene Nachrichtenklasse definiert. Einer der wichtigsten Vorteile der Verwendung von MAPI besteht in der Einrichtung von Standardbezeichnern und -formaten für eine große Anzahl von Messagingsystemelementen, sodass Benutzer Dienstanbieter nahtlos kombinieren und absprechen können. Dienstanbieter, die nicht standardmäßige Eigenschaften verwenden, funktionieren nicht so gut mit anderen Dienstanbietern. 
  
Clients können Inhaltseigenschaften für neue Nachrichtenklassen erstellen, indem sie:
  
- Verwenden von Eigenschaftenbezeichnern innerhalb eines festgelegten Bereichs für nachrichtenklassenspezifische Inhaltseigenschaften.
    
    - Oder -
    
- Verwenden benannter Eigenschaften. 
    
Die erste Option ist vorzuziehen, da nicht alle Dienstanbieter benannte Eigenschaften unterstützen. MAPI definiert zwei separate Bereiche für Clients, die für neue nachrichtenklassenspezifische Inhaltseigenschaften verwendet werden können:
  
- 0x6800, 0x7BFF für durchlässige Eigenschaften zu verwenden
    
- 0x7C00, 0x7FFF für nichttransmittable Eigenschaften zu verwenden
    
Eigenschaftenbezeichner müssen in vordefinierte Bereiche fallen, um Kollisionen zwischen Eigenschaften zu verhindern, die von verschiedenen Anbietern oder Benutzern definiert werden. Benutzer von Eigenschaften in diesen Bereichen können jedoch keine Annahmen zum Verhalten der Eigenschaften treffen. Jeder Client, der eine neue Nachrichtenklasse erstellt, hat Zugriff auf diese Bereiche. Eine Eigenschaft mit dem Bezeichner  _xxxx_ kann ein Verhalten für eine Nachrichtenklasse und ein anderes Verhalten für eine andere Nachrichtenklasse bedeuten. 
  
Benannte Eigenschaften werden verwendet, um zu gewährleisten, dass eine bestimmte Eigenschaft für eine Nachrichtenklasse eindeutig ist. Benannte Eigenschaftenbezeichner beginnen im 0x8000 Bereich. Clients definieren einen oder mehrere Namen und rufen dann die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) des Nachrichtenspeichers auf, um jedem Namen einen Bezeichner zuzuordnen. Benannte Eigenschaften können von Clients oder Dienstanbietern verwendet werden, um neue Eigenschaften für jedes Objekt nur zu definieren, wenn der Besitzer des Objekts benannte Eigenschaften unterstützt. Benutzer dieser Eigenschaften rufen **GetIDsFromNames** und eine verwandte **IMAPIProp-Methode,** [GetNamesFromIDs](imapiprop-getnamesfromids.md), auf, um einen Namen und dessen Bezeichner zu zuordnungen.
  
Alle neuen oder vorhandenen Eigenschaften müssen den Satz vordefinierter Eigenschaftentypen verwenden. Neue Eigenschaftstypen können nicht hinzugefügt werden, und vorhandene Typen können nicht geändert oder gelöscht werden. Einfache, kleine Eigenschaften, z. B. einstellige oder 16-Bit-ganzzahlige Eigenschaften, können in jedem geeigneten Typ gespeichert werden. Beispielsweise können ganze Zahlen als **ULONG** gespeichert werden, und Zeichenfolgen können als **PT_STRING8.** 
  
Verwenden Sie den **PT_BINARY,** um ein gezähltes Bytearray anzugeben. Dieser Eigenschaftstyp ist nützlich, um die Datentypen zu erweitern, die in einem Objekt gespeichert werden können. Bytes werden in der Reihenfolge übertragen, und es werden keine Annahmen zur Bedeutung der Daten gemacht. Wenn eine Clientanwendung Daten aus einer solchen Eigenschaft liest, bleiben die Daten unverändert von der Art und Weise, wie sie gespeichert wurden. Der Client muss beim Verschieben von Daten über CPUs alle erforderlichen Byte-Swappings ausführen. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

