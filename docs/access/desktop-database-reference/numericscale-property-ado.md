---
title: NumericScale-Eigenschaft (ADO)
TOCTitle: NumericScale Property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d70144ae886f60285ad22067e0c52b9193a0005
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475621"
---
# <a name="numericscale-property-ado"></a><span data-ttu-id="5c2b9-102">NumericScale-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5c2b9-102">NumericScale Property (ADO)</span></span>


<span data-ttu-id="5c2b9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c2b9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5c2b9-104">Gibt die Dezimalstellen numerischer Werte in einem [Parameter](parameter-object-ado.md)- oder [Field](field-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5c2b9-104">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5c2b9-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5c2b9-105">Settings and Return Values</span></span>

<span data-ttu-id="5c2b9-106">Legt einen **Byte** -Wert fest, der die Anzahl von Dezimalstellen angibt, in die numerische Werte aufgelöst werden, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c2b9-106">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2b9-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5c2b9-107">Remarks</span></span>

<span data-ttu-id="5c2b9-108">Bestimmen Sie mit der **NumericScale** -Eigenschaft die Anzahl von Stellen rechts vom Dezimalkomma, die zur Darstellung von Werten für ein numerisches **Parameter** - oder **Field** -Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c2b9-108">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="5c2b9-109">Bei **Parameter** -Objekten ist die **NumericScale** -Eigenschaft nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5c2b9-109">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="5c2b9-p101">Bei einem **Field** -Objekt ist **NumericScale** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **NumericScale** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="5c2b9-p101">For a **Field** object, **NumericScale** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

