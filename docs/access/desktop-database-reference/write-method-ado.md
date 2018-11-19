---
title: Write-Methode - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 227c7a3746d0c743c33f76362023d6d374269a81
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026281"
---
# <a name="write-method-ado"></a>Write-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Schreibt Binärdaten in ein [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. Schreiben des*Puffers*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Buffer* |Ein Wert vom Datentyp **Variant**, der ein Bytearray enthält, das geschrieben werden soll.|

## <a name="remarks"></a>Hinweise

Die angegebenen Bytes werden ohne Leerzeichen zwischen den einzelnen Bytes in das **Stream** -Objekt geschrieben.

Als aktuelle [Position](position-property-ado.md) wird das Byte festgelegt, das auf die geschriebenen Daten folgt. Mit der **Write** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Bytes abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.

Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) für **Stream** um neue Bytes erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.

> [!NOTE]
> Die **Write**-Methode wird für binäre Datenströme verwendet ([Type](type-property-ado-stream.md) ist **adTypeBinary**). Für Textdatenströme (**Type** ist **adTypeText**) verwenden Sie [WriteText](writetext-method-ado.md).

