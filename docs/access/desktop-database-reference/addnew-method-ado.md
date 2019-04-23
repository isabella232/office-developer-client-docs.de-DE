---
title: AddNew-Methode (ADO)
TOCTitle: AddNew method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f733c574ba7927587c6fcb6305a361ca1070de0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282513"
---
# <a name="addnew-method-ado"></a>AddNew-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Es wird ein neuer Datensatz für ein aktualisierbares [Recordset](recordset-object-ado.md)-Objekt erstellt.

## <a name="syntax"></a>Syntax

*Recordset*. AddNew *FieldList*, *Werte*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*recordset* |Ein **Recordset** -Objekt.|
|*FieldList* |Optional. Ein einzelner Name oder ein Array aus Namen oder Positionen der Felder im neuen Datensatz.|
|*Values* |Optional. Ein einzelner Wert oder ein Array aus Werten für die Felder im neuen Datensatz. Wenn *Fieldlist* ein Array ist, muss *Values* ebenfalls ein Array mit der gleichen Anzahl an Mitgliedern sein, andernfalls tritt ein Fehler auf. Die Reihenfolge der Feldnamen muss mit der Reihenfolge der Feldwerte in den einzelnen Arrays übereinstimmen.|

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **AddNew** -Methode zum Erstellen und Initialisieren eines neuen Datensatzes. Verwenden Sie die [Supports](supports-method-ado.md)-Methode mit **adAddNew** (ein [CursorOptionEnum](cursoroptionenum.md)-Wert), um zu überprüfen, ob Sie dem aktuellen **Recordset** -Objekt Datensätze hinzufügen können.

After you call the **AddNew** method, the new record becomes the current record and remains current after you call the [Update](update-method-ado.md) method. Since the new record is appended to the **Recordset**, a call to **MoveNext** following the Update will move past the end of the **Recordset**, making **EOF** True. If the **Recordset** object does not support bookmarks, you may not be able to access the new record once you move to another record. Depending on your cursor type, you may need to call the [Requery](requery-method-ado.md) method to make the new record accessible.

Wenn Sie **AddNew** beim Bearbeiten des aktuellen Datensatzes oder beim Hinzufügen eines neuen Datensatzes aufrufen, wird von ADO die **Update**-Methode aufgerufen, um alle Änderungen zu speichern und dann den neuen Datensatz zu erstellen.

Das Verhalten der **AddNew**-Methode hängt vom Aktualisierungsmodus des **Recordset**-Objekts ab und davon, ob Sie die Argumente *Fieldlist* und *Values* übergeben.

Im *unmittelbaren Aktualisierungsmodus* (in dem Änderungen durch den Anbieter in die zugrunde liegende Datenquelle geschrieben werden, wenn Sie die **Update**-Methode aufrufen) wird durch Aufrufen der **AddNew**-Methode ohne Argumente die [EditMode](editmode-property-ado.md)-Eigenschaft auf **adEditAdd** festgelegt (ein [EditModeEnum](editmodeenum.md)-Wert). Alle Änderungen von Feldwerten werden vom Anbieter lokal zwischengespeichert. Durch Aufrufen der **Update**-Methode wird der neue Datensatz in der Datenbank bereitgestellt und die **EditMode**-Eigenschaft auf **adEditNone** festgelegt (ein **EditModeEnum**-Wert). Wenn Sie die Argumente *Fieldlist* und *Values*übergeben, wird der neue Datensatz von ADO sofort in der Datenbank bereitgestellt (ein Aufruf von **Update** ist nicht notwendig); der Wert der **EditMode**-Eigenschaft wird nicht geändert (**adEditNone**).

Im *Batchaktualisierungsmodus* (in dem mehrere Änderungen nur durch den Anbieter zwischengespeichert und in die zugrunde liegende Datenbank geschrieben werden, wenn Sie die [UpdateBatch](updatebatch-method-ado.md)-Methode aufrufen) wird durch Aufrufen der **AddNew**-Methode ohne Argumente die **EditMode**-Eigenschaft auf **adEditAdd** festgelegt. Alle Änderungen von Feldwerten werden vom Anbieter lokal zwischengespeichert. Durch Aufrufen der **Update**-Methode wird der neue Datensatz dem aktuellen **Recordset**-Objekt hinzugefügt, und die **EditMode**-Eigenschaft wird auf **adEditNone** festgelegt. Die Änderungen werden jedoch erst vom Anbieter in der zugrunde liegenden Datenbank bereitgestellt, wenn Sie die **UpdateBatch**-Methode aufrufen. Wenn Sie die Argumente *Fieldlist* und *Values* übergeben, wird der neue Datensatz von ADO zur Speicherung in einem Cache an den Anbieter gesendet. Sie müssen die **UpdateBatch**-Methode aufrufen, um den neuen Datensatz in der zugrunde liegenden Datenbank bereitzustellen.

