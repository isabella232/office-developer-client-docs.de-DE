---
title: Update-Methode (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c0ad6ce433a6c4a087f0892264549f123ab81b2b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562111"
---
# <a name="update-method-ado"></a>Update-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Speichert alle Änderungen, die Sie an der aktuellen Zeile eines [Recordset](recordset-object-ado.md)-Objekts oder der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts vornehmen.

## <a name="syntax"></a>Syntax

*Recordset*. Aktualisieren *von Feldern*, *Werten*

*record*. *Felder*. Aktualisieren

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Fields* |Optional. Ein Wert vom Datentyp **Variant**, der einen einzelnen Namen darstellt, oder ein Array vom Datentyp **Variant**, das Namen oder Positionen des Felds oder der Felder darstellt, das bzw. die Sie ändern möchten.|
|*Values* |Optional. Ein Wert vom Datentyp **Variant**, der einen einzelnen Wert darstellt, oder ein Array vom Datentyp **Variant**, das Werte für das Feld oder die Felder im neuen Datensatz darstellt.|

## <a name="remarks"></a>HinwBemerkungeneise

### <a name="recordset"></a>Recordset

Verwenden Sie die **Update**-Methode, um Änderungen am aktuellen Datensatz eines **Recordset**-Objekts seit dem Aufrufen der [AddNew](addnew-method-ado.md)-Methode oder seit dem Ändern von Feldwerten in einem vorhandenen Datensatz zu speichern. Das **Recordset**-Objekt muss Aktualisierungen unterstützen.

Führen Sie eine der folgenden Aktionen aus, um Feldwerte festzulegen:

- Weisen Sie der [Value](value-property-ado.md)-Eigenschaft eines [Field](field-object-ado.md)-Objekts Werte zu, und rufen Sie die **Update**-Methode auf.

- Übergeben Sie mithilfe des **Update**-Aufrufs einen Feldnamen und einen Wert als Argumente.

- Übergeben Sie mithilfe des **Update**-Aufrufs ein Array von Feldnamen und ein Array von Werten.

Wenn Sie Arrays von Feldern und Werten verwenden, müssen in beiden Arrays gleich viele Elemente vorhanden sein. Die Reihenfolge der Feldnamen muss außerdem der Reihenfolge der Feldwerte entsprechen. Wenn die Anzahl und die Reihenfolge von Feldern und Werten nicht übereinstimmen, tritt ein Fehler auf.

Wenn das **Recordset** -Objekt die Batchaktualisierung unterstützt, können Sie mehrere Änderungen an mindestens einem Datensatz bis zum Aufrufen der [UpdateBatch](updatebatch-method-ado.md)-Methode lokal speichern. Falls Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie die **UpdateBatch** -Methode aufrufen, ruft ADO automatisch die **Update** -Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden.

Wenn Sie den Datensatz verlassen, den Sie hinzufügen oder bearbeiten, bevor Sie die **Update** -Methode aufrufen, ruft ADO zum Speichern der Änderungen automatisch **Update** auf. Sie müssen die [CancelUpdate](cancelupdate-method-ado.md)-Methode aufrufen, falls Sie Änderungen am aktuellen Datensatz abbrechen oder einen neu hinzugefügten Datensatz verwerfen möchten.

Der aktuelle Datensatz bleibt aktuell, nachdem Sie die **Update** -Methode aufgerufen haben.

### <a name="record"></a>Aufzeichnen

Mit der **Update**-Methode werden Lösch- und Aktualisierungsvorgänge für Felder in der [Fields](fields-collection-ado.md)-Auflistung eines **Record**-Objekts abgeschlossen.

Beispielsweise werden mit der **Delete**-Methode gelöschte Felder sofort zum Löschen gekennzeichnet, verbleiben aber in der Auflistung. Die **Update**-Methode muss aufgerufen werden, damit diese Felder tatsächlich in der Auflistung des Anbieters gelöscht werden.

