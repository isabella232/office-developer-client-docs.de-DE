---
title: TableDef. CreateProperty-Methode (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 8a92cc64-414e-f33c-1c3e-d1b62c1688c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197102(v=office.15)
ms:contentKeyID: 48546197
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3018bf8cc9a62cb866b35992e25ecb1f8f41514f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308421"
---
# <a name="tabledefcreateproperty-method-dao"></a><span data-ttu-id="94156-102">TableDef. CreateProperty-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="94156-102">TableDef.CreateProperty method (DAO)</span></span>

<span data-ttu-id="94156-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94156-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94156-104">Erstellt ein neues, benutzerdefiniertes **[Property](property-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="94156-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="94156-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94156-105">Syntax</span></span>

<span data-ttu-id="94156-106">*Ausdruck* . CreateProperty (***Name***, ***Type***, ***value***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="94156-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="94156-107">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="94156-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="94156-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="94156-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94156-109">Name</span><span class="sxs-lookup"><span data-stu-id="94156-109">Name</span></span></p></th>
<th><p><span data-ttu-id="94156-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="94156-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="94156-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="94156-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="94156-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94156-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94156-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="94156-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="94156-114">Optional</span><span class="sxs-lookup"><span data-stu-id="94156-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="94156-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="94156-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="94156-116">Ein <strong>String</strong>-Wert, der das neue <strong>Property</strong>-Objekt eindeutig benennt.</span><span class="sxs-lookup"><span data-stu-id="94156-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="94156-117">Weitere Informationen zu gültigen <strong>Property</strong>-Namen finden Sie in dem Thema zur <strong>Name</strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="94156-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94156-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="94156-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="94156-119">Optional</span><span class="sxs-lookup"><span data-stu-id="94156-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="94156-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="94156-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="94156-121">Eine Konstante, die den Datentyp des neuen <strong>Property</strong>-Objekts definiert.</span><span class="sxs-lookup"><span data-stu-id="94156-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="94156-122">Unter der <strong><a href="field-type-property-dao.md">Type</a></strong> -Eigenschaft finden Sie gültige Datentypen.</span><span class="sxs-lookup"><span data-stu-id="94156-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94156-123"><em>Wert</em></span><span class="sxs-lookup"><span data-stu-id="94156-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="94156-124">Optional</span><span class="sxs-lookup"><span data-stu-id="94156-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="94156-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="94156-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="94156-126">Ein <strong>Variant</strong>-Wert, der den ursprünglichen Eigenschaftswert enthält.</span><span class="sxs-lookup"><span data-stu-id="94156-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="94156-127">Details finden Sie unter der <strong><a href="field-value-property-dao.md">value</a></strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="94156-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94156-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="94156-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="94156-129">Optional</span><span class="sxs-lookup"><span data-stu-id="94156-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="94156-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="94156-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="94156-131">Ein <strong>Variant</strong>-Wert (Untertyp <strong>Boolean</strong>), der angibt, ob <strong>Property</strong> ein DDL-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="94156-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="94156-132">Der Standardwert ist <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="94156-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="94156-133">Wenn DDL auf <strong>true</strong>festgelegt ist, können Benutzer dieses <strong>Property-</strong> Objekt nur ändern oder löschen, wenn Sie über die <strong>dbSecWriteDef</strong> -Berechtigung verfügen.</span><span class="sxs-lookup"><span data-stu-id="94156-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="94156-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94156-134">Return value</span></span>

<span data-ttu-id="94156-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94156-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="94156-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94156-136">Remarks</span></span>

<span data-ttu-id="94156-137">Ein benutzerdefiniertes **Property**-Objekt können Sie nur in der **[Properties](properties-collection-dao.md)** -Auflistung eines beständigen Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="94156-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="94156-p105">Wenn Sie **CreateProperty** verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen hierzu finden Sie in den Themen zur **Name**-, **Type**- und **Value**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="94156-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="94156-141">Wenn Name auf ein Objekt verweist, das bereits ein Element der Auflistung ist, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="94156-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="94156-142">Verwenden Sie die [**Delete**](fields-delete-method-dao.md) -Methode für die [**Properties**](properties-collection-dao.md) -Auflistung, um ein benutzerdefiniertes **Property**-Objekt aus der Auflistung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="94156-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection.</span></span> <span data-ttu-id="94156-143">Sie können keine integrierten Eigenschaften löschen.</span><span class="sxs-lookup"><span data-stu-id="94156-143">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="94156-144">Wenn Sie das Argument DDL weglassen, wird standardmäßig false (nicht-DDL) verwendet.</span><span class="sxs-lookup"><span data-stu-id="94156-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="94156-145">Da keine entsprechende DDL-Eigenschaft verfügbar gemacht wird, müssen Sie ein **Property-** Objekt, das Sie von DDL in nicht-DDL ändern möchten, löschen und neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="94156-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object that you want to change from DDL to non-DDL.</span></span>


