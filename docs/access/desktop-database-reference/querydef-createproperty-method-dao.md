---
title: QueryDef.CreateProperty-Methode (DAO)
TOCTitle: CreateProperty Method
ms:assetid: e107b7d0-5556-7b87-f131-95f518893e4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835663(v=office.15)
ms:contentKeyID: 48548250
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 251b6e9b48e4a65f40250e4120251c919c5d455f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997203"
---
# <a name="querydefcreateproperty-method-dao"></a><span data-ttu-id="b7e0b-102">QueryDef.CreateProperty-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="b7e0b-102">QueryDef.CreateProperty method (DAO)</span></span>

<span data-ttu-id="b7e0b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7e0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7e0b-104">Erstellt ein neues, benutzerdefiniertes **[Property](property-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b7e0b-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7e0b-105">Syntax</span></span>

<span data-ttu-id="b7e0b-106">*Ausdruck* . CreateProperty (***Name***, ***Typ***, ***Wert***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="b7e0b-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="b7e0b-107">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7e0b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7e0b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7e0b-109">Name</span><span class="sxs-lookup"><span data-stu-id="b7e0b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b7e0b-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="b7e0b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b7e0b-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b7e0b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b7e0b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7e0b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7e0b-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="b7e0b-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b7e0b-114">Optional</span><span class="sxs-lookup"><span data-stu-id="b7e0b-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b7e0b-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b7e0b-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e0b-p101">Ein <strong>String</strong>-Wert, der das neue <strong>Property</strong>-Objekt eindeutig benennt. Weitere Informationen zu gültigen <strong>Property</strong>-Namen finden Sie in dem Thema zur <strong>Name</strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e0b-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="b7e0b-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="b7e0b-119">Optional</span><span class="sxs-lookup"><span data-stu-id="b7e0b-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="b7e0b-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b7e0b-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e0b-p102">Eine Konstante, die den Datentyp des neuen <strong>Property</strong>-Objekts definiert. Informationen zu gültigen Datentypen finden Sie in dem Thema zur <strong><a href="field-type-property-dao.md">Type</a></strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e0b-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="b7e0b-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="b7e0b-124">Optional</span><span class="sxs-lookup"><span data-stu-id="b7e0b-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="b7e0b-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b7e0b-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e0b-p103">Ein <strong>Variant</strong>-Wert, der den ursprünglichen Eigenschaftswert enthält. Weitere Informationen finden Sie in dem Thema zur <strong><a href="field-value-property-dao.md">Value</a></strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e0b-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="b7e0b-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="b7e0b-129">Optional</span><span class="sxs-lookup"><span data-stu-id="b7e0b-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="b7e0b-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b7e0b-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e0b-131"><strong>Variant</strong> (Untertyp<strong>Boolean</strong> ), der angibt, ob die <strong>Eigenschaft</strong> ein DDL-Objekt ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="b7e0b-132">Der Standardwert ist <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="b7e0b-133">Wenn DDL auf <strong>True</strong>festgelegt ist, können nicht Benutzer ändern oder diese <strong>Property-</strong> Objekt löschen, es sei denn, sie <strong>über DbSecWriteDef</strong> berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="b7e0b-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7e0b-134">Return value</span></span>

<span data-ttu-id="b7e0b-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7e0b-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e0b-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7e0b-136">Remarks</span></span>

<span data-ttu-id="b7e0b-137">Ein benutzerdefiniertes **Property**-Objekt können Sie nur in der **[Properties](properties-collection-dao.md)** -Auflistung eines beständigen Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="b7e0b-p105">Wenn Sie **CreateProperty** verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen hierzu finden Sie in den Themen zur **Name**-, **Type**- und **Value**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="b7e0b-141">Wenn Name auf ein Objekt, das bereits ein Element der Auflistung ist bezieht, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="b7e0b-p106">Verwenden Sie die [**Delete**](fields-delete-method-dao.md) -Methode für die [**Properties**](properties-collection-dao.md) -Auflistung, um ein benutzerdefiniertes **Property**-Objekt aus der Auflistung zu entfernen. Sie können keine integrierten Eigenschaften löschen.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection. You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="b7e0b-144">Wenn Sie das Argument DDL weglassen, wird standardmäßig auf False (nicht-DDL).</span><span class="sxs-lookup"><span data-stu-id="b7e0b-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="b7e0b-145">Da keine entsprechende DDL-Eigenschaft verfügbar gemacht wird, müssen Sie löschen und neu erstellen ein **Property-** Objekt, das Sie von DDL in nicht-DDL ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="b7e0b-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object that you want to change from DDL to non-DDL.</span></span>


