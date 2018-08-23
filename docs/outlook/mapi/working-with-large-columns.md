---
title: Arbeiten mit umfangreichen Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 11007fa18a57e296472c28f86480cb71b780e568
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593032"
---
# <a name="working-with-large-columns"></a>Arbeiten mit umfangreichen Spalten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Spalten mit Zeichenfolgen oder binäre Eigenschaftendaten können sehr groß sein, möglicherweise Tausende von Byte. Da eine oder mehrere Spalten mit Hunderten von Bytes in einer Ansicht einschließlich häufig nicht sinnvoll ist, kann MAPI Implementierer Tabelle, um den Wert, der am häufigsten auf 255 Byte und seltener 510 Byte abzuschneiden. Wenn möglich, sollte die Tabelle Implementierer den vollständigen Wert einer Eigenschaft in einer Tabellenspalte enthalten. Es wird empfohlen, stattdessen nur die ersten 255 Byte enthalten.
  
Clients können nicht im Voraus wissen, ob eine Tabelle verwendeten schneidet große Spalten ab. Sie sollten davon ausgehen, dass eine Spalte eine abgeschnittene Eigenschaft darstellt, wenn die Länge der Spalte 510 maximal 255 Bytes ist. Bei Bedarf können Clients direkt den vollständigen Wert einer abgeschnittene Spalte aus dem Objekt abrufen, indem das Objekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode aufrufen. 
  
Erstellen von Einschränkungen mit großen Eigenschaften Clients Beachten Sie, dass es bis zu der Tabelle Implementierer ist, wie diese Einschränkungen ausgeführt werden. Einige Implementierer Tabelle zulassen Einschränkungen, die erstellt werden, mit der abgeschnittene Spalte auf die abgeschnittene Größe basieren, während andere Benutzer auf den gesamten Wert basieren soll. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

