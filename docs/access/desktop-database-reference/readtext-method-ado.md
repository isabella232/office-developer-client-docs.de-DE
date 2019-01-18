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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699933"
---
# <a name="readtext-method-ado"></a>ReadText-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Liest eine angegebene Anzahl von Zeichen aus einem [Stream](stream-object-ado.md)-Textobjekt.

## <a name="syntax"></a>Syntax

*Zeichenfolge* = *Stream-Objekt*. ReadText (*NumChars*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*NumChars* |Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Zeichen oder einen [StreamReadEnum](streamreadenum.md)-Wert angibt. Der Standardwert lautet **adReadAll**.|

## <a name="return-value"></a>Rückgabewert

Die **ReadText** -Methode liest eine angegebene Anzahl von Zeichen, eine vollständige Zeile oder einen vollständigen Datenstrom aus einem **Stream** -Objekt und gibt die resultierende Zeichenfolge zurück.

## <a name="remarks"></a>Hinweise

Ist NumChar größer als die Anzahl der im Datenstrom verbliebenen Zeichen, werden nur die verbliebenen Zeichen zurückgegeben. Die gelesene Zeichenfolge wird nicht aufgefüllt, damit sie der durch NumChar angegebenen Länge entspricht. Wenn keine zu lesenden Zeichen vorhanden sind, wird ein Variant-Wert mit einem Nullwert zurückgegeben. ReadText kann nicht verwendet werden, um rückwärts zu lesen.

> [!NOTE]
> Die **ReadText**-Methode wird bei Textdatenströmen verwendet ([Type](type-property-ado-stream.md) ist auf **adTypeText** festgelegt). Verwenden Sie bei binären Datenströmen (**Type** ist auf **adTypeBinary** festgelegt) die [Read](read-method-ado.md)-Methode.

