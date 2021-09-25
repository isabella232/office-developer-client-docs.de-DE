---
title: Delete-Methode (ADO-Recordset)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 73dc83a240cb5e46b1b46e5d8bafbcd6ba1b8d56
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553137"
---
# <a name="delete-method-ado-recordset"></a>Delete-Methode (ADO-Recordset)

**Gilt für**: Access 2013, Office 2013

Löscht den aktuellen Datensatz oder eine Gruppe von Datensätzen.

## <a name="syntax"></a>Syntax

*Recordset*. Delete *AffectRecords*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*AffectRecords* |Ein [AffectEnum](affectenum.md)-Wert, der bestimmt, wie viele Datensätze die **Delete** -Methode beeinflusst. Der Standardwert lautet **adAffectCurrent**.|

> [!NOTE]
> [!HINWEIS] **adAffectAll** und **adAffectAllChapters** sind keine gültigen Argumente für **Delete**.

## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe der **Delete** -Methode kann der aktuelle Datensatz oder eine Gruppe von Datensätzen in einem [Recordset](recordset-object-ado.md)-Objekt zum Löschen markiert werden. Lässt das **Recordset** -Objekt das Löschen von Datensätzen nicht zu, tritt ein Fehler auf. Wenn Sie sich im Modus der unmittelbaren Aktualisierung befinden, werden die Löschvorgänge unmittelbar in der Datenbank angezeigt. Kann ein Datensatz nicht gelöscht werden (z. B. aufgrund von Verletzungen der Datenbankintegrität), verbleibt der Datensatz nach dem Aufrufen von **Update** im Bearbeitungsmodus. Folglich müssen Sie die Aktualisierung mithilfe von [CancelUpdate](cancelupdate-method-ado.md) abbrechen, bevor Sie den aktuellen Datensatz verlassen können (z. B. mithilfe von [Close](close-method-ado.md), [Move](move-method-ado.md) oder [NextRecordset](nextrecordset-method-ado.md)).

Wenn Sie sich im Batchaktualisierungsmodus befinden, werden die Datensätze zum Löschen aus dem Cache markiert, und der eigentliche Löschvorgang wird ausgeführt, sobald Sie die [UpdateBatch](updatebatch-method-ado.md)-Methode aufgerufen haben. (Verwenden Sie die [Filter](filter-property-ado.md)-Eigenschaft, um die gelöschten Datensätze anzuzeigen.)

Beim Abrufen von Feldwerten aus den gelöschten Datensätzen wird ein Fehler generiert. Nach dem Löschen des aktuellen Datensatzes bleibt der gelöschte Datensatz der aktuelle Datensatz, bis Sie zu einem anderen Datensatz wechseln. Sobald Sie einen gelöschten Datensatz verlassen, können Sie nicht mehr auf diesen Datensatz zugreifen.

Wenn Sie Löschvorgänge in eine Transaktion schachteln, können Sie gelöschte Datensätze mithilfe der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wiederherstellen. Wenn Sie sich im Batchaktualisierungsmodus befinden, können Sie mithilfe der [CancelBatch](cancelbatch-method-ado.md)-Methode einen ausstehenden Löschvorgang oder eine Gruppe von ausstehenden Löschvorgängen abbrechen.

Schlägt das Löschen eines Datensatzes aufgrund eines Konflikts mit den zugrunde liegenden Daten fehl (z. B. wenn ein Datensatz bereits von einem anderen Benutzer gelöscht wurde), gibt der Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurück, beendet aber nicht die Ausführung des Programms. Ein Laufzeitfehler tritt nur dann auf, wenn bei allen angeforderten Datensätzen Konflikte bestehen.

Ist die dynamische Eigenschaft [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) festgelegt und handelt es sich beim **Recordset** -Objekt um das Ergebnis der Ausführung eines JOIN-Vorgangs für mehrere Tabellen, löscht die **Delete** -Methode nur Zeilen aus der Tabelle, die in der [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)-Eigenschaft angegeben ist.

