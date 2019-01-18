---
title: Write-Methode - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702516"
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

