---
title: Relation.CreateField-Methode (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae322277dd1d357aceb3f9129110dded705f9eca
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716285"
---
# <a name="relationcreatefield-method-dao"></a><span data-ttu-id="8c777-102">Relation.CreateField-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8c777-102">Relation.CreateField method (DAO)</span></span>

<span data-ttu-id="8c777-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c777-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c777-104">Erstellt ein neues **[Field](field-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="8c777-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c777-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c777-105">Syntax</span></span>

<span data-ttu-id="8c777-106">*Ausdruck* . CreateField (***Name***, ***Typ***, ***Größe***)</span><span class="sxs-lookup"><span data-stu-id="8c777-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="8c777-107">*Ausdruck* Eine Variable, die ein **Relation** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c777-107">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c777-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c777-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c777-109">Name</span><span class="sxs-lookup"><span data-stu-id="8c777-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8c777-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="8c777-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8c777-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8c777-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="8c777-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c777-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c777-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="8c777-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="8c777-114">Optional</span><span class="sxs-lookup"><span data-stu-id="8c777-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="8c777-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8c777-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8c777-p101">Eine Zeichenfolge, die das neue <strong>Field</strong> -Objekt eindeutig benennt. Unter der <strong><a href="connection-name-property-dao.md">Name</a></strong> -Eigenschaft finden Sie Einzelheiten zu gültigen <strong>Field</strong> -Namen.  </span><span class="sxs-lookup"><span data-stu-id="8c777-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c777-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="8c777-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="8c777-119">Optional</span><span class="sxs-lookup"><span data-stu-id="8c777-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="8c777-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8c777-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8c777-121">Argument wird für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c777-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c777-122"><em>Größe</em></span><span class="sxs-lookup"><span data-stu-id="8c777-122"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="8c777-123">Optional</span><span class="sxs-lookup"><span data-stu-id="8c777-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="8c777-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8c777-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8c777-125">Argument wird für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c777-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="8c777-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c777-126">Return value</span></span>

<span data-ttu-id="8c777-127">Feld</span><span class="sxs-lookup"><span data-stu-id="8c777-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="8c777-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c777-128">Remarks</span></span>

<span data-ttu-id="8c777-p102">Mit der **CreateField**-Methode können Sie ein neues Feld erstellen und den Namen und Datentyp sowie die Größe des Felds angeben. Wenn Sie **CreateField** verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das neue Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c777-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="8c777-133">Die Argumente Typ und Größe gelten nur für **Field** -Objekte in ein **TableDef** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8c777-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="8c777-134">Wird ein **Field**-Objekt mit einem **Index**- oder **Relation**-Objekt verknüpft, werden diese Argumente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8c777-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="8c777-135">Wenn Name auf ein Objekt, das bereits ein Element der Auflistung ist bezieht, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c777-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="8c777-p104">Wenn Sie ein **Field**-Objekt aus einer **Fields**-Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung. Sie können ein **Field**-Objekt nicht mehr aus der **Fields**-Auflistung eines **TableDef**-Objekts löschen, nachdem Sie einen Index erstellt haben, der auf das Feld verweist.</span><span class="sxs-lookup"><span data-stu-id="8c777-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

