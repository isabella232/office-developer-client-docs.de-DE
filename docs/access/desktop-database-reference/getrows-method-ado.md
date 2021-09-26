---
title: GetRows-Methode (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 51263fb407c67f4a027f67d8fd7741908de31d8a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626519"
---
# <a name="getrows-method-ado"></a>GetRows-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Ruft mehrere Datensätze eines [Recordset](recordset-object-ado.md)-Objekts in ein Array ab.

## <a name="syntax"></a>Syntax

*Array*  =  *Recordset*. GetRows(*Rows*, *Start*, *Fields* )

## <a name="return-value"></a>Rückgabewert

Gibt einen **Variant**-Wert zurück, deren dessen Wert es sich um ein zweidimensionales Array handelt.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Rows* |Optional. Ein [GetRowsOptionEnum](getrowsoptionenum.md)-Wert, der die Anzahl der abzurufenden Datensätze angibt. Der Standardwert lautet **adGetRowsRest**.|
|*Start* |Optional. Ein **String** -Wert oder ein **Variant** -Wert, der die Textmarke für den Datensatz ergibt, bei dem der **GetRows** -Vorgang beginnen soll. Sie können auch einen [BookmarkEnum](bookmarkenum.md)-Wert verwenden.|
|*Fields* |Optional. Ein **Variant** -Wert, der einen einzelnen Feldnamen oder eine einzelne Ordnungsposition oder ein Array mit Feldnamen oder Nummern für Ordnungspositionen darstellt. ADO gibt nur die Daten in diesen Feldern zurück.|

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **GetRows**-Methode, um Datensätze aus einem **Recordset**-Objekt in ein zweidimensionales Array zu kopieren. Der erste Index identifiziert das Feld und der zweite die Nummer des Datensatzes. Die *Array*-Variable wird automatisch an die richtige Größe angepasst, wenn die **GetRows**-Methode die Daten zurückgibt.

Wenn Sie für das Argument *Rows* keinen Wert angeben, ruft die **GetRows**-Methode automatisch alle Datensätze im **Recordset**-Objekt ab. Wenn Sie mehr Datensätze anfordern, als verfügbar sind, gibt **GetRows** nur die verfügbaren Datensätze zurück.

Wenn das **Recordset**-Objekt Textmarken unterstützt, können Sie festlegen, bei welchem Datensatz die **GetRows**-Methode mit dem Abrufen von Daten beginnen soll, indem Sie den Wert der [Bookmark](bookmark-property-ado.md)-Eigenschaft dieses Datensatzes in das Argument *Start* übergeben.

Wenn Sie die beim Aufrufen von **GetRows** zurückgegebenen Felder einschränken möchten, können Sie einen einzelnen Feldnamen/eine einzelne Nummer oder ein Array mit Feldnamen/Nummern in das Argument *Fields* übergeben.

Nachdem Sie **GetRows** aufgerufen haben, wird der nächste ungelesene Datensatz zum aktuellen Datensatz, oder die [EOF](bof-eof-properties-ado.md)-Eigenschaft wird auf **True** festgelegt, wenn keine weiteren Datensätze verfügbar sind.

