---
title: CommandTimeout-Eigenschaft (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: b4edc56b5d0a11158e36bfc3797c9e6dea3a0bfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565800"
---
# <a name="commandtimeout-property-ado"></a>CommandTimeout-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt an, wie lange beim Ausführen eines Befehls gewartet wird, bis der Versuch beendet und ein Fehler generiert wird.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Sets or returns a **Long** value that indicates, in seconds, how long to wait for a command to execute. Default is 30.

## <a name="remarks"></a>HinwBemerkungeneise

Use the **CommandTimeout** property on a [Connection](connection-object-ado.md) object or [Command](command-object-ado.md) object to allow the cancellation of an [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method call, due to delays from network traffic or heavy server use. If the interval set in the **CommandTimeout** property elapses before the command completes execution, an error occurs and ADO cancels the command. If you set the property to zero, ADO will wait indefinitely until the execution is complete. Make sure the provider and data source to which you are writing code support the **CommandTimeout** functionality.

Die Einstellung von **CommandTimeout** in einem **Connection** -Objekt hat keine Auswirkung auf die Einstellung von **CommandTimeout** in einem **Command** -Objekt im gleichen **Connection** -Objekt. Das heißt, die **CommandTimeout** -Eigenschaft eines **Command** -Objekts erbt den Wert der **CommandTimeout** -Eigenschaft des **Connection** -Objekts nicht.

In einem **Connection**-Objekt behält die **CommandTimeout**-Eigenschaft nach dem Öffnen des **Connection**-Objekts Lese-/Schreibzugriff.

