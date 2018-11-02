---
title: CancelUpdate-Methode (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d5414f6f604392d64baba7e67c8b66d13afc94d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922587"
---
# <a name="cancelupdate-method-ado"></a>CancelUpdate-Methode (ADO)


**Betrifft**: Access 2013, Office 2013

Alle an der aktuellen oder neuen Zeile eines [Recordset](recordset-object-ado.md)-Objekts oder der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts vorgenommenen Änderungen werden abgebrochen, bevor die [Update](update-method-ado.md)-Methode aufgerufen wird.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. CancelUpdate

*Datensatz*. *Felder*. CancelUpdate

## <a name="remarks"></a>Hinweise

**Recordset**

Verwenden Sie die **CancelUpdate** -Methode, um alle an der aktuellen Zeile vorgenommenen Änderungen abzubrechen oder eine neu hinzugefügte Zeile zu verwerfen. Sie können Änderungen an der aktuellen Zeile oder an einer neuen Zeile nach dem Aufrufen der **Update** -Methode nur abbrechen, wenn die Änderungen Teil einer Transaktion, für die Sie mit der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode ein Rollback ausführen können, oder Teil einer Batchaktualisierung sind. Im Fall einer Batchaktualisierung können Sie die **Update** -Methode mit den Methoden **CancelUpdate** oder [CancelBatch](cancelbatch-method-ado.md) abbrechen.

Wenn Sie eine neue Zeile hinzufügen, wenn Sie die **CancelUpdate** -Methode aufrufen, wird die Zeile, die vor dem [AddNew](addnew-method-ado.md)-Aufruf aktuell war, zur aktuellen Zeile.

Wenn Sie im Bearbeitungsmodus den aktuellen Datensatz verlassen möchten (z. B. mit [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) oder [Close](close-method-ado.md)), können Sie mit **CancelUpdate** alle ausstehenden Änderungen abbrechen. Möglicherweise müssen Sie dies tun, wenn die Aktualisierung nicht erfolgreich für die Datenquelle bereitgestellt werden kann (z. B. bleibt bei einem Löschversuch, der aufgrund von Verletzungen der referenziellen Integrität fehlschlägt, das **Recordset** nach einem Aufruf von [Delete](delete-method-ado-recordset.md) im Bearbeitungsmodus).

**Record**

Durch die **CancelUpdate** -Methode werden alle ausstehenden Einfügungen oder Löschungen von [Field](field-object-ado.md)-Objekten abgebrochen. Außerdem werden alle ausstehenden Aktualisierungen vorhandener Felder abgebrochen, und die Originalwerte der Felder werden wiederhergestellt. Die [Status](status-property-ado-recordset.md)-Eigenschaft aller Felder in der **Fields** -Auflistung wird auf **adFieldOK** festgelegt.

