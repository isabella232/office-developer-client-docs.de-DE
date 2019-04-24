---
title: WRITETEXT-Methode (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92983163a909e72c3da142ebcf63b7e0723e96af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308267"
---
# <a name="writetext-method-ado"></a>WRITETEXT-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Schreibt eine angegebene Textzeichenfolge in ein [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Stream*. WRITETEXT-*Daten*, *Optionen*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Daten* |Ein Wert vom Datentyp **String**, der die Textzeichenfolge enthält, die geschrieben werden soll.|
|*Options* |Optional. Ein [StreamWriteEnum](streamwriteenum.md)-Wert, der angibt, ob am Ende der angegebenen Zeichenfolge ein Zeilentrennzeichen geschrieben werden muss.|

## <a name="remarks"></a>Bemerkungen

Die angegebenen Zeichenfolgen werden ohne Leerzeichen oder Buchstaben zwischen den einzelnen Zeichenfolgen in das **Stream**-Objekt geschrieben.

Als aktuelle [Position](position-property-ado.md) wird der Buchstabe festgelegt, der auf die geschriebenen Daten folgt. Mit der **WriteText** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Buchstaben abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.

Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) für **Stream** um neue Buchstaben erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.

> [!NOTE]
> Die **WriteText**-Methode wird für Textdatenströme verwendet ([Type](type-property-ado-stream.md) ist **adTypeText**). Für binäre Datenströme (**Type** ist **adTypeBinary**) verwenden Sie [Write](write-method-ado.md).


