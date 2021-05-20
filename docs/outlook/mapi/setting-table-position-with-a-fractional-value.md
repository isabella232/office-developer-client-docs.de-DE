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
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437336"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Festlegen der Tabellenposition mit einem Bruchwert

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Tabellenbenutzer können zu einer Position wechseln, die einen ungefähren Prozentsatz von Zeilen im Verhältnis zur Gesamtsumme darstellt. Anstatt zu einer genauen Zeile zu verschieben, teilt diese Positionierungsmethode die Tabelle auf der Grundlage von Brüchen in Teile auf. Tabellenbenutzer können z. B. zu einem Tabellenhalbpunkt oder zu der Zeile wechseln, die 7/8 des Wegs durch die Tabelle ist. 
  
 **So verschieben Sie den Cursor um eine ungefähre Anzahl von Zeilen**
  
- Rufen [Sie IMAPITable::SeekRowApprox auf.](imapitable-seekrowapprox.md) **SeekRowApprox** wechselt zu der Zeile, die einen bestimmten Prozentsatz von Zeilen im Verhältnis zum Anfang der Tabelle darstellt. Dieser Prozentsatz wird in den  _Parametern ulNumerator_ und  _ulDenominator_ angegeben. **SeekRowApprox** wird häufig zum Implementieren von Bildlaufleisten verwendet. 
    
 **So bestimmen Sie die ungefähre Position einer Tabelle**
  
- Rufen [Sie IMAPITable::QueryPosition auf.](imapitable-queryposition.md) **QueryPosition** kann verwendet werden, um den Benutzer über die aktuelle Position zu informieren. Sie legt einen Bruchwert fest, der auf der Anzahl der Zeilen in der Tabelle und der Anzahl der aktuellen Zeile basiert. Gehen Sie davon aus, dass dieser Wert eine Näherung darstellt. Table implementers are encouraged not calculate the exact position because accurate implementations can be expensive to invoke, especially on kategord tables. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

