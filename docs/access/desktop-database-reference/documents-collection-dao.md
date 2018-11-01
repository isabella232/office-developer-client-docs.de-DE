---
title: Documents Collection (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ed91166c8a244c20848069ecfd936a25c10accd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878164"
---
# <a name="documents-collection-dao"></a>Documents Collection (DAO)


**Betrifft**: Access 2013, Office 2013

Eine **Documents**-Auflistung enthält alle **Document**-Objekte für einen bestimmten Objekttyp (nur für Microsoft Access-Datenbanken).

## <a name="remarks"></a>Bemerkungen

Jedes **Container**-Objekt verfügt über eine **Documents**-Auflistung mit **Document**-Objekten, die Instanzen integrierter Objekte des durch das **Container**-Objekt angegebenen Typs beschreiben.

Der Verweis auf ein **Document**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:

  - **Documents**(0)

  - **Dokumente** ("*Name*")

  - **Dokumente**\!\[*Namen*\]

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

