---
title: ReadText-Methode (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 883f74c06da83a46f9ffd1c30861d796c04b5c74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300798"
---
# <a name="readtext-method-ado"></a>ReadText-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Liest eine angegebene Anzahl von Zeichen aus einem [Stream](stream-object-ado.md)-Textobjekt.

## <a name="syntax"></a>Syntax

*String* = -*Stream*. ReadText (*NumChars*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*NumChars* |Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Zeichen oder einen [StreamReadEnum](streamreadenum.md)-Wert angibt. Der Standardwert lautet **adReadAll**.|

## <a name="return-value"></a>Rückgabewert

Die **ReadText**-Methode liest eine angegebene Anzahl von Zeichen, eine vollständige Zeile oder einen vollständigen Datenstrom aus einem **Stream**-Objekt und gibt die resultierende Zeichenfolge zurück.

## <a name="remarks"></a>Bemerkungen

Wenn *NumChar* größer als die Anzahl der Zeichen im Stream ist, werden nur die verbleibenden Zeichen zurückgegeben. Die Zeichenfolge Read wird nicht mit der durch *NumChar*angegebenen Länge aufgefüllt. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.

> [!NOTE]
> Die **ReadText**-Methode wird bei Textdatenströmen verwendet ([Type](type-property-ado-stream.md) ist auf **adTypeText** festgelegt). Verwenden Sie bei binären Datenströmen (**Type** ist auf **adTypeBinary** festgelegt) die [Read](read-method-ado.md)-Methode.

