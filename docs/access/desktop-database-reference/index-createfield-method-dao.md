---
title: Index.CreateField Method (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4c8c4d897e58655aa986ba2a0c28b7eece235a7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605898"
---
# <a name="indexcreatefield-method-dao"></a><span data-ttu-id="b9335-102">Index.CreateField Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="b9335-102">Index.CreateField Method (DAO)</span></span>


<span data-ttu-id="b9335-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9335-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b9335-104">Erstellt ein neues **[Field](field-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b9335-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9335-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9335-105">Syntax</span></span>

<span data-ttu-id="b9335-106">*Ausdruck* . CreateField (***Name***, ***Typ***, ***Größe***)</span><span class="sxs-lookup"><span data-stu-id="b9335-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="b9335-107">*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9335-107">*expression* A variable that represents an **Index** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b9335-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9335-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9335-109">Name</span><span class="sxs-lookup"><span data-stu-id="b9335-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b9335-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="b9335-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b9335-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b9335-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b9335-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9335-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9335-113">Name</span><span class="sxs-lookup"><span data-stu-id="b9335-113">Name</span></span></p></td>
<td><p><span data-ttu-id="b9335-114">Optional</span><span class="sxs-lookup"><span data-stu-id="b9335-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9335-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9335-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9335-p101">Eine Zeichenfolge, die das neue <strong>Field</strong> -Objekt eindeutig benennt. Unter der <strong><a href="connection-name-property-dao.md">Name</a></strong> -Eigenschaft finden Sie Einzelheiten zu gültigen <strong>Field</strong> -Namen.  </span><span class="sxs-lookup"><span data-stu-id="b9335-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9335-118">Typ</span><span class="sxs-lookup"><span data-stu-id="b9335-118">Type</span></span></p></td>
<td><p><span data-ttu-id="b9335-119">Optional</span><span class="sxs-lookup"><span data-stu-id="b9335-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9335-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9335-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9335-121">Argument wird für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9335-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9335-122">Größe</span><span class="sxs-lookup"><span data-stu-id="b9335-122">Size</span></span></p></td>
<td><p><span data-ttu-id="b9335-123">Optional</span><span class="sxs-lookup"><span data-stu-id="b9335-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9335-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9335-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9335-125">Argument wird für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9335-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9335-126"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b9335-126"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="b9335-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9335-127">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="b9335-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9335-128">Return value</span></span>
>>>>>>> <span data-ttu-id="b9335-129">master</span><span class="sxs-lookup"><span data-stu-id="b9335-129">master</span></span>

<span data-ttu-id="b9335-130">Feld</span><span class="sxs-lookup"><span data-stu-id="b9335-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="b9335-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9335-131">Remarks</span></span>

<span data-ttu-id="b9335-p102">Mit der **CreateField**-Methode können Sie ein neues Feld erstellen und den Namen und Datentyp sowie die Größe des Felds angeben. Wenn Sie **CreateField** verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das neue Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9335-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="b9335-136">Die Argumente Typ und Größe gelten nur für **Field** -Objekte in ein **TableDef** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b9335-136">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="b9335-137">Wird ein **Field**-Objekt mit einem **Index**- oder **Relation**-Objekt verknüpft, werden diese Argumente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b9335-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="b9335-138">Wenn Name auf ein Objekt, das bereits ein Element der Auflistung ist bezieht, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9335-138">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="b9335-p104">Wenn Sie ein **Field**-Objekt aus einer **Fields**-Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung. Sie können ein **Field**-Objekt nicht mehr aus der **Fields**-Auflistung eines **TableDef**-Objekts löschen, nachdem Sie einen Index erstellt haben, der auf das Feld verweist.</span><span class="sxs-lookup"><span data-stu-id="b9335-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

