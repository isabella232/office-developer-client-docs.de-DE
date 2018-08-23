---
title: Festlegen der Tabellenposition mit einem Bruchwert
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8ffed8070c219e6611aebbcb1dd5cd181b662850
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579697"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Festlegen der Tabellenposition mit einem Bruchwert

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Tabelle Benutzer können auf eine Position verschieben, die einen ungefähren Prozentsatz der Zeilen in Bezug auf die Summe darstellt. Statt auf eine genaue Zeile verschoben wurde, auf der Grundlage dieser Methode für die Positionierung teilt der Tabelle in Teile Brüche. Benutzer können beispielsweise auf halb, zeigen Sie eine Tabelle oder in die Zeile, die die Art und Weise, durch die Tabelle die 7/8 ist verschieben. 
  
 **So verschieben Sie den Cursor eine ungefähre Anzahl der Zeilen**
  
- Rufen Sie [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** verschiebt in die Zeile, die einen bestimmten Prozentsatz der Zeilen in Bezug auf den Anfang der Tabelle darstellt. Dieser Prozentsatz ist in den _UlNumerator_ und _UlDenominator_ -Parameter angegeben. **SeekRowApprox** wird häufig zum Implementieren von Bildlaufleisten verwendet. 
    
 **Um die ungefähre Position einer Tabelle bestimmen**
  
- Rufen Sie [IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** kann verwendet werden, um den Benutzer über die aktuelle Position zu informieren. Einen Bruch Wert basierend auf der Anzahl der Zeilen in der Tabelle und die Anzahl der aktuellen Zeile festgelegt. Davon ausgehen Sie, dass dieser Wert eine Annäherung darstellt. Tabelle Implementierer sollten sich nicht um die genaue Position zu berechnen, da präzise Implementierungen aufzurufen, insbesondere für kategorisierten Tabellen kostspielig sein können. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

