---
title: Read-Methode - ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b47b557fcb3e3c9ed26af29ce910c95262e4fe13
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884947"
---
# <a name="read-method-ado"></a>Read-Methode (ADO)


**Betrifft**: Access 2013, Office 2013

Liest eine angegebene Anzahl von Bytes aus einem binären [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Variant* = *Stream-Objekt*. Lesen (*NumBytes* )

## <a name="parameters"></a>Parameter

  - *NumBytes*

  - Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Bytes oder den [StreamReadEnum](streamreadenum.md)-Wert **adReadAll** angibt. Dies ist der Standardwert.

## <a name="return-value"></a>Rückgabewert

Die **Read** -Methode liest eine angegebene Anzahl von Bytes oder den gesamten Datenstrom aus einem **Stream** -Objekt und gibt die resultierenden Daten als einen **Variant** -Wert zurück.

## <a name="remarks"></a>Hinweise

Ist NumBytes größer als die Anzahl der im Stream-Objekt verbliebenen Bytes, werden nur die verbliebenen Bytes zurückgegeben. Die gelesenen Daten werden nicht aufgefüllt, damit sie der durch NumBytes angegebenen Länge entsprechen. Wenn keine zu lesenden Bytes vorhanden sind, wird ein Variant-Wert mit einem Nullwert zurückgegeben. Mit Read kann nicht rückwärts gelesen werden.


> [!NOTE]
> <P>Mit <EM>NumBytes</EM> wird immer die Anzahl an Bytes ermittelt. Verwenden Sie bei aus Text bestehenden <STRONG>Stream</STRONG>-Objekten (<A href="type-property-ado-stream.md">Type</A> ist auf <STRONG>adTypeText</STRONG> festgelegt) die <A href="readtext-method-ado.md">ReadText</A>-Methode.</P>


