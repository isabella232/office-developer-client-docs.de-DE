---
title: Arbeiten mit großen Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420423"
---
# <a name="working-with-large-columns"></a>Arbeiten mit großen Spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Spalten mit Zeichenfolgen- oder binären Eigenschaftsdaten können groß sein, möglicherweise viele Tausend Byte lang. Da das Hinzufügen einer oder mehreren Spalten mit Hunderten von Bytes in einer Ansicht häufig nicht praktikabel ist, ermöglicht MAPI Tabellen implementierern, den Wert zu kürzen, meist auf 255 Byte und seltener auf 510 Byte. Nach Möglichkeit sollten Tabellen implementierer den vollständigen Wert einer Eigenschaft in einer Tabellenspalte enthalten. Die empfohlene Alternative ist, nur die ersten 255 Byte zu enthalten.
  
Clients können nicht im Voraus wissen, ob eine tabelle, die sie verwenden, große Spalten abkürzt. Sie sollten davon ausgehen, dass eine Spalte eine abgeschnittene Eigenschaft darstellt, wenn die Länge der Spalte entweder 255 oder 510 Byte beträgt. Bei Bedarf können Clients den vollständigen Wert einer abgeschnittenen Spalte direkt aus dem Objekt abrufen, indem sie die [IMAPIProp::GetProps-Methode des](imapiprop-getprops.md) Objekts aufrufen. 
  
Clients, die Einschränkungen mit großen Eigenschaften erstellen, sollten beachten, dass es dem Tabellen implementier ob liegt, wie diese Einschränkungen funktionieren. Einige Tabellen implementierer ermöglichen, dass Einschränkungen, die mit einer abgeschnittenen Spalte erstellt werden, auf der abgeschnittenen Größe basieren, während andere sie auf dem gesamten Wert basieren. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

