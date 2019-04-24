---
title: Behandeln von Fehlern in Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d0e76dc3cc9634a1531a34058bf7a1baf636c94c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292027"
---
# <a name="handling-errors-in-visual-c"></a>Behandeln von Fehlern in Visual C++


**Gilt für**: Access 2013, Office 2013

In COM, most operations return an HRESULT return code that indicates whether a function completed successfully. Die \#Import-Direktive generiert Wrappercode um jede "rohe" Methode oder Eigenschaft und überprüft das zurückgegebene HRESULT. Wenn der HRESULT-Fehler angibt, löst der Wrappercode einen COM-Fehler \_aus\_,\_indem com-Problem errorex () mit dem HRESULT-Rückgabecode als Argument aufgerufen wird. COM error objects can be caught in a **try-catch** block. (Aus Effizienzgründen sollten Sie einen Verweis auf ein \_com\_Error-Objekt abfangen.)

Denken Sie daran, dass es sich um ADO-Fehler handelt, die das Ergebnis eines Fehlers bei einem ADO-Vorgang sind. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekts angezeigt.

Die \#Import-Direktive erstellt nur Fehlerbehandlungsroutinen für Methoden und Eigenschaften, die in der ADO. dll deklariert sind. However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function. See the topic Visual C++ Extensions for examples.

