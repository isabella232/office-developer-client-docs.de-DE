---
title: Clear-Methode-ActiveX Data Objects (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0d76480bdb5d5a3ab258e103a00707af303a4d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296360"
---
# <a name="clear-method-ado"></a><span data-ttu-id="5cd57-102">Clear-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cd57-102">Clear method (ADO)</span></span>


<span data-ttu-id="5cd57-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cd57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cd57-104">Alle **Error**-Objekte werden aus der **Errors**-Auflistung entfernt.</span><span class="sxs-lookup"><span data-stu-id="5cd57-104">Removes all the **Error** objects from the **Errors** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cd57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cd57-105">Syntax</span></span>

<span data-ttu-id="5cd57-106">*Fehler*. Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="5cd57-106">*Errors*.Clear</span></span>

## <a name="remarks"></a><span data-ttu-id="5cd57-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cd57-107">Remarks</span></span>

<span data-ttu-id="5cd57-p101">Verwenden Sie die **Clear** -Methode für die [Errors](errors-collection-ado.md)-Auflistung, um alle vorhandenen [Error](error-object-ado.md)-Objekte aus der Auflistung zu entfernen. Wenn ein Fehler auftritt, wird die **Errors** -Auflistung automatisch von ADO gelöscht und mit auf dem neuen Fehler basierenden **Error** -Objekten gefüllt.</span><span class="sxs-lookup"><span data-stu-id="5cd57-p101">Use the **Clear** method on the [Errors](errors-collection-ado.md) collection to remove all existing [Error](error-object-ado.md) objects from the collection. When an error occurs, ADO automatically clears the **Errors** collection and fills it with **Error** objects based on the new error.</span></span>

<span data-ttu-id="5cd57-p102">Von manchen Eigenschaften und Methoden werden Warnungen zurückgegeben, die als **Error** -Objekte in der **Errors** -Auflistung angezeigt werden, ohne dass die Ausführung eines Programms angehalten wird. Rufen Sie vor dem Aufrufen der Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt oder der [Open](open-method-ado-connection.md)-Methode für ein [Connection](connection-object-ado.md)-Objekt oder vor dem Festlegen der [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt die **Clear** -Methode für die **Errors** -Auflistung auf. Auf diese Weise können Sie die [Count](count-property-ado.md)-Eigenschaft der **Errors** -Auflistung lesen, um auf zurückgegebene Warnungen zu testen.</span><span class="sxs-lookup"><span data-stu-id="5cd57-p102">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a [Connection](connection-object-ado.md) object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

