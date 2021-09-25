---
title: Behandeln von Fehlern in Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bb499b24b151f93d68ef28594217f6707bb48b34
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615445"
---
# <a name="handling-errors-in-visual-c"></a>Behandeln von Fehlern in Visual C++


**Gilt für**: Access 2013, Office 2013

In COM, most operations return an HRESULT return code that indicates whether a function completed successfully. Die \# Importdirektive generiert Wrappercode um jede "raw"-Methode oder -Eigenschaft und überprüft das zurückgegebene HRESULT. Wenn HRESULT einen Fehler angibt, löst der Wrappercode einen COM-Fehler aus, indem \_ com \_ issue \_ errorex() mit dem HRESULT-Rückgabecode als Argument aufgerufen wird. COM error objects can be caught in a **try-catch** block. (Um der Effizienz willen, fangen Sie einen Verweis auf ein \_ \_ Com-Fehlerobjekt ab.)

Denken Sie daran, dass es sich um ADO-Fehler handelt, die das Ergebnis eines Fehlers bei einem ADO-Vorgang sind. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekts angezeigt.

Die \# Importdirektive erstellt nur Fehlerbehandlungsroutinen für Methoden und Eigenschaften, die im ADO-.dll deklariert sind. However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function. See the topic Visual C++ Extensions for examples.

