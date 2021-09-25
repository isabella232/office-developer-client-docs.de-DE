---
title: ReadText-Methode (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a46a62505f3234dc552db1ed39d38383524cda9e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593803"
---
# <a name="readtext-method-ado"></a>ReadText-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Liest eine angegebene Anzahl von Zeichen aus einem [Stream](stream-object-ado.md)-Textobjekt.

## <a name="syntax"></a>Syntax

*Zeichenfolge*  =  *Stream*. ReadText (*NumChars*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*NumChars* |Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Zeichen oder einen [StreamReadEnum](streamreadenum.md)-Wert angibt. Der Standardwert lautet **adReadAll**.|

## <a name="return-value"></a>Rückgabewert

Die **ReadText**-Methode liest eine angegebene Anzahl von Zeichen, eine vollständige Zeile oder einen vollständigen Datenstrom aus einem **Stream**-Objekt und gibt die resultierende Zeichenfolge zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Wenn *NumChar* größer als die Anzahl der im Datenstrom verbleibenden Zeichen ist, werden nur die verbleibenden Zeichen zurückgegeben. Der Lesevorgang der Zeichenfolge ist nicht mit der durch *NumChar* angegebenen Länge aufgefüllt. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.

> [!NOTE]
> Die **ReadText**-Methode wird bei Textdatenströmen verwendet ([Type](type-property-ado-stream.md) ist auf **adTypeText** festgelegt). Verwenden Sie bei binären Datenströmen (**Type** ist auf **adTypeBinary** festgelegt) die [Read](read-method-ado.md)-Methode.

