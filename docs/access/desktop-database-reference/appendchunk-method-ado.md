---
title: AppendChunk-Methode (ADO)
TOCTitle: AppendChunk method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7582a33ea1add92f2c9d678a671cc6129e0f68ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607262"
---
# <a name="appendchunk-method-ado"></a>AppendChunk-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Daten werden einem großen [Field](field-object-ado.md)-Text- oder -Binärdatenobjekt oder einem [Parameter](parameter-object-ado.md)-Objekt angefügt.

## <a name="syntax"></a>Syntax

*object.* *AppendChunk-Daten*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Objekt* |Ein **Field** - oder **Parameter** -Objekt.|
|*Daten* |Ein **Variant** -Objekt, das die dem Objekt anzufügenden Daten enthält.|

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **AppendChunk**-Methode für ein **Field**- oder **Parameter**-Objekt, um es mit Long binarydaten oder Zeichendaten zu füllen. In Situationen mit beschränktem Systemspeicher können Sie mithilfe der **AppendChunk**-Methode lange Werte in Teilen anstatt als Ganzes bearbeiten.

### <a name="field"></a>Feld

If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.

Beim ersten **AppendChunk** -Aufruf für ein **Field** -Objekt werden Daten in das Feld geschrieben. Dabei werden alle vorhandenen Daten überschrieben. Durch nachfolgende **AppendChunk** -Aufrufe werden Daten den vorhandenen Daten hinzugefügt. Wenn Sie Daten einem Feld anfügen und dann den Wert eines anderen Felds im aktuellen Datensatz festlegen oder lesen, wird von ADO angenommen, dass das Anfügen von Daten an das erste Feld beendet ist. Wenn Sie die **AppendChunk** -Methode erneut für das erste Feld aufrufen, wird der Aufruf von ADO als neue **AppendChunk** -Operation interpretiert, und die vorhandenen Daten werden überschrieben. Durch das Zugreifen auf Felder in anderen [Recordset](recordset-object-ado.md)-Objekten, die keine Klone des ersten **Recordset** -Objekts sind, werden **AppendChunk** -Operationen nicht unterbrochen.

Wenn beim Aufrufen von **AppendChunk** für ein **Field** -Objekt kein aktueller Datensatz vorhanden ist, tritt ein Fehler auf.

> [!NOTE]
> [!HINWEIS] Die **AppendChunk** -Methode eignet sich nicht für **Field** -Objekte eines [Record](record-object-ado.md)-Objekts. Es werden keine Operationen ausgeführt, und es wird ein Laufzeitfehler erzeugt.

### <a name="parameters"></a>Parameter

If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.

Durch den ersten **AppendChunk** -Aufruf für ein **Parameter** -Objekt werden Daten in den Parameter geschrieben, und alle vorhandenen Daten werden überschrieben. Durch nachfolgende **AppendChunk** -Aufrufe für ein **Parameter** -Objekt werden Daten den vorhandenen Parameterdaten hinzugefügt. Durch einen **AppendChunk** -Aufruf, bei dem ein Nullwert übergeben wird, werden alle Parameterdaten verworfen.

