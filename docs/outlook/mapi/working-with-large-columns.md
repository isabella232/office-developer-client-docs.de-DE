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
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325781"
---
# <a name="working-with-large-columns"></a>Arbeiten mit umfangreichen Spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Spalten mit String-oder Binary-Eigenschaftendaten können große, möglicherweise viele Tausende von Bytes lang sein. Da das Einschließen einer oder mehrerer Spalten mit Hunderten von Bytes in einer Ansicht oft nicht praktikabel ist, ermöglicht MAPI den Tabellen Implementierer das Abschneiden des Werts, meistens auf 255 Byte und weniger oft auf 510 Byte. Wenn möglich, sollten Tabellen Implementierer den vollständigen Wert einer Eigenschaft in eine Tabellenspalte aufnehmen. Die empfohlene Alternative besteht darin, nur die ersten 255 Bytes einzuschließen.
  
Clients können nicht vorab wissen, ob eine von Ihnen verwendete Tabelle umfangreiche Spalten abschneidet. Sie sollten davon ausgehen, dass eine Spalte eine abgeschnittene Eigenschaft darstellt, wenn die Länge der Spalte 255 oder 510 Byte beträgt. Bei Bedarf können Clients den vollständigen Wert einer abgeschnittenen Spalte direkt aus dem Objekt abrufen, indem Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Objekts aufrufen. 
  
Bei Clients, die Einschränkungen mit umfangreichen Eigenschaften erstellen, sollten Sie sich darüber im klaren sein, dass es der Tabellen Implementierung entspricht, wie diese Einschränkungen funktionieren. Einige Tabellen Implementierer lassen Einschränkungen, die mit einer abgeschnittenen Spalte erstellt werden, auf der abgeschnittenen Größe basieren, während andere Sie auf den gesamten Wert stützen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

