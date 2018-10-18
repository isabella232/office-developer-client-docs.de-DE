---
title: TableDef.CreateField-Methode (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1fd66910a3630d8968f75c5a59bb535520419994
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606983"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="c6846-102">TableDef.CreateField-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c6846-102">TableDef.CreateField Method (DAO)</span></span>

<span data-ttu-id="c6846-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6846-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6846-104">Erstellt ein neues **[Field](field-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c6846-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6846-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6846-105">Syntax</span></span>

<span data-ttu-id="c6846-106">*Ausdruck* . CreateField (_**Name**_, _**Typ**_, _**Größe**_)</span><span class="sxs-lookup"><span data-stu-id="c6846-106">*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span></span>

<span data-ttu-id="c6846-107">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c6846-107">*expression* A variable that represents a **TableDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c6846-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6846-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6846-109">Name</span><span class="sxs-lookup"><span data-stu-id="c6846-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c6846-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="c6846-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c6846-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c6846-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c6846-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6846-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6846-113">Name</span><span class="sxs-lookup"><span data-stu-id="c6846-113">Name</span></span></p></td>
<td><p><span data-ttu-id="c6846-114">Optional</span><span class="sxs-lookup"><span data-stu-id="c6846-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="c6846-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c6846-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c6846-p101">Eine Zeichenfolge, die das neue <strong>Field</strong> -Objekt eindeutig benennt. Unter der <strong><a href="connection-name-property-dao.md">Name</a></strong> -Eigenschaft finden Sie Einzelheiten zu gültigen <strong>Field</strong> -Namen.  </span><span class="sxs-lookup"><span data-stu-id="c6846-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6846-118">Typ</span><span class="sxs-lookup"><span data-stu-id="c6846-118">Type</span></span></p></td>
<td><p><span data-ttu-id="c6846-119">Optional</span><span class="sxs-lookup"><span data-stu-id="c6846-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="c6846-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c6846-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c6846-p102">Eine Konstante, die den Datentyp des neuen <strong>Field</strong> -Objekts bestimmt. Unter der <strong><a href="field-type-property-dao.md">Type</a></strong> -Eigenschaft finden Sie gültige Datentypen.  </span><span class="sxs-lookup"><span data-stu-id="c6846-p102">A constant that determines the data type of the new <strong>Field</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6846-123">Größe</span><span class="sxs-lookup"><span data-stu-id="c6846-123">Size</span></span></p></td>
<td><p><span data-ttu-id="c6846-124">Optional</span><span class="sxs-lookup"><span data-stu-id="c6846-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="c6846-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c6846-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c6846-126">Eine Integer, die die maximale Größe eines <strong>Field</strong> -Objekts mit Text in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="c6846-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="c6846-127">Finden Sie unter der <strong><a href="field-size-property-dao.md">Size</a></strong> -Eigenschaft für gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="c6846-127">See the <strong><a href="field-size-property-dao.md">Size</a></strong> property for valid size values.</span></span> <span data-ttu-id="c6846-128">Dieses Argument wird für numerische Felder und Felder mit festgelegtem Format ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c6846-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6846-129"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="c6846-129"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="c6846-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6846-130">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="c6846-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6846-131">Return value</span></span>
>>>>>>> <span data-ttu-id="c6846-132">master</span><span class="sxs-lookup"><span data-stu-id="c6846-132">master</span></span>

<span data-ttu-id="c6846-133">Feld</span><span class="sxs-lookup"><span data-stu-id="c6846-133">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="c6846-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c6846-134">Remarks</span></span>

<span data-ttu-id="c6846-p104">Mit der **CreateField**-Methode können Sie ein neues Feld erstellen und den Namen und Datentyp sowie die Größe des Felds angeben. Wenn Sie **CreateField** verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das neue Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c6846-p104">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="c6846-139">Den Typ und die Größe der Argumente gelten nur für **Field** -Objekte in ein **TableDef** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c6846-139">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="c6846-140">Wird ein **Field**-Objekt mit einem **Index**- oder **Relation**-Objekt verknüpft, werden diese Argumente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c6846-140">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="c6846-141">Wenn Name auf ein Objekt, das bereits ein Element der Auflistung ist bezieht, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6846-141">If Name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="c6846-p106">Wenn Sie ein **Field**-Objekt aus einer **Fields**-Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung. Sie können ein **Field**-Objekt nicht mehr aus der **Fields**-Auflistung eines **TableDef**-Objekts löschen, nachdem Sie einen Index erstellt haben, der auf das Feld verweist.</span><span class="sxs-lookup"><span data-stu-id="c6846-p106">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="c6846-144">**Link bereitgestellt, von** der Community [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="c6846-144">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="c6846-145">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="c6846-145">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="c6846-146">Hinzufügen eines Hyperlinkfelds zu einer vorhandenen Tabelle mit DAO</span><span class="sxs-lookup"><span data-stu-id="c6846-146">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="c6846-147">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6846-147">Example</span></span>

<span data-ttu-id="c6846-p108">Im folgenden Beispiel wird veranschaulicht, wie Sie ein berechnetes Feld erstellen. Die CreateField-Methode erstellt ein Feld namens **FullName**. Die Expression-Eigenschaft wird dann auf den Ausdruck festgelegt, der den Wert des Felds berechnet.</span><span class="sxs-lookup"><span data-stu-id="c6846-p108">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="c6846-151">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c6846-151">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

