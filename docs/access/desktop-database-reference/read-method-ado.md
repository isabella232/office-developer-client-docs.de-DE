---
title: Read-Methode – ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2588df93b014d4e5ca85b0b545b0a18bfa751174
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593810"
---
# <a name="read-method-ado"></a>Read-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Liest eine angegebene Anzahl von Bytes aus einem binären [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Variant*  =  *Stream*. Read (*NumBytes* )

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Numbytes* |Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Bytes oder den [StreamReadEnum](streamreadenum.md)-Wert **adReadAll** angibt. Dies ist der Standardwert.|

## <a name="return-value"></a>Rückgabewert

Die **Read**-Methode liest eine angegebene Anzahl von Bytes oder den gesamten Datenstrom aus einem **Stream**-Objekt und gibt die resultierenden Daten als einen **Variant**-Wert zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Wenn *NumBytes* mehr als die Anzahl der verbleibenden Bytes im **Stream-Objekt** ist, werden nur die verbleibenden Bytes zurückgegeben. Die gelesenen Daten werden nicht mit der durch *NumBytes angegebenen* Länge abgeglichen. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.

> [!NOTE]
> Mit *NumBytes* wird immer die Anzahl an Bytes ermittelt. Verwenden Sie bei aus Text bestehenden **Stream**-Objekten ([Type](type-property-ado-stream.md) ist auf **adTypeText** festgelegt) die [ReadText](readtext-method-ado.md)-Methode.


