---
title: Resync-Methode (ADO)
TOCTitle: Resync Method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fc91be8b78ed7362029849dfb22a78d758c886e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474450"
---
# <a name="resync-method-ado"></a>Resync-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013



Die Daten im aktuellen [Recordset](recordset-object-ado.md)-Objekt oder in der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts werden anhand der zugrunde liegenden Datenbank aktualisiert.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. Resync*AffectRecords*, *ResyncValues*

*Datensatz*. *Felder*. Resync*ResyncValues*

## <a name="parameters"></a>Parameter

  - *AffectRecords*

  - Optional. Ein [AffectEnum](affectenum.md)-Wert, durch den bestimmt wird, auf wie viele Datensätze sich die **Resync** -Methode auswirkt. Der Standardwert ist **adAffectAll**. Dieser Wert steht für die **Resync** -Methode der **Fields** -Auflistung eines **Record** -Objekts nicht zur Verfügung.

  - *ResyncValues*

  - Optional. Ein [ResyncEnum](resyncenum.md)-Wert, durch den angegeben wird, ob zugrunde liegende Werte überschrieben werden. Der Standardwert ist **adResyncAllValues**.

## <a name="remarks"></a>Hinweise

**Recordset**

Verwenden Sie die **Resync** -Methode zum erneuten Synchronisieren von Datensätzen im aktuellen **Recordset** mit der zugrunde liegenden Datenbank. Dies ist nützlich, wenn Sie einen statischen Cursor oder einen Vorwärtscursor verwenden, aber alle Änderungen in der zugrunde liegenden Datenbank sehen möchten.

Wenn Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festlegen, steht **Resync** nur für nicht schreibgeschützte **Recordset** -Objekte zur Verfügung.

Im Gegensatz zur [Requery](requery-method-ado.md)-Methode wird durch die **Resync** -Methode der zugrunde liegende Befehl des **Recordset** -Objekts nicht erneut ausgeführt. Neue Datensätze in der zugrunde liegenden Datenbank werden nicht angezeigt.

Wenn der Versuch der erneuten Synchronisierung aufgrund eines Konflikts mit den zugrunde liegenden Daten fehlschlägt (z. B. weil ein Datensatz von einem anderen Benutzer gelöscht wurde), werden vom Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurückgegeben, und es tritt ein Laufzeitfehler auf. Verwenden Sie die Eigenschaften [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) und [Status](status-property-ado-recordset.md), um Datensätze mit Konflikten zu suchen.

Wenn die dynamischen Eigenschaften [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) und [Resync Command](resync-command-property-dynamic-ado.md) festgelegt sind und das **Recordset** das Ergebnis der Ausführung einer JOIN-Operation für mehrere Tabellen ist, wird von der **Resync** -Methode der Befehl in der **Resync Command** -Eigenschaft nur für die in der **Unique Table** -Eigenschaft genannte Tabelle ausgeführt.

**Fields**

Verwenden Sie die **Resync** -Methode zum erneuten Synchronisieren der Werte der **Fields** -Auflistung eines **Record** -Objekts mit der zugrunde liegenden Datenquelle. Auf die [Count](count-property-ado.md)-Eigenschaft wirkt sich diese Methode nicht aus.

Wenn *ResyncValues* **AdResyncAllValues** (Standardwert) festgelegt ist, werden die [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md)und [OriginalValue](originalvalue-property-ado.md) -Eigenschaften des [Field](field-object-ado.md) -Objekte in der Auflistung synchronisiert. Wenn *ResyncValues* **AdResyncUnderlyingValues**festgelegt ist, wird nur die **UnderlyingValue** -Eigenschaft synchronisiert.

Der Wert der **Status** -Eigenschaft für die einzelnen **Field** -Objekte zum Zeitpunkt des Aufrufs wirkt sich auch auf das Verhalten von **Resync** aus. Auf **Field** -Objekte mit den **Status** -Werten **adFieldPendingUnknown** oder **adFieldPendingInsert** hat **Resync** keine Auswirkung. Für die **Status** -Werte **adFieldPendingChange** oder **adFieldPendingDelete** werden durch **Resync** die Datenwerte für in der Datenquelle noch vorhandene Felder synchronisiert.

Durch **Resync** werden **Status** -Werte von **Field** -Objekten nur geändert, wenn beim Aufrufen von **Resync** ein Fehler auftritt. Wenn z. B. das Feld nicht mehr vorhanden ist, wird vom Anbieter ein entsprechender **Status** -Wert für das **Field** -Objekt zurückgegeben, z. B. **adFieldDoesNotExist**. Zurückgegebene **Status** -Werte können innerhalb des Werts der **Status** -Eigenschaft logisch kombiniert werden.

