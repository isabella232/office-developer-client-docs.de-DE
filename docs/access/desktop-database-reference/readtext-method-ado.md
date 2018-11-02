---
title: ReadText-Methode (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 97ef84cbacc02da0a3150cf0efcb3a24e548f2d2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929314"
---
# <a name="readtext-method-ado"></a>ReadText-Methode (ADO)


**Betrifft**: Access 2013, Office 2013

Liest eine angegebene Anzahl von Zeichen aus einem [Stream](stream-object-ado.md)-Textobjekt.

## <a name="syntax"></a>Syntax

*Zeichenfolge* = *Stream-Objekt*. ReadText (*NumChars*)

## <a name="parameters"></a>Parameter

  - *NumChars*

  - Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Zeichen oder einen [StreamReadEnum](streamreadenum.md)-Wert angibt. Der Standardwert lautet **adReadAll**.

## <a name="return-value"></a>Rückgabewert

Die **ReadText** -Methode liest eine angegebene Anzahl von Zeichen, eine vollständige Zeile oder einen vollständigen Datenstrom aus einem **Stream** -Objekt und gibt die resultierende Zeichenfolge zurück.

## <a name="remarks"></a>Hinweise

Ist NumChar größer als die Anzahl der im Datenstrom verbliebenen Zeichen, werden nur die verbliebenen Zeichen zurückgegeben. Die gelesene Zeichenfolge wird nicht aufgefüllt, damit sie der durch NumChar angegebenen Länge entspricht. Wenn keine zu lesenden Zeichen vorhanden sind, wird ein Variant-Wert mit einem Nullwert zurückgegeben. ReadText kann nicht verwendet werden, um rückwärts zu lesen.


> [!NOTE]
> <P>Die <STRONG>ReadText</STRONG>-Methode wird bei Textdatenströmen verwendet (<A href="type-property-ado-stream.md">Type</A> ist auf <STRONG>adTypeText</STRONG> festgelegt). Verwenden Sie bei binären Datenströmen (<STRONG>Type</STRONG> ist auf <STRONG>adTypeBinary</STRONG> festgelegt) die <A href="read-method-ado.md">Read</A>-Methode.</P>


