---
title: Property-Objekt (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63df510830dee77ababc9ee1be53f0ae328ad8c3
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997119"
---
# <a name="property-object-dao"></a><span data-ttu-id="67bab-102">Property-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="67bab-102">Property object (DAO)</span></span>

<span data-ttu-id="67bab-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67bab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67bab-104">Ein **Property**-Objekt stellt eine integrierte oder benutzerdefinierte Eigenschaft eines DAO-Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="67bab-104">A **Property** object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="remarks"></a><span data-ttu-id="67bab-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67bab-105">Remarks</span></span>

<span data-ttu-id="67bab-p101">Alle DAO-Objekte, außer den Objekten **Connection** und **Error**, enthalten eine **Properties**-Auflistung mit **Property**-Objekten, die den integrierten Eigenschaften dieses DAO-Objekts entsprechen. Der Benutzer kann außerdem **Property**-Objekte definieren und sie der **Properties**-Auflistung eines DAO-Objekts anfügen. Diese **Property**-Objekte (die häufig lediglich "Eigenschaften" genannt werden) kennzeichnen die betreffende Objektinstanz eindeutig.</span><span class="sxs-lookup"><span data-stu-id="67bab-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection which has **Property** objects corresponding to built-in properties of that DAO object. The user can also define **Property** objects and append them to the **Properties** collection of some DAO objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="67bab-109">Sie können für die folgenden Objekte benutzerdefinierte Eigenschaften erstellen:</span><span class="sxs-lookup"><span data-stu-id="67bab-109">You can create user-defined properties for the following objects:</span></span>

- <span data-ttu-id="67bab-110">**Database**-, **Index**-, **QueryDef**- und **TableDef**-Objekte</span><span class="sxs-lookup"><span data-stu-id="67bab-110">**Database**, **Index**, **QueryDef**, and **TableDef** objects</span></span>

- <span data-ttu-id="67bab-111">**Field**-Objekte in **Fields**-Auflistungen von **QueryDef**- und **TableDef**-Objekten</span><span class="sxs-lookup"><span data-stu-id="67bab-111">**Field** objects in **Fields** collections of **QueryDef** and **TableDef** objects</span></span>

<span data-ttu-id="67bab-p102">Um eine benutzerdefinierte Eigenschaft hinzuzufügen, erstellen Sie mit der **CreateProperty**-Methode ein **Property**-Objekt mit einer eindeutigen Einstellung der **Name**-Eigenschaft. Legen Sie die Eigenschaften **Type** und **Value** des neuen **Property**-Objekts fest, und fügen Sie es dann der **Properties**-Auflistung des entsprechenden Objekts an. Das Objekt, dem Sie die benutzerdefinierte Eigenschaft hinzufügen, muss bereits Bestandteil einer Auflistung sein. Wenn auf ein benutzerdefiniertes **Property**-Objekt verwiesen wird, das noch keiner **Properties**-Auflistung angefügt ist, tritt ein Fehler auf. Ein Fehler tritt auch auf, wenn ein benutzerdefiniertes **Property**-Objekt einer **Properties**-Auflistung angefügt wird, die bereits ein **Property**-Objekt desselben Namens enthält.</span><span class="sxs-lookup"><span data-stu-id="67bab-p102">To add a user-defined property, use the **CreateProperty** method to create a **Property** object with a unique **Name** property setting. Set the **Type** and **Value** properties of the new **Property** object, and then append it to the **Properties** collection of the appropriate object. The object to which you are adding the user-defined property must already be appended to a collection. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="67bab-116">Sie können benutzerdefinierte Eigenschaften aus der **Properties**-Auflistung entfernen, integrierte Eigenschaften können jedoch nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="67bab-116">You can delete user-defined properties from the **Properties** collection, but you can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="67bab-p103">[!HINWEIS] Ein benutzerdefiniertes **Property**-Objekt ist nur einer bestimmten Objektinstanz zugeordnet. Die Eigenschaft ist nicht für alle Objektinstanzen des ausgewählten Typs definiert.</span><span class="sxs-lookup"><span data-stu-id="67bab-p103">A user-defined **Property** object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="67bab-p104">Mithilfe der **Properties**-Auflistung eines Objekts können Sie dessen integrierte und benutzerdefinierte Eigenschaften auflisten. Zu diesem Zweck müssen Sie nicht genau wissen, welche Eigenschaften vorhanden sind oder mit welchen Merkmalen (**Name**- und **Type**-Eigenschaft) sie bearbeitet werden. Ein Fehler tritt jedoch auf, wenn Sie eine lesegeschützte Eigenschaft zu lesen versuchen (z. B. die **Password**-Eigenschaft eines **Workspace**-Objekts), oder wenn Sie versuchen, eine Eigenschaft in einem ungeeigneten Kontext zu lesen oder zu schreiben (z. B. die Einstellung der **Value**-Eigenschaft eines **Field**-Objekts in der **Fields**-Auflistung eines **TableDef**-Objekts).</span><span class="sxs-lookup"><span data-stu-id="67bab-p104">You can use the **Properties** collection of an object to enumerate the object's built-in and user-defined properties. You don't need to know beforehand exactly which properties exist or what their characteristics (**Name** and **Type** properties) are to manipulate them. However, if you try to read a write-only property, such as the **Password** property of a **Workspace** object, or try to read or write a property in an inappropriate context, such as the **Value** property setting of a **Field** object in the **Fields** collection of a **TableDef** object, an error occurs.</span></span>

<span data-ttu-id="67bab-122">Das **Property**-Objekt besitzt auch vier integrierte Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="67bab-122">The **Property** object also has four built-in properties:</span></span>

- <span data-ttu-id="67bab-123">Die **Name**-Eigenschaft mit einem **String**-Wert, der die Eigenschaft eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="67bab-123">The **Name** property, a **String** that uniquely identifies the property.</span></span>

- <span data-ttu-id="67bab-124">Die **Type**-Eigenschaft mit einem **Integer**-Wert, der den Datentyp der Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="67bab-124">The **Type** property, an **Integer** that specifies the property data type.</span></span>

- <span data-ttu-id="67bab-125">Die **Value**-Eigenschaft mit einem **Variant**-Wert, der die Einstellung der Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="67bab-125">The **Value** property, a **Variant** that contains the property setting.</span></span>

- <span data-ttu-id="67bab-p105">Die **Inherited**-Eigenschaft mit einem **Boolean**-Wert, der angibt, ob die Eigenschaft von einem anderen Objekt vererbt wurde. Ein **Field**-Objekt in einer **Fields**-Auflistung eines **Recordset**-Objekts kann z. B. Eigenschaften des zugrunde liegenden **TableDef**- oder **QueryDef**-Objekts erben.</span><span class="sxs-lookup"><span data-stu-id="67bab-p105">The **Inherited** property, a **Boolean** that indicates whether the property is inherited from another object. For example, a **Field** object in a **Fields** collection of a **Recordset** object can inherit properties from the underlying **TableDef** or **QueryDef** object.</span></span>

<span data-ttu-id="67bab-128">Wenn Sie auf ein integriertes **Property**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="67bab-128">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="67bab-129">\* Objekt \***. Eigenschaften**(0)</span><span class="sxs-lookup"><span data-stu-id="67bab-129">\*object\***.Properties**(0)</span></span>

- <span data-ttu-id="67bab-130">Objekt \*\*\*\*. Eigenschaften\**("* Name \*")</span><span class="sxs-lookup"><span data-stu-id="67bab-130">*object\***.Properties**("* name\*")</span></span>

- <span data-ttu-id="67bab-131">Objekt \*\*\*\*. Eigenschaften\**\!* Namen \*\]</span><span class="sxs-lookup"><span data-stu-id="67bab-131">*object\***.Properties**\!\[* name\*\]</span></span>

<span data-ttu-id="67bab-132">Bei einer integrierten Eigenschaft können Sie auch diese Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="67bab-132">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="67bab-133">- *Objekt*. *Name*</span><span class="sxs-lookup"><span data-stu-id="67bab-133">*object*.*name*</span></span>

> [!NOTE]
> <span data-ttu-id="67bab-134">Für eine benutzerdefinierte Eigenschaft müssen Sie die vollständige \*Objekt \***verwenden. Eigenschaften**("\* Name \*") Syntax.</span><span class="sxs-lookup"><span data-stu-id="67bab-134">For a user-defined property, you must use the full *object\***.Properties**("* name\*") syntax.</span></span>

<span data-ttu-id="67bab-p106">Sie können mit denselben Syntaxformen auf die **Value**-Eigenschaft eines **Property**-Objekts verweisen. Der Kontext des Verweises entscheidet, ob Sie sich auf das **Property**-Objekt selbst oder auf die **Value**-Eigenschaft des **Property**-Objekts beziehen.</span><span class="sxs-lookup"><span data-stu-id="67bab-p106">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

