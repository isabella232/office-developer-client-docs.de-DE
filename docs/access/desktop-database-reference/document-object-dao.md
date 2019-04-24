---
title: Document-Objekt (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f82ace31a991a6700417d4c0d66bf775fcb7b26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293777"
---
# <a name="document-object-dao"></a>Document-Objekt (DAO)

**Gilt für**: Access 2013, Office 2013

Ein **Document**-Objekt schließt Informationen zu einer Objektinstanz ein. Bei dem Objekt kann es sich um eine Datenbank, gespeicherte Tabelle, Abfrage oder Beziehung handeln (gilt nur für Microsoft Access-Datenbanken).

## <a name="remarks"></a>Bemerkungen

Jedes **Container**-Objekt besitzt eine **Documents**-Auflistung mit **Document**-Objekten. Diese Objekte beschreiben die Instanzen von integrierten Objekten des Typs, der durch das **Container**-Objekt angegeben wird. In der folgenden Tabelle wird der Objekttyp der einzelnen **Document**-Objekte, der Name des jeweiligen **Container**-Objekts und der Typ der im **Document**-Objekt enthaltenen Informationen beschrieben.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Dokument</p></th>
<th><p>Container</p></th>
<th><p>Enthält Informationen zu</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Database</p></td>
<td><p>Datenbanken</p></td>
<td><p>Gespeicherten Datenbanken</p></td>
</tr>
<tr class="even">
<td><p>Tabelle oder Abfrage</p></td>
<td><p>Tables</p></td>
<td><p>Gespeicherten Tabellen oder Abfragen</p></td>
</tr>
<tr class="odd">
<td><p>Beziehung</p></td>
<td><p>Relations</p></td>
<td><p>Gespeicherten Beziehungen</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.

Bei einem **Document**-Objekt können Sie die folgenden Aktionen ausführen:

- Geben Sie mit der **Name**-Eigenschaft den Namen zurück, den das Objekt bei seiner Erstellung von einem Benutzer oder dem Microsoft Access-Datenbankmodul erhalten hat.

- Geben Sie mit der **Container**-Eigenschaft den Namen des **Container**-Objekts zurück, das das **Document**-Objekt enthält.

- Verwenden Sie die **Owner**-Eigenschaft, um den Eigentümer des Objekts festzulegen oder zurückzugeben. Um die **Owner**-Eigenschaft festlegen zu können, benötigen Sie Schreibberechtigungen für das **Document**-Objekt, außerdem müssen Sie die Eigenschaft auf den Namen eines vorhandenen **User**- oder **Group**-Objekts festlegen.

- Verwenden Sie die **UserName**- oder **Permissions**-Eigenschaft, um die Zugriffsberechtigungen eines Benutzers oder einer Gruppe für das Objekt festzulegen oder zurückzugeben. Um diese Eigenschaften festlegen zu können, benötigen Sie Schreibberechtigungen für das **Document**-Objekt, außerdem müssen Sie die **UserName**-Eigenschaft auf den Namen eines vorhandenen **User**- oder **Group**-Objekts festlegen.

- Verwenden Sie die **DateCreated**- oder **LastUpdated**-Eigenschaft, um das Datum und die Uhrzeit der Erstellung oder letzten Änderung des **Document**-Objekts zurückzugeben.

Da ein **Document**-Objekt einem vorhandenen Objekt entspricht, können keine neuen **Document**-Objekte erstellt oder vorhandene gelöscht werden. Wenn Sie auf ein **Document**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:

- **Documents**(0)

- **Dokumente** ("*Name*")

- ****\!Dokument\[*Name*\]

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Documents**-Auflistung aus dem Tabellencontainer aufgeführt und anschließend die **Properties**-Auflistung des ersten **Document**-Objekts in der Auflistung.

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<br/>

Dieses Beispiel zeigt mit den Eigenschaften **Owner** und **SystemDB** die Eigentümer verschiedener **Document**-Objekte an.

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

