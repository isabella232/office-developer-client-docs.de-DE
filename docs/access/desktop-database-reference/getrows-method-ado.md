---
title: GetRows-Methode (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b472f8e2cb7d95a3aa79194e7704a877864c1339
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920277"
---
# <a name="getrows-method-ado"></a>GetRows-Methode (ADO)


**Betrifft**: Access 2013, Office 2013


Ruft mehrere Datensätze eines [Recordset](recordset-object-ado.md)-Objekts in ein Array ab.

## <a name="syntax"></a>Syntax

*Array* = *Recordset-Objekt*. GetRows (*Zeilen*, *Starten*, *Felder* )

## <a name="return-value"></a>Rückgabewert

Gibt einen **Variant** -Wert zurück, deren dessen Wert es sich um ein zweidimensionales Array handelt.

## <a name="parameters"></a>Parameter

  - *Rows*

  - Optional. Ein [GetRowsOptionEnum](getrowsoptionenum.md)-Wert, der die Anzahl der abzurufenden Datensätze angibt. Der Standardwert lautet **adGetRowsRest**.

  - *Start*

  - Optional. Ein **String** -Wert oder ein **Variant** -Wert, der die Textmarke für den Datensatz ergibt, bei dem der **GetRows** -Vorgang beginnen soll. Sie können auch einen [BookmarkEnum](bookmarkenum.md)-Wert verwenden.

  - *Fields*

  - Optional. Ein **Variant** -Wert, der einen einzelnen Feldnamen oder eine einzelne Ordnungsposition oder ein Array mit Feldnamen oder Nummern für Ordnungspositionen darstellt. ADO gibt nur die Daten in diesen Feldern zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **GetRows** -Methode, um Datensätze aus einem **Recordset** -Objekt in ein zweidimensionales Array zu kopieren. Der erste Index identifiziert das Feld und der zweite die Nummer des Datensatzes. Die *Array* -Variable wird automatisch an die richtige Größe dimensioniert, wenn **GetRows** -Methode die Daten zurückgibt.

Wenn Sie einen Wert für das Argument *Zeilen* nicht angeben, übernimmt die **GetRows** -Methode alle Datensätze im **Recordset** -Objekt. Wenn Sie mehr Datensätze anfordern, als verfügbar sind, gibt **GetRows** nur die verfügbaren Datensätze zurück.

Wenn das **Recordset** -Objekt Lesezeichen unterstützt, können Sie angeben, an welcher Datensatz **GetRows** -Methode beginnen soll das Abrufen von Daten, indem Sie den Wert der [Bookmark](bookmark-property-ado.md) -Eigenschaft des Datensatzes in der *Start* -Argument übergeben.

Wenn Sie die Felder zu beschränken, die das Aufrufen von **GetRows zurückgegebenen** möchten, können Sie ein einzelnes Feld Namen und die Nummer oder ein Array mit Feldnamen/Nummern in das Argument *Fields* übergeben.

Nachdem Sie **GetRows** aufgerufen haben, wird der nächste ungelesene Datensatz zum aktuellen Datensatz, oder die [EOF](bof-eof-properties-ado.md)-Eigenschaft wird auf **True** festgelegt, wenn keine weiteren Datensätze verfügbar sind.

