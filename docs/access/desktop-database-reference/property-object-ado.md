---
title: Property-Objekt (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b26a305557e2b7244399c6c2c5513909846eaaff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929569"
---
# <a name="property-object-ado"></a><span data-ttu-id="557a3-102">Property-Objekt (ADO)</span><span class="sxs-lookup"><span data-stu-id="557a3-102">Property object (ADO)</span></span>


<span data-ttu-id="557a3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="557a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="557a3-104">Stellt ein dynamisches Merkmal eines ADO-Objekts dar, das vom Anbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="557a3-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="557a3-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="557a3-105">Remarks</span></span>

<span data-ttu-id="557a3-106">ADO-Objekte weisen zwei Arten von Eigenschaften auf, nämlich integrierte und dynamische Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="557a3-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="557a3-107">Integrierte Eigenschaften sind diese Eigenschaften in ADO implementiert und für jedes neue Objekt mithilfe der Syntax.</span><span class="sxs-lookup"><span data-stu-id="557a3-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="557a3-108">Sie erscheinen nicht als **Property** -Objekte in der [Properties](properties-collection-ado.md)-Auflistung eines Objekts, sodass Sie ihre Merkmale nicht ändern können, obwohl ihre Werte geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="557a3-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="557a3-109">Dynamische Eigenschaften werden durch den zugrunde liegenden Datenanbieter definiert und in der **Properties** -Auflistung für das entsprechende ADO-Objekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="557a3-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="557a3-110">Beispielsweise kann eine anbieterspezifische Eigenschaft anzeigen, ob Transaktionen oder Aktualisierungen von einem [Recordset](recordset-object-ado.md) -Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="557a3-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="557a3-111">Diese zusätzlichen Eigenschaften werden als **Property** -Objekte in der **Properties** -Auflistung dieses **Recordset** -Objekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="557a3-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="557a3-112">Dynamische Eigenschaften können nur über die Auflistung mithilfe der MyObject.Properties(0) verwiesen werden oder oder MyObject.Properties("Name") Syntax.</span><span class="sxs-lookup"><span data-stu-id="557a3-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="557a3-113">Keiner der beiden Eigenschaftstypen kann gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="557a3-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="557a3-114">Ein dynamisches **Property** -Objekt weist vier integrierte Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="557a3-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="557a3-115">Die [Name](name-property-ado.md) -Eigenschaft ist eine Zeichenfolge zur Identifizierung der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="557a3-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="557a3-116">Die [Type](type-property-ado.md) -Eigenschaft ist eine ganze Zahl zur Angabe des Datentyps der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="557a3-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="557a3-p103">Die Value-Eigenschaft ist vom Datentyp Variant und enthält die Eigenschaftseinstellung. Value ist die Standardeigenschaft für ein Property-Objekt.</span><span class="sxs-lookup"><span data-stu-id="557a3-p103">The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="557a3-119">Die [Attributes](attributes-property-ado.md) -Eigenschaft ist ein long-Wert, der Merkmale der anbieterspezifischen Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="557a3-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>

