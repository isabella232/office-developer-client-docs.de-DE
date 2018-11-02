---
title: Refresh-Methode (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4bbc44dbb9cdfeaac0904ed5296db206016211d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922762"
---
# <a name="refresh-method-ado"></a><span data-ttu-id="4bbb6-102">Refresh-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="4bbb6-102">Refresh method (ADO)</span></span>


<span data-ttu-id="4bbb6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bbb6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bbb6-104">Die Objekte in einer Auflistung werden aktualisiert, um Objekte widerzuspiegeln, die vom Anbieter verfügbar sind und spezifisch für diesen sind.</span><span class="sxs-lookup"><span data-stu-id="4bbb6-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bbb6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bbb6-105">Syntax</span></span>

<span data-ttu-id="4bbb6-106">*Auflistung*. Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4bbb6-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="4bbb6-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4bbb6-107">Remarks</span></span>

<span data-ttu-id="4bbb6-108">Abhängig von der Auflistung, aus der Sie die **Refresh** -Methode aufrufen, werden unterschiedliche Tasks ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bbb6-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bbb6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bbb6-109">Parameters</span></span>

<span data-ttu-id="4bbb6-p101">Durch Verwenden der **Refresh** -Methode für die [Parameters](command-object-ado.md)-Auflistung eines [Command](parameters-collection-ado.md)-Objekts werden anbieterseitige Parameterinformationen für die im **Command** -Objekt angegebene gespeicherte Prozedur oder parametrisierte Abfrage abgerufen. Für Anbieter, die Aufrufe gespeicherter Prozeduren oder parametrisierte Abfragen nicht unterstützen, ist die Auflistung leer.</span><span class="sxs-lookup"><span data-stu-id="4bbb6-p101">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object. The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="4bbb6-112">Legen Sie die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft des **Command** -Objekts auf ein gültiges [Connection](connection-object-ado.md)-Objekt, die [CommandText](commandtext-property-ado.md)-Eigenschaft auf einen gültigen Befehl und die [CommandType](commandtype-property-ado.md)-Eigenschaft auf **adCmdStoredProc** fest, bevor Sie die **Refresh** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4bbb6-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="4bbb6-113">Wenn Sie vor dem Aufrufen der **Refresh** -Methode auf die **Parameters** -Auflistung zugreifen, wird die Methode automatisch von ADO aufgerufen, und die Auflistung wird aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="4bbb6-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4bbb6-p102">Wenn Sie die Refresh-Methode zum Abrufen von Parameterinformationen vom Anbieter verwenden und mindestens ein Parameter-Objekt mit dem variable-length-Datentyp zurückgegeben wird, wird der Speicher für die Parameter von ADO möglicherweise basierend auf der potenziellen Maximalgröße zugeordnet. Dies verursacht einen Fehler bei der Ausführung. Legen Sie die Size-Eigenschaft für diese Parameter vor dem Aufrufen der Execute-Methode explizit fest, um Fehler zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4bbb6-p102">If you use the <STRONG>Refresh</STRONG> method to obtain parameter information from the provider and it returns one or more variable-length data type <A href="parameter-object-ado.md">Parameter</A> objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution. You should explicitly set the <A href="size-property-ado.md">Size</A> property for these parameters before calling the <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</A> method to prevent errors.</span></span></P>



<span data-ttu-id="4bbb6-116">**Fields**</span><span class="sxs-lookup"><span data-stu-id="4bbb6-116">**Fields**</span></span>

<span data-ttu-id="4bbb6-p103">Das Verwenden der **Refresh** -Methode für die **Fields** -Auflistung hat keine sichtbare Auswirkung. Zum Abrufen von Änderungen aus der zugrunde liegenden Datenbankstruktur müssen Sie entweder die [Requery](requery-method-ado.md)-Methode oder, wenn Textmarken vom [Recordset](recordset-object-ado.md)-Objekt nicht unterstützt werden, die [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bbb6-p103">Using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="4bbb6-119">**Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="4bbb6-119">**Properties**</span></span>

<span data-ttu-id="4bbb6-p104">Durch Verwenden der **Refresh** -Methode für eine **Properties** -Auflistung mancher Objekte wird die Auflistung mit den vom Anbieter verfügbar gemachten dynamischen Eigenschaften aufgefüllt. Durch diese Eigenschaften werden Informationen zu anbieterspezifischer Funktionalität bereitgestellt, die über die von ADO unterstützten integrierten Eigenschaften hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="4bbb6-p104">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes. These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

