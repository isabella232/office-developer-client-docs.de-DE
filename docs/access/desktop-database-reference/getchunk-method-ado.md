---
title: GetChunk-Methode (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44cd0cb5632e64811de14f9abd3c78aac9203705
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292286"
---
# <a name="getchunk-method-ado"></a>GetChunk-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt den gesamten Inhalt oder einen Teil des Inhalts eines [Field](field-object-ado.md)-Objekts mit umfangreichem Text oder Binärdaten zurück.

## <a name="syntax"></a>Syntax

*Variablen* = *Feld*. GetChunk (*Größe* )

## <a name="return-value"></a>Rückgabewert

Gibt einen **Variant**-Wert zurück.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Size* |Ein **Long** -Ausdruck, der der Anzahl von Bytes oder Zeichen entspricht, die Sie abrufen möchten.|

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **GetChunk**-Methode für ein **Field**-Objekt, um einen Teil der bzw. die gesamten umfangreichen Binär- oder Zeichendaten abzurufen. In Situationen, bei denen der Systemspeicher beschränkt ist, können Sie die **GetChunk**-Methode verwenden, um umfangreiche Werte in kleinere Einheiten aufzuteilen, statt deren Gesamtheit beizubehalten.

Die beim Aufrufen von **GetChunk** zurückgegebenen Daten werden *Variable* zugewiesen. Ist *Size* größer als die restlichen Daten, gibt die **GetChunk**-Methode nur die restlichen Daten zurück, ohne *Variable* mit Leerzeichen aufzufüllen. Ist das Feld leer, gibt die **GetChunk**-Methode einen Nullwert zurück.

Bei jedem weiteren Aufruf von **GetChunk** werden die Daten ab der Stelle abgerufen, an der beim vorherigen Aufruf von **GetChunk** abgebrochen wurde. Wenn Sie jedoch Daten aus einem Feld abrufen und anschließend den Wert eines anderen Felds im aktuellen Datensatz festlegen oder lesen, geht ADO davon aus, dass Sie das Abrufen von Daten aus dem ersten Feld beendet haben. Wenn Sie die **GetChunk** -Methode erneut für das erste Feld aufrufen, interpretiert ADO den Aufruf als einen neuen **GetChunk** -Vorgang und beginnt am Anfang der Daten mit dem Lesen. Beim Zugriff auf Felder in anderen [Recordset](recordset-object-ado.md)-Objekten, bei denen es sich nicht um Klone des ersten **Recordset** -Objekts handelt, werden die **GetChunk** -Operationen nicht unterbrochen.

Besitzt das **adFldLong** -Bit in der [Attributes](attributes-property-ado.md)-Eigenschaft eines **Field** -Objekts den Wert **True**, können Sie die **GetChunk** -Methode für dieses Feld verwenden.

Ist kein aktueller Datensatz vorhanden, wenn Sie die **GetChunk** -Methode für ein **Field** -Objekt verwenden, tritt Fehler 3021 (kein aktueller Datensatz) auf.


> [!NOTE]
> [!HINWEIS] Die **GetChunk** -Methode kann nicht auf **Field** -Objekte eines [Record](record-object-ado.md)-Objekts angewendet werden. Sie führt keine Vorgänge aus und generiert einen Laufzeitfehler.


