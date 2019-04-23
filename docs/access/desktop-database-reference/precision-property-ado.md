---
title: Precision-Eigenschaft (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 662e5e9287da1ccfb81c727f5d5e5dfedce2969b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287475"
---
# <a name="precision-property-ado"></a><span data-ttu-id="33f1c-102">Precision-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="33f1c-102">Precision property (ADO)</span></span>


<span data-ttu-id="33f1c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33f1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33f1c-104">Gibt den Genauigkeitsgrad für numerische Werte in einem [Parameter](parameter-object-ado.md)-Objekt oder für numerische [Field](field-object-ado.md)-Objekte an.</span><span class="sxs-lookup"><span data-stu-id="33f1c-104">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="33f1c-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="33f1c-105">Settings and return values</span></span>

<span data-ttu-id="33f1c-106">Legt einen **Byte**-Wert fest oder gibt den Wert zurück, der die maximale Anzahl von Stellen angibt, die zum Darstellen eines Werts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33f1c-106">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="33f1c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33f1c-107">Remarks</span></span>

<span data-ttu-id="33f1c-108">Bestimmen Sie mit der **Precision**-Eigenschaft die maximale Anzahl von Stellen, die zum Darstellen von Werten für ein numerisches **Parameter**- oder **Field**-Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33f1c-108">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="33f1c-109">Der Wert ist bei einem **Parameter** -Objekt nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="33f1c-109">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="33f1c-p101">Bei einem **Field** -Objekt ist **Precision** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Precision** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="33f1c-p101">For a **Field** object, **Precision** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

