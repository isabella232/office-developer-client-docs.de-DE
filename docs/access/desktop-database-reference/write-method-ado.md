---
title: Write-Methode - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5987b16c033b13be145e60317cdfdc821851be38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867412"
---
# <a name="write-method-ado"></a>Write-Methode (ADO)


**Betrifft**: Access 2013, Office 2013


Schreibt Binärdaten in ein [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. Schreiben des*Puffers*

## <a name="parameters"></a>Parameter

  - *Buffer*

  - Ein Wert vom Datentyp **Variant**, der ein Bytearray enthält, das geschrieben werden soll.

## <a name="remarks"></a>Hinweise

Die angegebenen Bytes werden ohne Leerzeichen zwischen den einzelnen Bytes in das **Stream** -Objekt geschrieben.

Als aktuelle [Position](position-property-ado.md) wird das Byte festgelegt, das auf die geschriebenen Daten folgt. Mit der **Write** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Bytes abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.

Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) für **Stream** um neue Bytes erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.


> [!NOTE]
> <P>Die <STRONG>Write</STRONG>-Methode wird für binäre Datenströme verwendet (<A href="type-property-ado-stream.md">Type</A> ist <STRONG>adTypeBinary</STRONG>). Für Textdatenströme (<STRONG>Type</STRONG> ist <STRONG>adTypeText</STRONG>) verwenden Sie <A href="writetext-method-ado.md">WriteText</A>.</P>


