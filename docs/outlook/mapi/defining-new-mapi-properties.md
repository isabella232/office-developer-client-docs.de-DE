---
title: Definieren neuer MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b0f28efea6e7ba05dc399565ee866cf2e34572bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584633"
---
# <a name="defining-new-mapi-properties"></a>Definieren neuer MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Trotz der Vielzahl von Eigenschaften, die von der MAPI für die Verwendung durch Clients und Dienstanbieter bereitgestellt werden, ermöglicht MAPI bei Bedarf die Erstellung neuer Eigenschaften. Einige der gültigen Szenarien zum Definieren neuer öffentlicher Eigenschaften sind ein Client, der Eigenschaften zur Unterstützung einer neuen Nachrichtenklasse erstellt, und ein Dienstanbieter, der neue Eigenschaften erstellt, um eindeutige Messagingsystemfeatures verfügbar zu machen.
  
Es ist in der Regel nicht gültig, wenn ein Dienstanbieter neue Eigenschaften für ein vorhandenes MAPI-Objekt oder eine vorhandene Nachrichtenklasse definiert. Einer der Hauptvorteile der Verwendung der MAPI besteht darin, dass Standardbezeichner und -formate für eine große Anzahl von Messagingsystemelementen eingerichtet werden, sodass Benutzer Dienstanbieter nahtlos kombinieren und abgleichen können. Dienstanbieter, die nicht standardmäßige Eigenschaften verwenden, funktionieren nicht genauso gut mit anderen Dienstanbietern. 
  
Clients können Inhaltseigenschaften für neue Nachrichtenklassen erstellen, indem sie:
  
- Verwenden von Eigenschaftsbezeichnern innerhalb eines festgelegten Bereichs für nachrichtenklassenspezifische Inhaltseigenschaften.
    
    - Oder -
    
- Verwenden benannter Eigenschaften. 
    
Die erste Option ist vorzuziehen, da nicht alle Dienstanbieter benannte Eigenschaften unterstützen. MAPI definiert zwei separate Bereiche für Clients, die für neue nachrichtenklassenspezifische Inhaltseigenschaften verwendet werden:
  
- 0x6800 für datenübertragungsfähige Eigenschaften zu 0x7BFF
    
- 0x7C00 0x7FFF für nicht übermitbare Eigenschaften
    
Eigenschaftsbezeichner müssen in vordefinierte Bereiche fallen, um Konflikte zwischen Eigenschaften zu verhindern, die von verschiedenen Anbietern oder Benutzern definiert werden. Benutzer von Eigenschaften in diesen Bereichen können jedoch nicht vom Verhalten der Eigenschaften ausgehen. Jeder Client, der eine neue Nachrichtenklasse erstellt, hat Zugriff auf diese Bereiche. Eine Eigenschaft mit dem Bezeichner  _xxxx_ kann ein Verhalten für eine Nachrichtenklasse und ein anderes Verhalten für eine andere Nachrichtenklasse bedeuten. 
  
Benannte Eigenschaften werden verwendet, um sicherzustellen, dass eine bestimmte Eigenschaft für eine Nachrichtenklasse eindeutig ist. Benannte Eigenschaftsbezeichner beginnen im 0x8000 Bereich. Clients definieren einen oder mehrere Namen und rufen dann die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) des Nachrichtenspeichers auf, um jedem Namen einen Bezeichner zuzuordnen. Benannte Eigenschaften können von Clients oder Dienstanbietern nur verwendet werden, um neue Eigenschaften für jedes Objekt zu definieren, wenn der Besitzer des Objekts benannte Eigenschaften unterstützt. Benutzer dieser Eigenschaften rufen **GetIDsFromNames** und die zugehörige **IMAPIProp-Methode** [GetNamesFromIDs](imapiprop-getnamesfromids.md)auf, um einen Namen und dessen Bezeichner zuzuordnen.
  
Alle neuen oder vorhandenen Eigenschaften müssen den Satz vordefinierter Eigenschaftentypen verwenden. Neue Eigenschaftstypen können nicht hinzugefügt werden, und vorhandene Typen können nicht geändert oder gelöscht werden. Einfache, kleine Eigenschaften, z. B. Einzelzeichen- oder 16-Bit-Ganzzahleigenschaften, können in jedem geeigneten Typ gespeichert werden. So können z. B. ganze Zahlen als **ULONG** und Zeichenfolgen als **PT_STRING8** gespeichert werden. 
  
Verwenden  Sie den PT_BINARY Typ, um ein Bytearray mit Zählung anzugeben. Dieser Eigenschaftstyp ist nützlich, um die Datentypen zu erweitern, die in einem Objekt gespeichert werden können. Bytes werden nacheinander übertragen, und es werden keine Annahmen zur Bedeutung der Daten gemacht. Wenn eine Clientanwendung Daten aus einer solchen Eigenschaft liest, sind die Daten unverändert von der Art und Weise, wie sie gespeichert wurden. Der Client muss alle erforderlichen Byte-Tauschvorgänge ausführen, wenn Daten über CPUs verschoben werden. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

