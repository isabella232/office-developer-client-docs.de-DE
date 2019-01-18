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
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="79685-102">Behandeln von Fehlern in Visual C++</span><span class="sxs-lookup"><span data-stu-id="79685-102">Handling errors in Visual C++</span></span>


<span data-ttu-id="79685-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79685-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79685-104">In COM geben die meisten Vorgänge einen HRESULT-Rückgabecode, der angibt, ob eine Funktion erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="79685-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="79685-105">Die \#Import-Direktive generiert Wrappercode um jede "unformatierte" Methode oder Eigenschaft und überprüft den zurückgegebenen HRESULT.</span><span class="sxs-lookup"><span data-stu-id="79685-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="79685-106">Wenn das HRESULT einen Fehler angibt, löst der Code einen COM-Fehler durch Aufrufen von \_com\_Problem\_errorex() mit dem HRESULT-Rückgabecode als Argument.</span><span class="sxs-lookup"><span data-stu-id="79685-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="79685-107">Com-Error-Objekte können in einem **Try-Catch** -Block abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="79685-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="79685-108">(Aus Gründen der Effizienz catch einen Verweis auf eine \_com\_Error-Objekt.)</span><span class="sxs-lookup"><span data-stu-id="79685-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="79685-p102">Denken Sie daran, dass es sich um ADO-Fehler handelt, die das Ergebnis eines Fehlers bei einem ADO-Vorgang sind. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79685-p102">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="79685-111">Die \#Import-Direktive erstellt nur Fehlerbehandlungsroutinen für Methoden und Eigenschaften, die in der ADO-DLL deklariert.</span><span class="sxs-lookup"><span data-stu-id="79685-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="79685-112">Jedoch können Sie denselben Mechanismus für die Fehlerbehandlung nutzen durch Ihre eigene fehlerüberprüfung Makro oder Inline-Funktion schreiben.</span><span class="sxs-lookup"><span data-stu-id="79685-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="79685-113">Finden Sie im Thema Visual C++-Erweiterungen für Beispiele.</span><span class="sxs-lookup"><span data-stu-id="79685-113">See the topic Visual C++ Extensions for examples.</span></span>

