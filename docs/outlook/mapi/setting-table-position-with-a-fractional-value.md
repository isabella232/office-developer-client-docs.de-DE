---
title: Festlegen der Tabellenposition mit einem Bruchwert
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b22cefe52bf525f31041dcf87c94a0c32751c5a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550043"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Festlegen der Tabellenposition mit einem Bruchwert

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Tabellenbenutzer können zu einer Position wechseln, die einen ungefähren Prozentsatz von Zeilen im Verhältnis zur Summe darstellt. Anstatt zu einer genauen Zeile zu wechseln, teilt diese Methode der Positionierung die Tabelle in Teile auf der Grundlage von Bruchzahlen. Tabellenbenutzer können z. B. zum Halbwegpunkt einer Tabelle oder zu der Zeile wechseln, die 7/8 der Tabelle durchlaufen hat. 
  
 **So verschieben Sie den Cursor eine ungefähre Anzahl von Zeilen**
  
- Rufen Sie [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)auf. **SeekRowApprox** wechselt zu der Zeile, die einen bestimmten Prozentsatz von Zeilen im Verhältnis zum Anfang der Tabelle darstellt. Dieser Prozentsatz wird in den  _Parametern ulNumerator_ und  _ulDenominator_ angegeben. **SeekRowApprox** wird häufig zum Implementieren von Bildlaufleisten verwendet. 
    
 **So bestimmen Sie die ungefähre Position einer Tabelle**
  
- Aufrufen [von IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** kann verwendet werden, um den Benutzer über die aktuelle Position zu informieren. Sie legt einen Bruchwert basierend auf der Anzahl der Zeilen in der Tabelle und der Anzahl der aktuellen Zeile fest. Erwarten Sie, dass dieser Wert eine Näherung darstellt. Tabellenimplementierer werden empfohlen, die genaue Position nicht zu berechnen, da genaue Implementierungen teuer aufgerufen werden können, insbesondere bei kategorisierten Tabellen. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

