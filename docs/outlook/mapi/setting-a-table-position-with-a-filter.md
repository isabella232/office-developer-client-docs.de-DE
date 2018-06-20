---
title: Wenn Sie eine Tabelle Position mit einem Filter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4c3a5c13433fb2f037be24ddd4c877579429f7bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795515"
---
# <a name="setting-a-table-position-with-a-filter"></a>Wenn Sie eine Tabelle Position mit einem Filter

  
  
**Betrifft**: Outlook 
  
Tabelle Benutzer können den Cursor an eine Zeile setzen, die einen Satz von Filterkriterien entsprechen. Filter können verschiedene Richtlinien wie Spaltenwerte-Eigenschaft, Bitmasken oder Unterobjekte basieren. Filter werden in MAPI mithilfe der Struktur einer [SRestriction](srestriction.md) angegeben. 
  
 **Positionieren Sie auf die erste Zeile eine Tabelle, die in einer Einschränkung festgelegten Kriterien entspricht**
  
- Rufen Sie die [IMAPITable](imapitable-findrow.md) -Methode. Beginnend mit der Zeile, die durch eine bestimmte Textmarke dargestellt, sucht **FindRow** ein vorwärts oder rückwärts ausgeführt, eine Zeile zu finden, die die in der Einschränkung angegebenen Kriterien entspricht. **FindRow** ist hilfreich für die Implementierung von einer Bildlaufleiste angezeigt, die auf Zeichenfolgen anstelle von Bruchzahlen basiert. Beispielsweise kann ein Client des MAPI-Implementierung der **FindRow** aufrufen, bei der Suche über die integrierte-Adressbuch zum Aktivieren eines Benutzers, durch Eingabe von einem oder mehreren Zeichen, um den ersten Namen zu suchen, der mit der angegebenen Zeichen beginnt. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

