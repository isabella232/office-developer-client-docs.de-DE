---
title: Festlegen einer Tabellenposition mit einem Filter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 677312ddc1f5a62d553ccbcb91f675ed31a1979d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586719"
---
# <a name="setting-a-table-position-with-a-filter"></a>Festlegen einer Tabellenposition mit einem Filter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Tabellenbenutzer können den Cursor in eine Zeile verschieben, die einer Reihe von Filterkriterien entspricht. Filter können auf einer Vielzahl von Richtlinien basieren, z. B. Spalteneigenschaftenwerte, Bitmasken oder Unterobjekte. Filter werden in der MAPI mithilfe einer [SRestriction-Struktur](srestriction.md) angegeben. 
  
 **So positionieren Sie eine Tabelle in der ersten Zeile, die den in einer Einschränkung festgelegten Kriterien entspricht**
  
- Rufen Sie die [IMAPITable::FindRow-Methode](imapitable-findrow.md) auf. Beginnend mit der Zeile, die durch eine bestimmte Textmarke dargestellt wird, sucht **FindRow** in Vorwärts- oder Rückwärtsrichtung nach einer Zeile, die den in der Einschränkung angegebenen Kriterien entspricht. **FindRow** kann nützlich sein, um eine Bildlaufleiste zu implementieren, die auf Zeichenzeichenfolgen anstelle von Bruchwerten basiert. Beispielsweise kann ein Client die MAPI-Implementierung von **FindRow** aufrufen, wenn er das integrierte Adressbuch durchsucht, damit ein Benutzer durch Eingeben eines oder mehrerer Zeichen den Vornamen suchen kann, der mit den angegebenen Zeichen beginnt. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

