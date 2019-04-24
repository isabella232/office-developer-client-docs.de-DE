---
title: CopyTo-Methode (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295478"
---
# <a name="copyto-method-ado"></a>CopyTo-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Kopiert die angegebene Anzahl von Zeichen oder Bytes (in Abhängigkeit vom [Type](type-property-ado-stream.md)) von einem [Stream](stream-object-ado.md)-Objekt in ein anderes **Stream**-Objekt.

## <a name="syntax"></a>Syntax

*Stream*. CopyTo *DestStream*, *NumChars*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DestStream* |Der Wert einer Objektvariable, der einen Verweis auf ein geöffnetes **Stream** -Objekt enthält. Das aktuelle **Stream**-Objekt wird in das durch *DestStream* angegebene **Stream**-Zielobjekt kopiert. Das **Stream**-Zielobjekt muss bereits geöffnet sein. Ist dies nicht der Fall, tritt ein Laufzeitfehler auf.<br/><br/>**Hinweis**: der *DestStream* -Parameter ist möglicherweise kein Proxy des **Stream** -Objekts, da dies den Zugriff auf eine private Schnittstelle für das **Stream** -Objekt erfordert, das nicht auf den Client übertragen werden kann.|
|*NumChars* |Optional. Ein **ganzzahliger** Wert, der die Anzahl von Bytes oder Zeichen angibt, die von der aktuellen Position im Quell **Daten** Strom in den **Zielstream**kopiert werden sollen. Der Standardwert ist – 1, der angibt, dass alle Zeichen oder Bytes von der aktuellen Position zu [EOS](eos-property-ado.md)kopiert werden.|

## <a name="remarks"></a>Bemerkungen

This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property. If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied. Wenn der Wert von *NumChars* ist – 1 oder nicht angegeben, werden alle Zeichen oder bytes, die von der aktuellen Position beginnen, kopiert.

Wenn der Zieldatenstrom bereits Zeichen oder Bytes enthält, bleibt der gesamte Inhalt nach dem Punkt, an dem die Kopie endet, erhalten und wird nicht abgeschnitten. **Position** beginnt bei dem Byte, dass unmittelbar auf das letzte kopierte Byte folgt. Wenn Sie diese Bytes abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.

**CopyTo** sollte verwendet werden, um Daten in ein **Stream**-Zielobjekt zu kopieren, das denselben Typ wie das **Stream**-Quellobjekt aufweist (ihre **Type**-Eigenschaften sind jeweils auf **adTypeText** oder auf **adTypeBinary** festgelegt). Bei **Stream**-Textobjekten können Sie die Einstellung der [Charset](charset-property-ado.md)-Eigenschaft für das **Stream**-Zielobjekt so ändern, dass ein Datensatz in einen anderen übertragen wird. **Stream**-Textobjekte können auch in binäre **Stream**-Objekte kopiert werden, aber binäre **Stream**-Objekte können nicht in **Stream**-Textobjekte kopiert werden.

