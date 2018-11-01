---
title: AddNew-Methode (ADO)
TOCTitle: AddNew Method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 720445d488f70f3e6219db65192946d4056ddfe4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886053"
---
# <a name="addnew-method-ado"></a>AddNew-Methode (ADO)


**Betrifft**: Access 2013, Office 2013

Es wird ein neuer Datensatz für ein aktualisierbares [Recordset](recordset-object-ado.md)-Objekt erstellt.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. AddNew *FieldList*, *Werte*

## <a name="parameters"></a>Parameter

  - *recordset*

  - Ein **Recordset** -Objekt.

  - *Feldliste*

  - Optional. Ein einzelner Name oder ein Array aus Namen oder Positionen der Felder im neuen Datensatz.

  - *Values*

  - Optional. Ein einzelner Wert oder ein Array aus Werten für die Felder im neuen Datensatz. Wenn *Fieldlist* ein Array ist, muss *Werte* auch ein Array mit der gleichen Anzahl von Elementen sein; andernfalls, tritt ein Fehler auf. Die Reihenfolge der Feldnamen muss mit der Reihenfolge der Feldwerte in den einzelnen Arrays übereinstimmen.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **AddNew** -Methode zum Erstellen und Initialisieren eines neuen Datensatzes. Verwenden Sie die [Supports](supports-method-ado.md)-Methode mit **adAddNew** (ein [CursorOptionEnum](cursoroptionenum.md)-Wert), um zu überprüfen, ob Sie dem aktuellen **Recordset** -Objekt Datensätze hinzufügen können.

Nach dem Aufrufen der AddNew-Methode wird der neue Datensatz zum aktuellen Datensatz und bleibt aktuell, wenn Sie die Update-Methode aufrufen. Da der neue Datensatz dem Recordset-Objekt angefügt wird, wird durch einen Aufruf von MoveNext nach der Aktualisierung an das Ende des Recordset-Objekts gewechselt, sodass EOF True entspricht. Wenn vom Recordset-Objekt keine Lesezeichen unterstützt werden, können Sie möglicherweise nicht auf den neuen Datensatz zugreifen, wenn Sie zu einem anderen Datensatz wechseln. Abhängig vom Cursortyp müssen Sie möglicherweise die Requery-Methode aufrufen, um den Zugriff auf den neuen Datensatz zu ermöglichen.

Wenn Sie **AddNew** beim Bearbeiten des aktuellen Datensatzes oder beim Hinzufügen eines neuen Datensatzes aufrufen, wird von ADO die **Update** -Methode aufgerufen, um alle Änderungen zu speichern und dann den neuen Datensatz zu erstellen.

Das Verhalten der **AddNew** -Methode hängt vom Aktualisierungsmodus des **Recordset** -Objekts und gibt an, ob Sie die Argumente *Fieldlist* und *Values* übergeben.

Im *unmittelbaren Aktualisierungsmodus* (in dem Änderungen durch den Anbieter in die zugrunde liegende Datenquelle geschrieben werden, wenn Sie die **Update**-Methode aufrufen) wird durch Aufrufen der **AddNew**-Methode ohne Argumente die [EditMode](editmode-property-ado.md)-Eigenschaft auf **adEditAdd** festgelegt (ein [EditModeEnum](editmodeenum.md)-Wert). Alle Änderungen von Feldwerten werden vom Anbieter lokal zwischengespeichert. Durch Aufrufen der **Update**-Methode wird der neue Datensatz in der Datenbank bereitgestellt und die **EditMode**-Eigenschaft auf **adEditNone** festgelegt (ein **EditModeEnum**-Wert). Wenn Sie die Argumente *Fieldlist* und *Values*übergeben, wird der neue Datensatz von ADO sofort in der Datenbank bereitgestellt (ein Aufruf von **Update** ist nicht notwendig); der Wert der **EditMode**-Eigenschaft wird nicht geändert (**adEditNone**).

Im *Batchaktualisierungsmodus* (in dem der Anbieter mehrere Änderungen zwischenspeichert und schreibt sie in der zugrunde liegenden Datenquelle nur, wenn Sie die [UpdateBatch](updatebatch-method-ado.md) -Methode aufrufen), durch Aufrufen der **AddNew** -Methode ohne Argumente **EditMode** wird **AdEditAdd**-Eigenschaft. Alle Änderungen von Feldwerten werden vom Anbieter lokal zwischengespeichert. Aufrufen der **Update** -Methode fügt den neuen Datensatz zum aktuellen **Recordset-Objekt** und die **EditMode** -Eigenschaft auf **adEditNone festgelegt**, aber der Anbieter nicht die Änderungen an der zugrunde liegenden Datenbank gebucht wird erst nach dem Aufruf der **UpdateBatch **Methode. Wenn Sie die Argumente *Fieldlist* und *Values* übergeben, sendet ADO den neuen Datensatz an den Anbieter für die Speicherung in einem Cache. Sie müssen die **UpdateBatch** -Methode, um den neuen Datensatz in der zugrunde liegenden Datenbank buchen aufrufen.

