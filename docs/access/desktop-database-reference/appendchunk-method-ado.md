---
title: AppendChunk-Methode (ADO)
TOCTitle: AppendChunk Method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a565430cf81eed5cbc1ebfe135ce80ee6f0177e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475542"
---
# <a name="appendchunk-method-ado"></a>AppendChunk-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013


Daten werden einem großen [Field](field-object-ado.md)-Text- oder -Binärdatenobjekt oder einem [Parameter](parameter-object-ado.md)-Objekt angefügt.

## <a name="syntax"></a>Syntax

*-Objekt.* Methoden "AppendChunk" *Daten*

## <a name="parameters"></a>Parameter

  - *Objekt*

  - Ein **Field** - oder **Parameter** -Objekt.

  - *Daten*

  - Ein **Variant** -Objekt, das die dem Objekt anzufügenden Daten enthält.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **AppendChunk** -Methode für ein **Field** - oder **Parameter** -Objekt, um es mit Long binarydaten oder Zeichendaten zu füllen. In Situationen mit beschränktem Systemspeicher können Sie mithilfe der **AppendChunk** -Methode lange Werte in Teilen anstatt als Ganzes bearbeiten.

**Field**

Wenn das **AdFldLong** -Bit in der [Attributes](attributes-property-ado.md) -Eigenschaft eines **Field** -Objekts festgelegt ist, auf "true" können Sie die **AppendChunk** -Methode für dieses Feld verwenden.

Beim ersten **AppendChunk** -Aufruf für ein **Field** -Objekt werden Daten in das Feld geschrieben. Dabei werden alle vorhandenen Daten überschrieben. Durch nachfolgende **AppendChunk** -Aufrufe werden Daten den vorhandenen Daten hinzugefügt. Wenn Sie Daten einem Feld anfügen und dann den Wert eines anderen Felds im aktuellen Datensatz festlegen oder lesen, wird von ADO angenommen, dass das Anfügen von Daten an das erste Feld beendet ist. Wenn Sie die **AppendChunk** -Methode erneut für das erste Feld aufrufen, wird der Aufruf von ADO als neue **AppendChunk** -Operation interpretiert, und die vorhandenen Daten werden überschrieben. Durch das Zugreifen auf Felder in anderen [Recordset](recordset-object-ado.md)-Objekten, die keine Klone des ersten **Recordset** -Objekts sind, werden **AppendChunk** -Operationen nicht unterbrochen.

Wenn beim Aufrufen von **AppendChunk** für ein **Field** -Objekt kein aktueller Datensatz vorhanden ist, tritt ein Fehler auf.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>AppendChunk</STRONG> -Methode eignet sich nicht für <STRONG>Field</STRONG> -Objekte eines <A href="record-object-ado.md">Record</A>-Objekts. Es werden keine Operationen ausgeführt, und es wird ein Laufzeitfehler erzeugt.</P>



**Parameter**

Wenn das adParamLong-Bit in der Attributes-Eigenschaft eines Parameter-Objekts auf True festgelegt ist, können Sie für dieses Feld die AppendChunk-Methode verwenden.

Durch den ersten **AppendChunk** -Aufruf für ein **Parameter** -Objekt werden Daten in den Parameter geschrieben, und alle vorhandenen Daten werden überschrieben. Durch nachfolgende **AppendChunk** -Aufrufe für ein **Parameter** -Objekt werden Daten den vorhandenen Parameterdaten hinzugefügt. Durch einen **AppendChunk** -Aufruf, bei dem ein Nullwert übergeben wird, werden alle Parameterdaten verworfen.

