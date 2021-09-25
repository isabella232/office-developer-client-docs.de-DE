---
title: WriteText-Methode (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b61687a933ff7a9b52ebd10958aa080aa383723b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593215"
---
# <a name="writetext-method-ado"></a>WriteText-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Schreibt eine angegebene Textzeichenfolge in ein [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Stream*. WriteText *Data*, *Options*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Daten* |Ein Wert vom Datentyp **String**, der die Textzeichenfolge enthält, die geschrieben werden soll.|
|*Options* |Optional. Ein [StreamWriteEnum](streamwriteenum.md)-Wert, der angibt, ob am Ende der angegebenen Zeichenfolge ein Zeilentrennzeichen geschrieben werden muss.|

## <a name="remarks"></a>HinwBemerkungeneise

Die angegebenen Zeichenfolgen werden ohne Leerzeichen oder Buchstaben zwischen den einzelnen Zeichenfolgen in das **Stream**-Objekt geschrieben.

Als aktuelle [Position](position-property-ado.md) wird der Buchstabe festgelegt, der auf die geschriebenen Daten folgt. Mit der **WriteText** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Buchstaben abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.

Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) für **Stream** um neue Buchstaben erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.

> [!NOTE]
> Die **WriteText**-Methode wird für Textdatenströme verwendet ([Type](type-property-ado-stream.md) ist **adTypeText**). Für binäre Datenströme (**Type** ist **adTypeBinary**) verwenden Sie [Write](write-method-ado.md).


