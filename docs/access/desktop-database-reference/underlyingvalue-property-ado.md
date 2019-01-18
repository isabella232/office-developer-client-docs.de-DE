---
title: UnderlyingValue-Eigenschaft (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6d1618a0cb310c1e564fe18289da6a2d35e91d0b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717293"
---
# <a name="underlyingvalue-property-ado"></a>UnderlyingValue-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013



Gibt den aktuellen Wert eines [Field](field-object-ado.md)-Objekts in der Datenbank an.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Variant** -Wert zurück, der den Wert eines **Field** -Objekts angibt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **UnderlyingValue** -Eigenschaft, um den aktuellen Feldwert aus der Datenbank zu ermitteln. Der Feldwert in der **UnderlyingValue** -Eigenschaft ist der Wert, der für Ihre Transaktion zu sehen ist. Er ist möglicherweise das Ergebnis einer kürzlichen Aktualisierung durch eine andere Transaktion. Dieser Wert kann sich von der [OriginalValue](originalvalue-property-ado.md)-Eigenschaft unterscheiden, die den ursprünglich an das [Recordset](recordset-object-ado.md)-Objekt zurückgegebenen Wert wiedergibt.

Dieses Verhalten ähnelt der [Resync](resync-method-ado.md)-Methode. Jedoch gibt die **UnderlyingValue** -Eigenschaft nur den Wert für ein bestimmtes Feld aus dem aktuellen Datensatz zurück. Dabei handelt es sich um denselben Wert, der bei der [Resync](resync-method-ado.md)-Methode zum Ersetzen der [Value](value-property-ado.md)-Eigenschaft verwendet wird.

Wenn Sie diese Eigenschaft in Verbindung mit der **UnderlyingValue** -Eigenschaft verwenden, können Sie Konflikte lösen, die durch Batchaktualisierungen auftreten.

## <a name="record"></a>Record

Bei [Record](record-object-ado.md)-Objekten ist diese Eigenschaft für Felder leer, die vor dem Aufruf der [Update](update-method-ado.md)-Methode hinzugefügt wurden.

