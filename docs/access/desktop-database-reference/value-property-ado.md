---
title: Value-Eigenschaft (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 00b82706d934356621ac1e41fffca61ec88e081f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715067"
---
# <a name="value-property-ado"></a><span data-ttu-id="f5510-102">Value-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f5510-102">Value property (ADO)</span></span>

<span data-ttu-id="f5510-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5510-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5510-104">Gibt den Wert an, der einem [Field](field-object-ado.md)-, [Parameter](parameter-object-ado.md)- oder [Property](property-object-ado.md)-Objekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f5510-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f5510-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f5510-105">Settings and return values</span></span>

<span data-ttu-id="f5510-p101">Legt einen **Variant** -Wert fest, der den Wert eines Objekts angibt, oder gibt den Wert zurück. Der Standardwert hängt von der [Type](type-property-ado.md)-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="f5510-p101">Sets or returns a **Variant** value that indicates the value of the object. Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5510-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f5510-108">Remarks</span></span>

<span data-ttu-id="f5510-p102">Verwenden Sie die **Value** -Eigenschaft zum Festlegen oder Zurückgeben von Daten bei **Field** -Objekten, zum Festlegen oder Zurückgeben von Parameterwerten bei **Parameter** -Objekten oder zum Festlegen oder Zurückgeben von Eigenschafteneinstellungen bei **Property** -Objekten. Ob die **Value** -Eigenschaft schreibgeschützt ist, hängt von verschiedenen Faktoren ab. Weitere Informationen dazu finden Sie in dem Thema zum jeweiligen Objekt.</span><span class="sxs-lookup"><span data-stu-id="f5510-p102">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects. Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="f5510-111">ADO ermöglicht das Festlegen oder Zurückgeben von Long binary-Daten mit der Value-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f5510-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>

> [!NOTE]
> <span data-ttu-id="f5510-p103">[!HINWEIS] Bei **Parameter** -Objekten liest ADO die **Value** -Eigenschaft nur einmal vom Anbieter. Wenn ein Befehl ein **Parameter** -Objekt enthält, dessen **Value** -Eigenschaft leer ist, und Sie ein [Recordset](recordset-object-ado.md)-Objekt durch den Befehl erstellen, schließen Sie zuerst das **Recordset** -Objekt. Rufen Sie erst danach die **Value** -Eigenschaft ab. Andernfalls ist bei einigen Anbietern die **Value** -Eigenschaft möglicherweise leer und enthält nicht den richtigen Wert.</span><span class="sxs-lookup"><span data-stu-id="f5510-p103">For **Parameter** objects, ADO reads the **Value** property only once from the provider. If a command contains a **Parameter** whose **Value** property is empty, and you create a [Recordset](recordset-object-ado.md) from the command, ensure that you first close the **Recordset** before retrieving the **Value** property. Otherwise, for some providers, the **Value** property may be empty, and won't contain the correct value.</span></span>

<span data-ttu-id="f5510-p104">Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, muss die **Value** -Eigenschaft festgelegt werden, bevor andere **Field** -Eigenschaften angegeben werden. Zuerst müssen ein angegebener Wert für die **Value** -Eigenschaft zugewiesen und die [Update](update-method-ado.md)-Methode für die **Fields** -Auflistung aufgerufen worden sein. Anschließend kann auf weitere Eigenschaften, wie z. B. [Type](type-property-ado.md) oder [Attributes](attributes-property-ado.md), zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="f5510-p104">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

