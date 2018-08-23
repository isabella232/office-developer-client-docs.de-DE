---
title: Festlegen einer Tabellenposition mit einem Filter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565592"
---
# <a name="setting-a-table-position-with-a-filter"></a>Festlegen einer Tabellenposition mit einem Filter

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Tabelle Benutzer können den Cursor an eine Zeile setzen, die einen Satz von Filterkriterien entsprechen. Filter können verschiedene Richtlinien wie Spaltenwerte-Eigenschaft, Bitmasken oder Unterobjekte basieren. Filter werden in MAPI mithilfe der Struktur einer [SRestriction](srestriction.md) angegeben. 
  
 **Positionieren Sie auf die erste Zeile eine Tabelle, die in einer Einschränkung festgelegten Kriterien entspricht**
  
- Rufen Sie die [IMAPITable](imapitable-findrow.md) -Methode. Beginnend mit der Zeile, die durch eine bestimmte Textmarke dargestellt, sucht **FindRow** ein vorwärts oder rückwärts ausgeführt, eine Zeile zu finden, die die in der Einschränkung angegebenen Kriterien entspricht. **FindRow** ist hilfreich für die Implementierung von einer Bildlaufleiste angezeigt, die auf Zeichenfolgen anstelle von Bruchzahlen basiert. Beispielsweise kann ein Client des MAPI-Implementierung der **FindRow** aufrufen, bei der Suche über die integrierte-Adressbuch zum Aktivieren eines Benutzers, durch Eingabe von einem oder mehreren Zeichen, um den ersten Namen zu suchen, der mit der angegebenen Zeichen beginnt. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

