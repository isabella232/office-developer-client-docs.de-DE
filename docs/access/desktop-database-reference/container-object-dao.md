---
title: Container-Objekt (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295632"
---
# <a name="container-object-dao"></a>Container-Objekt (DAO)

**Gilt für**: Access 2013, Office 2013

Ein **Container**-Objekt fasst ähnliche Typen von **Document**-Objekten in Gruppen zusammen.

## <a name="remarks"></a>Bemerkungen

Jedes **Database**-Objekt besitzt eine **Containers**-Auflistung, die aus integrierten **Container**-Objekten besteht. Anwendungen können eigene Dokumenttypen und entsprechende Container definieren (gilt nur für Microsoft Access-Datenbanken). Diese Objekte werden jedoch möglicherweise nicht immer von DAO unterstützt.

Einige dieser **Container**-Objekte werden durch das Microsoft Access-Datenbankmodul und einige möglicherweise durch andere Anwendungen definiert. In der folgenden Tabelle werden die Namen der einzelnen **Container**-Objekte, die durch das Microsoft Access-Datenbankmodul definiert werden, und der Typ der jeweils enthaltenen Informationen aufgeführt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Containername</p></th>
<th><p>Enthält Informationen zu</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Datenbanken</p></td>
<td><p>Gespeicherten Datenbanken</p></td>
</tr>
<tr class="even">
<td><p>Tables</p></td>
<td><p>Gespeicherten Tabellen und Abfragen</p></td>
</tr>
<tr class="odd">
<td><p>Relations</p></td>
<td><p>Gespeicherten Beziehungen</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.

Jedes **Container**-Objekt besitzt eine **Documents**-Auflistung mit **Document**-Objekten. Diese Objekte beschreiben die Instanzen von integrierten Objekten des Typs, der durch das **Container**-Objekt angegeben wird. In der Regel verwenden Sie ein **Container**-Objekt als direkte Verknüpfung mit den Informationen des **Document**-Objekts. Mithilfe der **Containers**-Auflistung können Sie die Sicherheit für alle **Document**-Objekte eines bestimmten Typs festlegen.

Bei einem vorhandenen **Container**-Objekt können Sie die folgenden Aktionen ausführen:

- Geben Sie mit der **Name**-Eigenschaft den vordefinierten Namen des **Container**-Objekts zurück.

- Verwenden Sie die **Owner**-Eigenschaft, um den Eigentümer des **Container**-Objekts festzulegen oder zurückzugeben. Um die **Owner**-Eigenschaft festlegen zu können, benötigen Sie Schreibberechtigungen für das **Container**-Objekt, außerdem müssen Sie die Eigenschaft auf den Namen eines vorhandenen **User**- oder **Group**-Objekts festlegen.

- Legen Sie mit den Eigenschaften **Permissions** und **UserName** die Zugriffsberechtigungen für das **Container**-Objekt fest. Jedes **Document**-Objekt, das in der **Documents**-Auflistung eines **Container**-Objekts erstellt wird, erbt diese Zugriffsberechtigungseinstellungen.

Da **Container**-Objekte integriert sind, können Sie neue **Container**-Objekte erstellen oder vorhandene Objekte löschen.

Wenn Sie auf ein **Container**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:

- **Container** 0

- **Container** ("*Name*")

- ****\!Container\[*Name*\]

## <a name="example"></a>Beispiel

Das folgende Beispiel führt die **Containers**-Auflistung der Nordwind-Datenbank und die **Properties**-Auflistung jedes **Container**-Objekts der Auflistung auf.

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
