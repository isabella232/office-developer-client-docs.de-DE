---
title: GetString-Methode (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: efb5997e7b194d06d9facd5eeb1874d1d3286764
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618098"
---
# <a name="getstring-method-ado"></a>GetString-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt das [Recordset](recordset-object-ado.md)-Objekt als eine Zeichenfolge zurück.

## <a name="syntax"></a>Syntax

*Variant*  =  *Recordset*. GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)

## <a name="return-value"></a>Rückgabewert

Gibt das **Recordset**-Objekt als eine **Variant**-Variable (BSTR) mit Zeichenfolgenwerten zurück.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Stringformat* |Ein [StringFormatEnum](stringformatenum.md)-Wert, der angibt, wie das **Recordset**-Objekt in eine Zeichenfolge konvertiert werden soll. Die Parameter *RowDelimiter*, *ColumnDelimiter* und *NullExpr* werden nur mit einem *StringFormat* mit dem Wert **adClipString** verwendet.|
|*NumRows* |Optional. Die Anzahl von im **Recordset**-Objekt zu konvertierenden Zeilen. Ist *NumRows* nicht angegeben oder größer als die Gesamtanzahl der Zeilen im **Recordset**-Objekt, werden alle Zeilen im **Recordset**-Objekt konvertiert.|
|*ColumnDelimiter* |Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Tabulatorzeichen.|
|*RowDelimiter* |Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Wagenrücklaufzeichen.|
|*NullExpr* |Optional. Wenn angegeben, ein statt des Nullwerts verwendeter Ausdruck, andernfalls die leere Zeichenfolge.|

## <a name="remarks"></a>Bemerkungen

In der Zeichenfolge werden Zeilendaten aber keine Schemadaten gespeichert. Daher kann ein **Recordset**-Objekt nicht erneut mithilfe dieser Zeichenfolge geöffnet werden.

Diese Methode entspricht der **GetClipString** -Methode in RDO.

