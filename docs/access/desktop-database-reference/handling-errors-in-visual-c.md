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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709474"
---
# <a name="handling-errors-in-visual-c"></a>Behandeln von Fehlern in Visual C++


**Betrifft**: Access 2013, Office 2013

In COM geben die meisten Vorgänge einen HRESULT-Rückgabecode, der angibt, ob eine Funktion erfolgreich abgeschlossen. Die \#Import-Direktive generiert Wrappercode um jede "unformatierte" Methode oder Eigenschaft und überprüft den zurückgegebenen HRESULT. Wenn das HRESULT einen Fehler angibt, löst der Code einen COM-Fehler durch Aufrufen von \_com\_Problem\_errorex() mit dem HRESULT-Rückgabecode als Argument. Com-Error-Objekte können in einem **Try-Catch** -Block abgefangen werden. (Aus Gründen der Effizienz catch einen Verweis auf eine \_com\_Error-Objekt.)

Denken Sie daran, dass es sich um ADO-Fehler handelt, die das Ergebnis eines Fehlers bei einem ADO-Vorgang sind. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekts angezeigt.

Die \#Import-Direktive erstellt nur Fehlerbehandlungsroutinen für Methoden und Eigenschaften, die in der ADO-DLL deklariert. Jedoch können Sie denselben Mechanismus für die Fehlerbehandlung nutzen durch Ihre eigene fehlerüberprüfung Makro oder Inline-Funktion schreiben. Finden Sie im Thema Visual C++-Erweiterungen für Beispiele.

