---
title: Size-Eigenschaft (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a1bed3454d081b9d5de3a01e9b326130b40baa4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711609"
---
# <a name="size-property-ado"></a>Size-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt die maximale Größe eines [Parameter](parameter-object-ado.md)-Objekts in Bytes oder Zeichen an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert fest, der die maximale Größe eines Werts in einem **Parameter** -Objekt in Bytes oder Zeichen angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Bestimmen Sie mit der **Size** -Eigenschaft die maximale Größe von Werten, die in die [Value](value-property-ado.md)-Eigenschaft eines **Parameter** -Objekts geschrieben oder daraus gelesen werden.

Wenn Sie einen Datentyp variabler Länge für ein **Parameter**-Objekt angeben (beispielsweise einen beliebigen **String**-Typ wie z. B. **adVarChar**), müssen Sie die **Size**-Eigenschaft festlegen, bevor Sie sie der [Parameters](parameters-collection-ado.md)-Auflistung anfügen. Andernfalls tritt ein Fehler auf.

Wenn Sie das **Parameter** -Objekt bereits der **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts angefügt haben und seinen Typ in einen Datentyp variabler Länge ändern, müssen Sie die **Size** -Eigenschaft des **Parameter** -Objekts festlegen, bevor Sie das **Command** -Objekt ausführen. Andernfalls tritt ein Fehler auf.

Wenn Sie die [Refresh](refresh-method-ado.md)-Methode verwenden, um Parameterinformationen vom Anbieter zu erhalten, und ein oder mehrere **Parameter** -Objekte mit einem Datentyp variabler Länge zurückgegeben werden, reserviert ADO möglicherweise Speicher entsprechend der maximal möglichen Größe der Parameter. Das kann einen Fehler während der Ausführung verursachen. Damit kein Fehler auftritt, sollten Sie die **Size** -Eigenschaft für diese Parameter explizit festlegen, bevor Sie den Befehl ausführen.

Die **Size** -Eigenschaft ist nicht schreibgeschützt.

