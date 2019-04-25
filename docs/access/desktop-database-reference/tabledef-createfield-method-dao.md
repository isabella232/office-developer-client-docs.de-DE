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
localization_priority: Priority
ms.openlocfilehash: 713f2530369a824a6d7204655ded4333f7fe2765
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308442"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="d7199-102">TableDef.CreateField-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="d7199-102">TableDef.CreateField Method (DAO)</span></span>

<span data-ttu-id="d7199-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7199-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7199-104">Erstellt ein neues **[Field](field-object-dao.md)**-Objekt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="d7199-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7199-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7199-105">Syntax</span></span>

<span data-ttu-id="d7199-106">*Ausdruck* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span><span class="sxs-lookup"><span data-stu-id="d7199-106">CreateField( Name ,  Type ,  Size )</span></span>

<span data-ttu-id="d7199-107">*Ausdruck* Eine Variable, die ein **TableDef**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d7199-107">*expression*  A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7199-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7199-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7199-109">Name</span><span class="sxs-lookup"><span data-stu-id="d7199-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d7199-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="d7199-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d7199-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d7199-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d7199-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7199-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7199-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="d7199-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="d7199-114">Optional</span><span class="sxs-lookup"><span data-stu-id="d7199-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d7199-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d7199-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d7199-p101">Eine Zeichenfolge, die das neue <strong>Field</strong>-Objekt eindeutig benennt. Unter der <strong><a href="connection-name-property-dao.md">Name</a></strong>-Eigenschaft finden Sie Einzelheiten zu gültigen <strong>Field</strong>-Namen.</span><span class="sxs-lookup"><span data-stu-id="d7199-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7199-118"><em>Typ</em></span><span class="sxs-lookup"><span data-stu-id="d7199-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="d7199-119">Optional</span><span class="sxs-lookup"><span data-stu-id="d7199-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="d7199-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d7199-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d7199-p102">Eine Konstante, die den Datentyp des neuen <strong>Field</strong>-Objekts bestimmt. Unter der <strong><a href="field-type-property-dao.md">Type</a></strong>-Eigenschaft finden Sie gültige Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d7199-p102">A constant that determines the data type of the new <strong>Field</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7199-123"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="d7199-123"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="d7199-124">Optional</span><span class="sxs-lookup"><span data-stu-id="d7199-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="d7199-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d7199-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d7199-126">Eine ganze Zahl, die die maximale Größe eines <strong>Field</strong>-Objekts, das Text enthält, in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="d7199-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="d7199-127">Unter der <strong><a href="field-size-property-dao.md">Size</a></strong>-Eigenschaft finden Sie gültige Werte für size.</span><span class="sxs-lookup"><span data-stu-id="d7199-127">See the <a href="field-size-property-dao.md"><strong>Size</strong></a> property for valid size values.</span></span> <span data-ttu-id="d7199-128">Dieses Argument wird für numerische Felder und Felder mit fester Breite ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d7199-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="d7199-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7199-129">Return value</span></span>

<span data-ttu-id="d7199-130">Feld</span><span class="sxs-lookup"><span data-stu-id="d7199-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="d7199-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7199-131">Remarks</span></span>

<span data-ttu-id="d7199-p104">Mit der **CreateField**-Methode können Sie ein neues Feld erstellen und den Namen, den Datentyp sowie die Größe des Felds angeben. Wenn Sie einen oder mehrere der optionalen Teile für **CreateField** weglassen, können Sie die entsprechende Eigenschaft mithilfe einer entsprechenden Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das neue Objekt angefügt haben, können Sie einige, aber nicht alle Eigenschafteneinstellungen ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d7199-p104">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="d7199-136">Die Argumente Typ und Größe gelten nur für **Field**-Objekte in einem **TableDef**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7199-136">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="d7199-137">Diese Argumente werden ignoriert, wenn ein **Field**-Objekt einem **Index**- oder **Relation**-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7199-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="d7199-138">Bezieht sich Name auf ein Objekt, das bereits ein Element der Auflistung ist, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)**-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7199-138">If  name refers to an object that is already a member of the collection, a run-time error occurs when you use the  Append  method.</span></span>

<span data-ttu-id="d7199-p106">Um ein **Field**-Objekt aus einer **Fields**-Auflistung zu entfernen, führen Sie die **[Delete](fields-delete-method-dao.md)**-Methode für die Auflistung aus. Sie können ein **Field**-Objekt nicht mehr aus der **Fields**-Auflistung eines **TableDef**-Objekts löschen, nachdem Sie einen Index erstellt haben, der auf das Feld verweist.</span><span class="sxs-lookup"><span data-stu-id="d7199-p106">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="d7199-141">\*\*Link zur Verfügung gestellt von: \*\* [UtterAccess](https://www.utteraccess.com)-Community.</span><span class="sxs-lookup"><span data-stu-id="d7199-141">**Link provided by:Community Member Icon** The [UtterAccess](https://www.utteraccess.com) community</span></span> <span data-ttu-id="d7199-142">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="d7199-142">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="d7199-143">Hinzufügen eines Hyperlinkfelds zu einer vorhandenen Tabelle mit DAO</span><span class="sxs-lookup"><span data-stu-id="d7199-143">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="d7199-144">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d7199-144">Example</span></span>

<span data-ttu-id="d7199-p108">Im folgenden Beispiel wird veranschaulicht, wie Sie ein berechnetes Feld erstellen. Die CreateField-Methode erstellt ein Feld namens **FullName**. Die Expression-Eigenschaft wird dann auf den Ausdruck festgelegt, der den Wert des Felds berechnet.</span><span class="sxs-lookup"><span data-stu-id="d7199-p108">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="d7199-148">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d7199-148">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

