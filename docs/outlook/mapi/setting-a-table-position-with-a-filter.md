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
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425470"
---
# <a name="setting-a-table-position-with-a-filter"></a>Festlegen einer Tabellenposition mit einem Filter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Tabellenbenutzer können den Cursor in eine Zeile verschieben, die einer Reihe von Filterkriterien entspricht. Filter können auf einer Vielzahl von Richtlinien basieren, z. B. Spalteneigenschaftswerte, Bitmasken oder Unterobjekte. Filter werden in MAPI mithilfe einer [SRestriction-Struktur](srestriction.md) angegeben. 
  
 **So positionieren Sie eine Tabelle in der ersten Zeile, die den in einer Einschränkung festgelegten Kriterien entspricht**
  
- Rufen Sie die [IMAPITable::FindRow-Methode](imapitable-findrow.md) auf. Beginnend mit der Zeile, die durch eine bestimmte Textmarke dargestellt wird, sucht **FindRow** vorwärts oder rückwärts nach einer Zeile, die den in der Einschränkung angegebenen Kriterien entspricht. **FindRow** kann nützlich sein, um eine Bildlaufleiste zu implementieren, die auf Zeichenzeichenfolgen anstelle von Bruchwerten basiert. Beispielsweise kann ein Client die MAPI-Implementierung von **FindRow** aufrufen, wenn er das integrierte Adressbuch durchsucht, um einem Benutzer durch Eingabe eines oder mehrere Zeichen zu ermöglichen, den Vornamen zu finden, der mit den angegebenen Zeichen beginnt. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

