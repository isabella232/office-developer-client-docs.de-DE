---
title: Festlegen einer Tabellen Position mit einem Filter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316044"
---
# <a name="setting-a-table-position-with-a-filter"></a>Festlegen einer Tabellen Position mit einem Filter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Tabellen Benutzer können den Cursor in eine Zeile verschieben, die mit einem Satz von Filterkriterien übereinstimmt. Filter können auf einer Vielzahl von Richtlinien basieren, wie beispielsweise Spalten Eigenschaftswerte, Bitmasken oder unter Objekte. Filter werden in MAPI mithilfe einer [SRestriction](srestriction.md) -Struktur angegeben. 
  
 **So positionieren Sie eine Tabelle auf der ersten Zeile, die den Kriterien entspricht, die in einer Einschränkung festgelegt sind**
  
- Rufen Sie die [IMAPITable:: FindRow](imapitable-findrow.md) -Methode auf. Beginnend mit der Zeile, die durch eine bestimmte Textmarke dargestellt wird, sucht **FindRow** entweder nach vorn oder rückwärts, um eine Zeile zu suchen, die den in der Einschränkung angegebenen Kriterien entspricht. **FindRow** kann für die Implementierung einer Bildlaufleiste, die auf Zeichen Zeichenfolgen basiert, anstelle von Bruchwerten hilfreich sein. Beispielsweise kann ein Client die MAPI-Implementierung von **FindRow** aufrufen, wenn er das integrierte Adressbuch durchsucht, um einen Benutzer durch Eingabe eines oder mehrerer Zeichen zu aktivieren, um den ersten Namen zu finden, der mit den angegebenen Zeichen beginnt. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

