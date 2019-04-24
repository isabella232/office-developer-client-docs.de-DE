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
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="53ed5-102">Behandeln von Fehlern in Visual C++</span><span class="sxs-lookup"><span data-stu-id="53ed5-102">Handling errors in Visual C++</span></span>


<span data-ttu-id="53ed5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53ed5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53ed5-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span><span class="sxs-lookup"><span data-stu-id="53ed5-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="53ed5-105">Die \#Import-Direktive generiert Wrappercode um jede "rohe" Methode oder Eigenschaft und überprüft das zurückgegebene HRESULT.</span><span class="sxs-lookup"><span data-stu-id="53ed5-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="53ed5-106">Wenn der HRESULT-Fehler angibt, löst der Wrappercode einen COM-Fehler \_aus\_,\_indem com-Problem errorex () mit dem HRESULT-Rückgabecode als Argument aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="53ed5-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="53ed5-107">COM error objects can be caught in a **try-catch** block.</span><span class="sxs-lookup"><span data-stu-id="53ed5-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="53ed5-108">(Aus Effizienzgründen sollten Sie einen Verweis auf ein \_com\_Error-Objekt abfangen.)</span><span class="sxs-lookup"><span data-stu-id="53ed5-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="53ed5-p102">Denken Sie daran, dass es sich um ADO-Fehler handelt, die das Ergebnis eines Fehlers bei einem ADO-Vorgang sind. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53ed5-p102">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="53ed5-111">Die \#Import-Direktive erstellt nur Fehlerbehandlungsroutinen für Methoden und Eigenschaften, die in der ADO. dll deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="53ed5-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="53ed5-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span><span class="sxs-lookup"><span data-stu-id="53ed5-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="53ed5-113">See the topic Visual C++ Extensions for examples.</span><span class="sxs-lookup"><span data-stu-id="53ed5-113">See the topic Visual C++ Extensions for examples.</span></span>

