---
title: Fields-Auflistung (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726260"
---
# <a name="fields-collection-ado"></a><span data-ttu-id="22545-102">Fields-Auflistung (ADO)</span><span class="sxs-lookup"><span data-stu-id="22545-102">Fields collection (ADO)</span></span>


<span data-ttu-id="22545-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22545-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="22545-104">Enthält alle [Field](field-object-ado.md)-Objekte eines [Recordset](recordset-object-ado.md)- oder [Record](record-object-ado.md)-Objekts.</span><span class="sxs-lookup"><span data-stu-id="22545-104">Contains all the [Field](field-object-ado.md) objects of a [Recordset](recordset-object-ado.md) or [Record](record-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="22545-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22545-105">Remarks</span></span>

<span data-ttu-id="22545-p101">Ein **Recordset** -Objekt besitzt eine **Fields** -Auflistung, die aus **Field** -Objekten besteht. Jedes **Field** -Objekt entspricht einer Spalte im **Recordset** -Objekt. Sie können die **Fields** -Auflistung auffüllen, bevor Sie das **Recordset** -Objekt öffnen, indem Sie die [Refresh](refresh-method-ado.md)-Methode der Auflistung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22545-p101">A **Recordset** object has a **Fields** collection made up of **Field** objects. Each **Field** object corresponds to a column in the **Recordset**. You can populate the **Fields** collection before opening the **Recordset** by calling the [Refresh](refresh-method-ado.md) method on the collection.</span></span>

> [!NOTE]
> <span data-ttu-id="22545-109">[!HINWEIS] Eine detaillierte Beschreibung der Verwendung der **Field** -Objekte finden Sie in der Beschreibung des **Field** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="22545-109">See the **Field** object topic for a more detailed explanation of how to use **Field** objects.</span></span>

<span data-ttu-id="22545-110">Die **Fields** -Auflistung verfügt über die [Append](append-method-ado.md)-Methode, die ein **Field** -Objekt provisorisch erstellt und der Auflistung hinzufügt, sowie die **Update** -Methode, die Hinzufügungen und Löschungen fertig stellt.</span><span class="sxs-lookup"><span data-stu-id="22545-110">The **Fields** collection has an [Append](append-method-ado.md) method, which provisionally creates and adds a **Field** object to the collection, and an **Update** method, which finalizes any additions or deletions.</span></span>

<span data-ttu-id="22545-p102">Ein **Record** -Objekt hat zwei spezielle Felder, die mit [FieldEnum](fieldenum.md)-Konstanten indiziert werden können. Eine Konstante greift auf ein Feld zu, das den Standarddatenstrom für das **Record** -Objekt erstellt. Die andere Konstante greift auf ein Feld zu, das die absolute URL-Zeichenfolge für das **Record** -Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="22545-p102">A **Record** object has two special fields that can be indexed with [FieldEnum](fieldenum.md) constants. One constant accesses a field containing the default stream for the **Record**, and the other accesses a field containing the absolute URL string for the **Record**.</span></span>

<span data-ttu-id="22545-p103">Bestimmte Anbieter (z. B. der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) füllen die **Fields** -Auflistung mit einer Teilmenge der verfügbaren Felder für das **Record** - oder **Recordset** -Objekt auf. Andere Felder werden der Auflistung erst dann hinzugefügt, wenn im Code namentlich auf sie verwiesen wird oder sie indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="22545-p103">Certain providers (for example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) may populate the **Fields** collection with a subset of available fields for the **Record** or **Recordset**. Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</span></span>

<span data-ttu-id="22545-p104">Wenn Sie versuchen, auf ein nicht vorhandenes Feld namentlich zu verweisen, wird ein neues **Field** -Objekt an die **Fields** -Auflistung angehängt. Die [Status](status-property-ado-field.md)-Eigenschaft des Objekts hat den Wert **adFieldPendingInsert**. Wenn Sie [Update](update-method-ado.md) aufrufen, erstellt ADO ein neues Feld in der Datenquelle, sofern dies vom Anbieter zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="22545-p104">If you attempt to reference a nonexistent field by name, a new **Field** object will be appended to the **Fields** collection with a [Status](status-property-ado-field.md) of **adFieldPendingInsert**. When you call [Update](update-method-ado.md), ADO will create a new field in your data source if allowed by your provider.</span></span>

