---
title: CopyTo-Methode (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a17e74e1e3483b7ad2a70c5444503234cff5be12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920249"
---
# <a name="copyto-method-ado"></a>CopyTo-Methode (ADO)


**Betrifft**: Access 2013, Office 2013


Kopiert die angegebene Anzahl von Zeichen oder Bytes (in Abhängigkeit vom [Type](type-property-ado-stream.md)) von einem [Stream](stream-object-ado.md)-Objekt in ein anderes **Stream** -Objekt.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. CopyTo *DestStream*, *NumChars*

## <a name="parameters"></a>Parameter

  - *DestStream*

  - Der Wert einer Objektvariable, der einen Verweis auf ein geöffnetes **Stream**-Objekt enthält. Das aktuelle **Stream**-Objekt wird in das durch *DestStream* angegebene **Stream**-Zielobjekt kopiert. Das **Stream**-Zielobjekt muss bereits geöffnet sein. Ist dies nicht der Fall, tritt ein Laufzeitfehler auf.

   

    > [!NOTE]
    > Der *DestStream* -Parameter möglicherweise nicht, da dies erfordert Zugriff auf eine private Schnittstelle am **Stream** -Objekt, das an den Client nicht remotefähig einen Proxy des **Stream** -Objekts.

  - *NumChars*

  - Optional. Ein **Integer** -Wert, der angibt, die Anzahl von Bytes oder Zeichen von der aktuellen Position in der Quelle **Stream-Objekt** an das Ziel **Stream**kopiert werden sollen. Der Standardwert ist-1, gibt an, dass alle Zeichen oder Bytes in [EOS](eos-property-ado.md)von der aktuellen Position kopiert werden.

## <a name="remarks"></a>Hinweise

Diese Methode kopiert die angegebene Anzahl von Zeichen oder Bytes ab der durch die Position-Eigenschaft angegebenen aktuellen Position. Ist die angegebene Anzahl höher als die verfügbare Anzahl von Bytes bis zu EOS, werden nur die Zeichen oder Bytes ab der aktuellen Position bis zu EOS kopiert. Wenn der Wert für NumChars -1 oder nicht angegeben ist, werden alle Zeichen oder Bytes ab der aktuellen Position kopiert.

Wenn der Zieldatenstrom bereits Zeichen oder Bytes enthält, bleibt der gesamte Inhalt nach dem Punkt, an dem die Kopie endet, erhalten und wird nicht abgeschnitten. **Position** beginnt bei dem Byte, dass unmittelbar auf das letzte kopierte Byte folgt. Wenn Sie diese Bytes abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.

**CopyTo** sollte verwendet werden, um Daten in ein **Stream**-Zielobjekt zu kopieren, das denselben Typ wie das **Stream**-Quellobjekt aufweist (ihre **Type**-Eigenschaften sind jeweils auf **adTypeText** oder auf **adTypeBinary** festgelegt). Bei **Stream**-Textobjekten können Sie die Einstellung der [Charset](charset-property-ado.md)-Eigenschaft für das **Stream**-Zielobjekt so ändern, dass ein Datensatz in einen anderen übertragen wird. **Stream**-Textobjekte können auch in binäre **Stream**-Objekte kopiert werden, aber binäre **Stream**-Objekte können nicht in **Stream**-Textobjekte kopiert werden.

