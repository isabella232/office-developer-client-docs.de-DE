---
title: Type-Eigenschaft (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314014"
---
# <a name="type-property-ado"></a><span data-ttu-id="622f3-102">Type-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="622f3-102">Type property (ADO)</span></span>


<span data-ttu-id="622f3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="622f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="622f3-104">Gibt den Funktions- oder Datentyp eines [Parameter](parameter-object-ado.md)-, [Field](field-object-ado.md)- oder [Property](property-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="622f3-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="622f3-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="622f3-105">Settings and return values</span></span>

<span data-ttu-id="622f3-106">Legt einen [DataTypeEnum](datatypeenum.md)-Wert fest oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="622f3-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="622f3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="622f3-107">Remarks</span></span>

<span data-ttu-id="622f3-p101">Bei **Parameter** -Objekten ist die **Type** -Eigenschaft nicht schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Type** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="622f3-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="622f3-110">Bei allen anderen Objekten ist die **Type** -Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="622f3-110">For all other objects, the **Type** property is read-only.</span></span>

