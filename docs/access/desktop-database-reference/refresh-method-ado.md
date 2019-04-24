---
title: Refresh-Methode (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bd7c47e7c3e41a7b42571043cfafc9e4e909a9f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309256"
---
# <a name="refresh-method-ado"></a><span data-ttu-id="37342-102">Refresh-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="37342-102">Refresh method (ADO)</span></span>

<span data-ttu-id="37342-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37342-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37342-104">Die Objekte in einer Auflistung werden aktualisiert, um Objekte widerzuspiegeln, die vom Anbieter verfügbar sind und spezifisch für diesen sind.</span><span class="sxs-lookup"><span data-stu-id="37342-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="37342-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37342-105">Syntax</span></span>

<span data-ttu-id="37342-106">*Sammlung*. Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="37342-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="37342-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37342-107">Remarks</span></span>

<span data-ttu-id="37342-108">Abhängig von der Auflistung, aus der Sie die **Refresh**-Methode aufrufen, werden unterschiedliche Tasks ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37342-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="37342-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="37342-109">Parameters</span></span>

<span data-ttu-id="37342-p101">Durch Verwenden der **Refresh**-Methode für die [Parameters](parameters-collection-ado.md)-Auflistung eines [Command](command-object-ado.md)-Objekts werden anbieterseitige Parameterinformationen für die im **Command**-Objekt angegebene gespeicherte Prozedur oder parametrisierte Abfrage abgerufen. Für Anbieter, die Aufrufe gespeicherter Prozeduren oder parametrisierte Abfragen nicht unterstützen, ist die Auflistung leer.</span><span class="sxs-lookup"><span data-stu-id="37342-p101">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object. The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="37342-112">Legen Sie die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft des **Command** -Objekts auf ein gültiges [Connection](connection-object-ado.md)-Objekt, die [CommandText](commandtext-property-ado.md)-Eigenschaft auf einen gültigen Befehl und die [CommandType](commandtype-property-ado.md)-Eigenschaft auf **adCmdStoredProc** fest, bevor Sie die **Refresh** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37342-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="37342-113">Wenn Sie vor dem Aufrufen der **Refresh**-Methode auf die **Parameters**-Auflistung zugreifen, wird die Methode automatisch von ADO aufgerufen, und die Auflistung wird aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="37342-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

> [!NOTE]
> <span data-ttu-id="37342-p102">If you use the **Refresh** method to obtain parameter information from the provider and it returns one or more variable-length data type [Parameter](parameter-object-ado.md) objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution. You should explicitly set the [Size](size-property-ado.md) property for these parameters before calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method to prevent errors.</span><span class="sxs-lookup"><span data-stu-id="37342-p102">If you use the **Refresh** method to obtain parameter information from the provider and it returns one or more variable-length data type [Parameter](parameter-object-ado.md) objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution. You should explicitly set the [Size](size-property-ado.md) property for these parameters before calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method to prevent errors.</span></span>

### <a name="fields"></a><span data-ttu-id="37342-116">Fields</span><span class="sxs-lookup"><span data-stu-id="37342-116">Fields</span></span>

<span data-ttu-id="37342-p103">Das Verwenden der **Refresh**-Methode für die **Fields**-Auflistung hat keine sichtbare Auswirkung. Zum Abrufen von Änderungen aus der zugrunde liegenden Datenbankstruktur müssen Sie entweder die [Requery](requery-method-ado.md)-Methode oder, wenn Textmarken vom [Recordset](recordset-object-ado.md)-Objekt nicht unterstützt werden, die [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="37342-p103">Using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

### <a name="properties"></a><span data-ttu-id="37342-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37342-119">Properties</span></span>

<span data-ttu-id="37342-p104">Durch Verwenden der **Refresh**-Methode für eine **Properties**-Auflistung mancher Objekte wird die Auflistung mit den vom Anbieter verfügbar gemachten dynamischen Eigenschaften aufgefüllt. Durch diese Eigenschaften werden Informationen zu anbieterspezifischer Funktionalität bereitgestellt, die über die von ADO unterstützten integrierten Eigenschaften hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="37342-p104">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes. These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

