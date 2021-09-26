---
title: UpdateBatch-Methode (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7ccb06a047fc7f1fcb304765350588f69e7f6808
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621654"
---
# <a name="updatebatch-method-ado"></a>UpdateBatch-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Schreibt alle ausstehenden Batchaktualisierungen auf einen Datenträger.

## <a name="syntax"></a>Syntax

*Recordset*. UpdateBatch *AffectRecords*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*AffectRecords* |Optional. Ein [AffectEnum](affectenum.md)-Wert, der angibt, wie viele Datensätze von der **UpdateBatch** -Methode betroffen sind.|

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **UpdateBatch**-Methode, wenn Sie ein **Recordset**-Objekt im Batchaktualisierungsmodus ändern, um alle in einem **Recordset**-Objekt vorgenommenen Änderungen an die zugrunde liegende Datenbank zu übertragen.

Wenn das **Recordset** -Objekt die Batchaktualisierung unterstützt, können Sie mehrere Änderungen an mindestens einem Datensatz bis zum Aufrufen der **UpdateBatch** -Methode lokal speichern. Falls Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie die **UpdateBatch** -Methode aufrufen, ruft ADO automatisch die [Update](update-method-ado.md)-Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden. Sie sollten die Batchaktualisierung nur mit einem Keysetcursor oder einem statischen Cursor verwenden.

> [!NOTE]
> [!HINWEIS] Wenn Sie **adAffectGroup** als Wert für diesen Parameter angeben, wird ein Fehler erzeugt, falls im aktuellen **Recordset** -Objekt keine Datensätze angezeigt werden (z. B. ein Filter, mit dem keine Datensätze übereinstimmen).

Wenn beim Übertragen von Änderungen ein Fehler bei einem Datensatz oder allen Datensätzen aufgrund eines Konflikts mit den zugrunde liegenden Daten auftritt (z. B. wurde ein Datensatz bereits von einem anderen Benutzer gelöscht), gibt der Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurück, und ein Laufzeitfehler wird gemeldet. Verwenden Sie die [Filter](filter-property-ado.md)-Eigenschaft (**adFilterAffectedRecords**) und die [Status](status-property-ado-recordset.md)-Eigenschaft, um nach Datensätzen mit Konflikten zu suchen.

Mit der [CancelBatch](cancelbatch-method-ado.md)-Methode brechen Sie alle ausstehenden Batchaktualisierungen ab.

Wenn die dynamischen Eigenschaften [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) und [Update Resync](update-resync-property-dynamic-ado.md) festgelegt sind und das **Recordset** -Objekt das Ergebnis der Ausführung einer JOIN-Operation mit mehreren Tabellen ist, folgt je nach den Einstellungen der **Update Resync** -Eigenschaft auf die Ausführung der [UpdateBatch](resync-method-ado.md) -Methode implizit die **Resync**-Methode.

Die Reihenfolge, in der die einzelnen Aktualisierungen eines Batches in der Datenquelle ausgeführt werden, stimmt nicht unbedingt mit der Reihenfolge überein, in der sie im lokalen **Recordset** -Objekt ausgeführt wurden. Die Aktualisierungsreihenfolge ist vom Anbieter abhängig. Berücksichtigen Sie dies beim Codieren von miteinander verknüpften Aktualisierungen, wie z. B. Fremdschlüsseleinschränkungen für eine Einfügung oder Aktualisierung.

