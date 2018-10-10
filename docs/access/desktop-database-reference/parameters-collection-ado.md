---
title: Parameters-Auflistung (ADO)
TOCTitle: Parameters Collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 96d2f4094c6b0df43e1579d7d35cbb78c12cc39c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473877"
---
# <a name="parameters-collection-ado"></a><span data-ttu-id="890d3-102">Parameters-Auflistung (ADO)</span><span class="sxs-lookup"><span data-stu-id="890d3-102">Parameters Collection (ADO)</span></span>


<span data-ttu-id="890d3-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="890d3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="890d3-104">Enthält alle [Parameter](parameter-object-ado.md)-Objekte eines [Command](command-object-ado.md)-Objekts.</span><span class="sxs-lookup"><span data-stu-id="890d3-104">Contains all the [Parameter](parameter-object-ado.md) objects of a [Command](command-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="890d3-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="890d3-105">Remarks</span></span>

<span data-ttu-id="890d3-106">Ein **Command** -Objekt besitzt eine **Parameters** -Auflistung, die aus **Parameter** -Objekten besteht.</span><span class="sxs-lookup"><span data-stu-id="890d3-106">A **Command** object has a **Parameters** collection made up of **Parameter** objects.</span></span>

<span data-ttu-id="890d3-p101">Mithilfe der [Refresh](refresh-method-ado.md)-Methode für eine **Parameters** -Auflistung eines **Command** -Objekts rufen Sie Anbieterparameterinformationen für die gespeicherte Prozedur oder parametrisierte Abfrage ab, die im **Command** -Objekt angegeben wist. Einige Anbieter unterstützen keine Aufrufe von gespeicherten Prozeduren oder parametrisierte Abfragen. Wenn Sie einen solchen Anbieter verwenden und die **Refresh** -Methode für die **Parameters** -Auflistung aufrufen, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="890d3-p101">Using the [Refresh](refresh-method-ado.md) method on a **Command** object's **Parameters** collection retrieves provider parameter information for the stored procedure or parameterized query specified in the **Command** object. Some providers do not support stored procedure calls or parameterized queries; calling the **Refresh** method on the **Parameters** collection when using such a provider will return an error.</span></span>

<span data-ttu-id="890d3-109">Wenn Sie eigene **Parameter** -Objekte definiert haben und auf die **Parameters** -Auflistung zugreifen, bevor Sie die **Refresh** -Methode aufrufen, ruft ADO automatisch die Methode auf und füllt sie auf.</span><span class="sxs-lookup"><span data-stu-id="890d3-109">If you have not defined your own **Parameter** objects and you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

<span data-ttu-id="890d3-p102">Sie können die Aufrufe des Providers zur Verbesserung der Leistung gering halten, wenn Sie die Eigenschaften der Parameter kennen, die der gespeicherten Prozedur oder der aufzurufenden parametrisierten Abfrage zugeordnet sind. Verwenden Sie die [CreateParameter](createparameter-method-ado.md)-Methode, um **Parameter** -Objekte mit den entsprechenden Eigenschaftseinstellungen zu erstellen, und verwenden Sie die [Append](append-method-ado.md)-Methode, um diese der **Parameters** -Auflistung hinzuzufügen. Auf diese Weise können Sie Parameterwerte festlegen und zurückgeben, ohne den Provider für die Parameterinformationen aufrufen zu müssen. Wenn Sie die Abfrage an einen Provider richten, der keine Parameterinformationen bereitstellt, müssen Sie die **Parameters** -Auflistung mit dieser Methode manuell zurückgeben, um Parameter verwenden zu können. Mit der [Delete](delete-method-ado-parameters-collection.md)-Methode können Sie **Parameter** -Objekte aus der **Parameters** -Auflistung entfernen, falls nötig.</span><span class="sxs-lookup"><span data-stu-id="890d3-p102">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call. Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the **Parameters** collection. This lets you set and return parameter values without having to call the provider for the parameter information. If you are writing to a provider that does not supply parameter information, you must manually populate the **Parameters** collection using this method to be able to use parameters at all. Use the [Delete](delete-method-ado-parameters-collection.md) method to remove **Parameter** objects from the **Parameters** collection if necessary.</span></span>

<span data-ttu-id="890d3-115">Die Objekte in der **Parameters** -Auflistung eines **Recordset** -Objekts liegen außerhalb des Gültigkeitsbereichs (und sind somit nicht verfügbar), wenn das **Recordset** -Objekt geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="890d3-115">The objects in the **Parameters** collection of a **Recordset** go out of scope (therefore becoming unavailable) when the **Recordset** is closed.</span></span>

