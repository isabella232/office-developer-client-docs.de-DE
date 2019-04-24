---
title: Property-Objekt (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 262f4873359508a985b27f3d4ea70a5fcbfd620f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302919"
---
# <a name="property-object-ado"></a><span data-ttu-id="1120b-102">Property-Objekt (ADO)</span><span class="sxs-lookup"><span data-stu-id="1120b-102">Property object (ADO)</span></span>


<span data-ttu-id="1120b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1120b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1120b-104">Stellt ein dynamisches Merkmal eines ADO-Objekts dar, das vom Anbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="1120b-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="1120b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1120b-105">Remarks</span></span>

<span data-ttu-id="1120b-106">ADO-Objekte weisen zwei Arten von Eigenschaften auf, nämlich integrierte und dynamische Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1120b-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="1120b-107">Bei integrierten Eigenschaften handelt es sich um die Eigenschaften, die in ADO implementiert werden und die mit der Syntax sofort für jedes neue Objekt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1120b-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="1120b-108">Sie erscheinen nicht als **Property** -Objekte in der [Properties](properties-collection-ado.md)-Auflistung eines Objekts, sodass Sie ihre Merkmale nicht ändern können, obwohl ihre Werte geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1120b-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="1120b-109">Dynamische Eigenschaften werden durch den zugrunde liegenden Datenanbieter definiert und in der **Properties** -Auflistung für das entsprechende ADO-Objekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1120b-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="1120b-110">Beispielsweise kann eine anbieterspezifische Eigenschaft kennzeichnen, ob Transaktionen oder Aktualisierungen von einem [Recordset](recordset-object-ado.md)-Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1120b-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="1120b-111">Diese zusätzlichen Eigenschaften werden als **Property**-Objekte in der **Properties**-Auflistung dieses **Recordset**-Objekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1120b-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="1120b-112">Auf dynamische Eigenschaften kann nur über die Auflistung mit der MyObject. Properties (0)-oder MyObject. Properties ("Name")-Syntax verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1120b-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="1120b-113">Keiner der beiden Eigenschaftstypen kann gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1120b-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="1120b-114">Ein dynamisches **Property**-Objekt weist vier integrierte Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="1120b-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="1120b-115">Die [Name](name-property-ado.md)-Eigenschaft ist eine Zeichenfolge zur Identifizierung der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1120b-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="1120b-116">Die [Type](type-property-ado.md)-Eigenschaft ist eine ganze Zahl zur Angabe des Datentyps der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1120b-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="1120b-p103">The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span><span class="sxs-lookup"><span data-stu-id="1120b-p103">The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="1120b-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span><span class="sxs-lookup"><span data-stu-id="1120b-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>

