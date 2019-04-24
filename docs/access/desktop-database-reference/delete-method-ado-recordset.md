---
title: Delete-Methode (ADO-Recordset)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e8142d4fc4fc0036f80693f0bff779d9f3f2a62e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294099"
---
# <a name="delete-method-ado-recordset"></a>Delete-Methode (ADO-Recordset)

**Gilt für**: Access 2013, Office 2013

Löscht den aktuellen Datensatz oder eine Gruppe von Datensätzen.

## <a name="syntax"></a>Syntax

*Recordset*. *AffectRecords* löschen

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*AffectRecords* |Ein [AffectEnum](affectenum.md)-Wert, der bestimmt, wie viele Datensätze die **Delete** -Methode beeinflusst. Der Standardwert lautet **adAffectCurrent**.|

> [!NOTE]
> [!HINWEIS] **adAffectAll** und **adAffectAllChapters** sind keine gültigen Argumente für **Delete**.

## <a name="remarks"></a>Bemerkungen

Mithilfe der **Delete** -Methode kann der aktuelle Datensatz oder eine Gruppe von Datensätzen in einem [Recordset](recordset-object-ado.md)-Objekt zum Löschen markiert werden. Lässt das **Recordset** -Objekt das Löschen von Datensätzen nicht zu, tritt ein Fehler auf. Wenn Sie sich im Modus der unmittelbaren Aktualisierung befinden, werden die Löschvorgänge unmittelbar in der Datenbank angezeigt. Kann ein Datensatz nicht gelöscht werden (z. B. aufgrund von Verletzungen der Datenbankintegrität), verbleibt der Datensatz nach dem Aufrufen von **Update** im Bearbeitungsmodus. Folglich müssen Sie die Aktualisierung mithilfe von [CancelUpdate](cancelupdate-method-ado.md) abbrechen, bevor Sie den aktuellen Datensatz verlassen können (z. B. mithilfe von [Close](close-method-ado.md), [Move](move-method-ado.md) oder [NextRecordset](nextrecordset-method-ado.md)).

Wenn Sie sich im Batchaktualisierungsmodus befinden, werden die Datensätze zum Löschen aus dem Cache markiert, und der eigentliche Löschvorgang wird ausgeführt, sobald Sie die [UpdateBatch](updatebatch-method-ado.md)-Methode aufgerufen haben. (Verwenden Sie die [Filter](filter-property-ado.md)-Eigenschaft, um die gelöschten Datensätze anzuzeigen.)

Beim Abrufen von Feldwerten aus den gelöschten Datensätzen wird ein Fehler generiert. Nach dem Löschen des aktuellen Datensatzes bleibt der gelöschte Datensatz der aktuelle Datensatz, bis Sie zu einem anderen Datensatz wechseln. Sobald Sie einen gelöschten Datensatz verlassen, können Sie nicht mehr auf diesen Datensatz zugreifen.

Wenn Sie Löschvorgänge in eine Transaktion schachteln, können Sie gelöschte Datensätze mithilfe der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wiederherstellen. Wenn Sie sich im Batchaktualisierungsmodus befinden, können Sie mithilfe der [CancelBatch](cancelbatch-method-ado.md)-Methode einen ausstehenden Löschvorgang oder eine Gruppe von ausstehenden Löschvorgängen abbrechen.

Schlägt das Löschen eines Datensatzes aufgrund eines Konflikts mit den zugrunde liegenden Daten fehl (z. B. wenn ein Datensatz bereits von einem anderen Benutzer gelöscht wurde), gibt der Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurück, beendet aber nicht die Ausführung des Programms. Ein Laufzeitfehler tritt nur dann auf, wenn bei allen angeforderten Datensätzen Konflikte bestehen.

Ist die dynamische Eigenschaft [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) festgelegt und handelt es sich beim **Recordset** -Objekt um das Ergebnis der Ausführung eines JOIN-Vorgangs für mehrere Tabellen, löscht die **Delete** -Methode nur Zeilen aus der Tabelle, die in der [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)-Eigenschaft angegeben ist.

