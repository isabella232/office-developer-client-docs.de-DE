---
title: Arbeiten mit großen Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0f7bf7488404f9ffe8d39c1d6f2f0a430fa1a20d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609201"
---
# <a name="working-with-large-columns"></a>Arbeiten mit großen Spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Spalten mit Zeichenfolgen- oder binären Eigenschaftsdaten können groß sein, möglicherweise viele Tausend Byte lang. Da das Einschließen einer oder mehrerer Spalten mit Hunderten von Bytes in einer Ansicht häufig unpraktisch ist, ermöglicht MAPI Tabellen implementierern, den Wert zu kürzen, meistens auf 255 Bytes und seltener auf 510 Bytes. Wenn möglich, sollten Tabellen implementers den vollständigen Wert einer Eigenschaft in eine Tabellenspalte einschließen. Die empfohlene Alternative besteht darin, nur die ersten 255 Bytes einzuschließen.
  
Clients können nicht im Voraus wissen, ob eine tabelle, die sie verwenden, große Spalten abgeschnitten. Sie sollten davon ausgehen, dass eine Spalte eine abgeschnittene Eigenschaft darstellt, wenn die Länge der Spalte 255 oder 510 Byte beträgt. Bei Bedarf können Clients den vollständigen Wert einer abgeschnittenen Spalte direkt aus dem Objekt abrufen, indem sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Objekts aufrufen. 
  
Clients, die Einschränkungen mit umfangreichen Eigenschaften erstellen, sollten beachten, dass es dem Tabellen-Implementierer obliegt, wie diese Einschränkungen funktionieren. Einige Tabellen-Implementierer lassen zu, dass Einschränkungen, die mit einer abgeschnittenen Spalte erstellt werden, auf der abgeschnittenen Größe basieren, während andere auf dem gesamten Wert basieren. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

