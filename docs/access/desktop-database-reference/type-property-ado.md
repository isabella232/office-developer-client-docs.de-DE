---
title: Type-Eigenschaft (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 646284877722baf9aec6bb591b071667fdf9cc1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867727"
---
# <a name="type-property-ado"></a><span data-ttu-id="df777-102">Type-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="df777-102">Type property (ADO)</span></span>


<span data-ttu-id="df777-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df777-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df777-104">Gibt den Funktions- oder Datentyp eines [Parameter](parameter-object-ado.md)-, [Field](field-object-ado.md)- oder [Property](property-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="df777-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="df777-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="df777-105">Settings and return values</span></span>

<span data-ttu-id="df777-106">Legt einen [DataTypeEnum](datatypeenum.md)-Wert fest oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="df777-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df777-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df777-107">Remarks</span></span>

<span data-ttu-id="df777-p101">Bei **Parameter** -Objekten ist die **Type** -Eigenschaft nicht schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Type** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="df777-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="df777-110">Bei allen anderen Objekten ist die **Type** -Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="df777-110">For all other objects, the **Type** property is read-only.</span></span>

