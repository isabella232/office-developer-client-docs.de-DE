---
title: Index-Eigenschaft (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 28769059f6a7ab2ab6edd0723ad81d1fc156e43c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626386"
---
# <a name="index-property-ado"></a>Index-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen des Indexes an, der aktuell für das [Recordset](recordset-object-ado.md)-Objekt wirksam ist.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt den Indexnamen als **String**-Wert fest oder gibt den Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der durch die **Index**-Eigenschaft benannte Index muss zuvor für die Basistabelle deklariert worden sein, die dem **Recordset**-Objekt zugrunde liegt. Das heißt, der Index muss programmgesteuert entweder als ADOX-[Index](index-object-adox.md)-Objekt oder beim Erstellen der Basistabelle deklariert worden sein.

Wenn der Index nicht festgelegt werden kann, tritt ein Laufzeitfehler auf. Die **Index** -Eigenschaft kann in folgenden Fällen nicht festgelegt werden:

  - Innerhalb eines [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md)- oder eines **RecordsetChangeComplete** -Ereignishandlers.

  - Während das **Recordset**-Objekt noch eine Operation ausführt (was mithilfe der [State](state-property-ado.md)-Eigenschaft ermittelt werden kann).

  - Wenn mit der [Filter](filter-property-ado.md)-Eigenschaft ein Filter für das **Recordset**-Objekt festgelegt wurde.

Die **Index**-Eigenschaft kann immer fehlerfrei festgelegt werden, wenn das **Recordset**-Objekt geschlossen ist. Wenn der zugrunde liegende Anbieter jedoch keine Indizes unterstützt, wird das **Recordset**-Objekt nicht fehlerfrei geöffnet, oder der Index kann nicht verwendet werden.

Wenn der Index festgelegt werden kann, ändert sich möglicherweise die aktuelle Zeilenposition. Dadurch wird die [AbsolutePosition](absoluteposition-property-ado.md)-Eigenschaft aktualisiert und die Ereignisse **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md) und [MoveComplete](willmove-and-movecomplete-events-ado.md) werden generiert.

Wenn der Index festgelegt werden kann und die [LockType](locktype-property-ado.md)-Eigenschaft auf **AdLockPessimistic** oder **AdLockOptimistic** festgelegt ist, wird eine implizite [UpdateBatch](updatebatch-method-ado.md)-Operation ausgeführt. Dadurch werden die aktuellen und betroffenen Gruppen freigegeben. Alle vorhanden Filter werden freigegeben, und die aktuelle Zeilenposition wird zur ersten Zeile des neu angeordneten **Recordset** -Objekts.

Die **Index** -Eigenschaft wird zusammen mit der [Seek](seek-method-ado.md)-Methode verwendet. Wenn der zugrunde liegende Anbieter die **Index** -Eigenschaft und somit die **Seek** -Methode nicht unterstützt, können Sie stattdessen die [Find](find-method-ado.md)-Methode verwenden. Bestimmen Sie mit der [Supports](supports-method-ado.md)**(adIndex)-Methode,** ob das **Recordset-Objekt** Indizes unterstützt.

Die integrierte **Index**-Eigenschaft hängt nicht mit der dynamischen [Optimize](optimize-property-dynamic-ado.md)-Eigenschaft zusammen, obwohl sich beide auf Indizes beziehen.

