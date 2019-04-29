---
title: Festlegen der Tabellen Position mit einem Bruchwert
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437336"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Festlegen der Tabellen Position mit einem Bruchwert

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Tabellen Benutzer können zu einer Position verschoben werden, die einen ungefähren Prozentsatz der Zeilen im Verhältnis zur Gesamtsumme darstellt. Anstatt zu einer exakten Zeile zu wechseln, wird die Tabelle durch diese Positionierungsmethode in Teile aufgeteilt, die auf Bruchteilen basieren. Tabellen Benutzer können beispielsweise in den halben Punkt einer Tabelle oder in die Zeile, die sich in der Tabelle von 7/8 befindet, verschieben. 
  
 **So verschieben Sie den Cursor um eine ungefähre Anzahl von Zeilen**
  
- Rufen Sie [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md)auf. **SeekRowApprox** wechselt zu der Zeile, die einen bestimmten Prozentsatz von Zeilen relativ zum Anfang der Tabelle darstellt. Dieser Prozentsatz wird in den Parametern _ulNumerator_ und _ulDenominator_ angegeben. **SeekRowApprox** wird häufig zum Implementieren von Bildlaufleisten verwendet. 
    
 **So bestimmen Sie die ungefähre Position einer Tabelle**
  
- Rufen Sie [IMAPITable:: QueryPosition](imapitable-queryposition.md)auf. **QueryPosition** kann verwendet werden, um den Benutzer über die aktuelle Position zu informieren. Es wird ein Bruchwert basierend auf der Anzahl der Zeilen in der Tabelle und der Nummer der aktuellen Zeile festgelegt. Erwarten Sie, dass dieser Wert eine Näherung darstellt. Tabellen Implementierer werden dazu angehalten, die genaue Position nicht zu berechnen, da genaue Implementierungen vor allem bei kategorisierten Tabellen kostspielig sein können. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

