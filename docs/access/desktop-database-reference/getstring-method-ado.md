---
title: GetString-Methode (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698211"
---
# <a name="getstring-method-ado"></a>GetString-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt das [Recordset](recordset-object-ado.md)-Objekt als eine Zeichenfolge zurück.

## <a name="syntax"></a>Syntax

*Variant* = *Recordset-Objekt*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)

## <a name="return-value"></a>Rückgabewert

Gibt das **Recordset** -Objekt als eine **Variant** -Variable (BSTR) mit Zeichenfolgenwerten zurück.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*StringFormat* |Ein [StringFormatEnum](stringformatenum.md)-Wert, der angibt, wie das **Recordset**-Objekt in eine Zeichenfolge konvertiert werden soll. Die Parameter *RowDelimiter*, *ColumnDelimiter* und *NullExpr* werden nur mit einem *StringFormat* mit dem Wert **adClipString** verwendet.|
|*NumRows* |Optional. Die Anzahl von im **Recordset** -Objekt zu konvertierenden Zeilen. Wenn *NumRows* nicht angegeben ist oder wenn es größer als die Gesamtzahl der Zeilen im **Recordset-Objekt**ist, werden alle Zeilen in das **Recordset-Objekt** konvertiert.|
|*ColumnDelimiter* |Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Tabulatorzeichen.|
|*RowDelimiter* |Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Wagenrücklaufzeichen.|
|*NullExpr* |Optional. Wenn angegeben, ein statt des Nullwerts verwendeter Ausdruck, andernfalls die leere Zeichenfolge.|

## <a name="remarks"></a>Hinweise

In der Zeichenfolge werden Zeilendaten aber keine Schemadaten gespeichert. Daher kann ein **Recordset** -Objekt nicht erneut mithilfe dieser Zeichenfolge geöffnet werden.

Diese Methode entspricht der **GetClipString** -Methode in RDO.

