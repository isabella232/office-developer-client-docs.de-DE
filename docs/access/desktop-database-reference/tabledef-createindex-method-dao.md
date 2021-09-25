---
title: TableDef.CreateIndex-Methode (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 5a88ecf43d84867f770cecd44057d0c796350e62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601688"
---
# <a name="tabledefcreateindex-method-dao"></a>TableDef.CreateIndex-Methode (DAO)

**Gilt für**: Access 2013, Office 2013 

Erstellt ein neues **[Index](index-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateIndex(***Name***)

*Ausdruck* Eine Variable, die ein **TableDef**-Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>String</strong> -Objekt, mit dem das neue <strong>Index</strong> -Objekt eindeutig benannt wird. Weitere Informationen zu gültigen <strong>Index</strong> -Namen erhalten Sie unter der <strong>Name</strong> -Eigenschaft.  </p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Index 

## <a name="remarks"></a>HinwBemerkungeneise

Mit der **CreateIndex**-Methode können Sie ein neues **Index**-Objekt für ein **TableDef**-Objekt erstellen. Wenn Sie beim Verwenden von **CreateIndex** den optionalen Teil name weglassen, können Sie die **Name**-Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Ob Sie nach dem Anfügen des Objekts dessen **Name**-Eigenschaft festlegen können, hängt davon ab, welcher Objekttyp die **Indexes**-Auflistung enthält. Weitere Informationen finden Sie im Thema zur **Name**-Eigenschaft.

Wenn sich der Name auf ein Objekt bezieht, das bereits ein Element der Auflistung ist, tritt ein Laufzeitfehler auf, wenn Sie die **[Append-Methode](fields-append-method-dao.md)** verwenden.

Wenn Sie ein **Index** -Objekt aus einer Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung.

## <a name="example"></a>Beispiel

Dieses Beispiel verwendet die **CreateIndex** -Methode, um zwei neue **Index** -Objekte zu erstellen, und fügt sie dann der **Indexes** -Auflistung des **TableDef** -Objekts der Employees-Tabelle (Personal) an. Anschließend führt es die Indexes-Auflistung des **TableDef** -Objekts, die **Fields** -Auflistung des neuen **Index** -Objekts und die Properties-Auflistung des neuen **Index** -Objekts auf. Zum Ausführen dieser Prozedur ist die CreateIndexOutput-Funktion erforderlich.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
