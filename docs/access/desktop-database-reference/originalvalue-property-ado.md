---
title: OriginalValue-Eigenschaft (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 872e7c88e5ea4e79d6bff4aa590e72743feb3893
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884912"
---
# <a name="originalvalue-property-ado"></a>OriginalValue-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt den Wert eines [Felds](field-object-ado.md) im Datensatz an, bevor Änderungen vorgenommen wurden.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Variant** -Wert zurück, der den Wert eines Felds vor einer Änderung darstellt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **OriginalValue** -Eigenschaft, um den ursprünglichen Wert eines Felds aus dem aktuellen Datensatz zurückzugeben.

Im *sofortigen Aktualisierungsmodus* (in dem der Anbieter schreibt Änderungen in der zugrunde liegenden Datenquelle nach dem Aufruf der [Update](update-method-ado.md) -Methode), die **OriginalValue** -Eigenschaft gibt den Wert des Felds, das vor Änderungen vorhanden war (d. h., da die letzte Aufruf der **Update** -Methode). Dies ist der gleichen Wert, den die [CancelUpdate](cancelupdate-method-ado.md) -Methode verwendet, um die [Value](value-property-ado.md) -Eigenschaft ersetzen.

Im *Batchaktualisierungsmodus* (in dem der Anbieter mehrere Änderungen zwischenspeichert und schreibt sie in der zugrunde liegenden Datenquelle nur, wenn Sie die [UpdateBatch](updatebatch-method-ado.md) -Methode aufrufen), die **OriginalValue** -Eigenschaft gibt den Wert des Felds, das vorhanden, bevor Sie eine war ändert (d. h., seit die letzte **UpdateBatch** -Methode aufrufen). Dies ist der gleiche Wert, den die [CancelBatch](cancelbatch-method-ado.md) -Methode verwendet, um die **Value** -Eigenschaft ersetzen. Wenn Sie diese Eigenschaft mit der [UnderlyingValue](underlyingvalue-property-ado.md) -Eigenschaft verwenden, können Sie Konflikte lösen, die durch Batchaktualisierungen auftreten.

## <a name="record"></a>Record

Bei [Record](record-object-ado.md)-Objekten ist die **OriginalValue** -Eigenschaft für Felder leer, die vor dem Aufruf der [Update](update-method-ado.md)-Methode hinzugefügt wurden.

