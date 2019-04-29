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
  
Trotz der Fülle an Eigenschaften, die von MAPI zur Verwendung durch Clients und Dienstanbieter bereitgestellt wurden, ermöglicht MAPI, dass bei Bedarf neue Eigenschaften erstellt werden. Einige der gültigen Szenarien für die Definition neuer öffentlicher Eigenschaften sind ein Client, der Eigenschaften erstellt, um eine neue Nachrichtenklasse zu unterstützen, und einen Dienstanbieter, der neue Eigenschaften erstellt, um eindeutige Messagingsystem Features offenzulegen.
  
Es ist in der Regel nicht gültig, dass ein Dienstanbieter neue Eigenschaften für ein vorhandenes MAPI-Objekt oder eine Nachrichtenklasse definiert. Einer der Hauptvorteile der Verwendung von MAPI besteht darin, dass Standardbezeichner und-Formate für eine Vielzahl von Messagingsystem Elementen eingerichtet sind, die es Benutzern ermöglichen, Dienstanbieter nahtlos zu kombinieren. Dienstanbieter, die nicht standardmäßige Eigenschaften verwenden, funktionieren nicht so gut mit anderen Dienstanbietern. 
  
Clients können Inhaltseigenschaften für neue Nachrichtenklassen erstellen, indem Sie:
  
- Verwenden von Eigenschafts Bezeichnern in einem bestimmten Bereich für Nachrichtenklassen spezifische Inhaltseigenschaften.
    
    - Oder
    
- Verwenden benannter Eigenschaften. 
    
Die erste Option ist vorzuziehen, da nicht alle Dienstanbieter benannte Eigenschaften unterstützen. MAPI definiert zwei separate Bereiche für Clients, die für neue Nachrichtenklassen spezifische Inhaltseigenschaften verwendet werden sollen:
  
- 0x6800 zu 0x7BFF für transmitable-Eigenschaften
    
- 0x7C00 zu 0x7FFF für nicht übertragbare Eigenschaften
    
Eigenschaftsbezeichner müssen in vordefinierte Bereiche fallen, um Kollisionen zwischen Eigenschaften zu vermeiden, die von verschiedenen Anbietern oder Benutzern definiert werden. Benutzer von Eigenschaften in diesen Bereichen können jedoch keine Annahmen hinsichtlich des Verhaltens der Eigenschaften treffen. Jeder Client, der eine neue Nachrichtenklasse erstellt, hat Zugriff auf diese Bereiche; eine Eigenschaft mit dem Bezeichner _xxxx_ kann ein Verhalten für eine Nachrichtenklasse und ein anderes Verhalten für eine andere Nachrichtenklasse bedeuten. 
  
Benannte Eigenschaften werden verwendet, um sicherzustellen, dass eine bestimmte Eigenschaft für eine Nachrichtenklasse eindeutig ist. Benannte Eigenschaftsbezeichner beginnen im 0X8000-Range. Clients definieren einen oder mehrere Namen und rufen dann die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode des Nachrichtenspeichers auf, um jedem Namen einen Bezeichner zuzuordnen. Benannte Eigenschaften können von Clients oder Dienstanbietern nur dann zum Definieren neuer Eigenschaften für ein Objekt verwendet werden, wenn der Besitzer des Objekts benannte Eigenschaften unterstützt. Benutzer dieser Eigenschaften rufen **GetIDsFromNames** und eine zugehörige **IMAPIProp** -Methode [GetNamesFromIDs](imapiprop-getnamesfromids.md)auf, um zwischen einem Namen und seinem Bezeichner zu ordnen.
  
Bei allen Eigenschaften, New oder existing, muss der Satz vordefinierter Eigenschaftentypen verwendet werden. Neue Eigenschaftentypen können nicht hinzugefügt werden, und vorhandene Typen können nicht geändert oder gelöscht werden. Einfache, kleine Eigenschaften wie Einzel-oder 16-Bit-Ganzzahl-Eigenschaften können in jedem geeigneten Typ gespeichert werden. Beispielsweise können ganze Zahlen als **ulong** gespeichert werden, und Zeichenfolgen können als **PT_String8**gespeichert werden. 
  
Verwenden Sie den **PT_BINARY** -Typ, um ein Gezähltes Bytearray anzugeben. Dieser Eigenschafts eignet sich zum Erweitern der Datentypen, die in einem Objekt gespeichert werden können. Bytes werden in der Reihenfolge übertragen, und es werden keine Annahmen hinsichtlich der Bedeutung der Daten vorgenommen. Wenn eine Clientanwendung Daten aus einer solchen Eigenschaft liest, werden die Daten unverändert, wie Sie gespeichert wurden. Der Client muss alle erforderlichen Byte Tauschvorgänge ausführen, wenn Daten über CPUs hinweg übertragen werden. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

