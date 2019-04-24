---
title: Read-Methode-ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307672"
---
# <a name="read-method-ado"></a>Read-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Liest eine angegebene Anzahl von Bytes aus einem binären [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Variant* = **-Wert. Lesen (*numBytes* )

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*NumBytes* |Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Bytes oder den [StreamReadEnum](streamreadenum.md)-Wert **adReadAll** angibt. Dies ist der Standardwert.|

## <a name="return-value"></a>Rückgabewert

Die **Read**-Methode liest eine angegebene Anzahl von Bytes oder den gesamten Datenstrom aus einem **Stream**-Objekt und gibt die resultierenden Daten als einen **Variant**-Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn *numBytes* größer ist als die Anzahl der Bytes, die im **Stream**übrig bleiben, werden nur die verbleibenden Bytes zurückgegeben. Die gelesenen Daten werden nicht mit der durch *numBytes*angegebenen Länge aufgefüllt. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.

> [!NOTE]
> Mit *NumBytes* wird immer die Anzahl an Bytes ermittelt. Verwenden Sie bei aus Text bestehenden **Stream**-Objekten ([Type](type-property-ado-stream.md) ist auf **adTypeText** festgelegt) die [ReadText](readtext-method-ado.md)-Methode.


