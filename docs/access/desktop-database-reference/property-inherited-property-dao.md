---
title: Eigenschaft. Inherited-Eigenschaft (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf3aef6d04c7d7cc573ec1d6efaca7d5238f5125
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302926"
---
# <a name="propertyinherited-property-dao"></a>Eigenschaft. Inherited-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013 

Gibt einen Wert zurück, der angibt, ob ein **[Property](property-object-dao.md)** -Objekt von einem zugrunde liegenden Objekt geerbt wurde.

## <a name="syntax"></a>Syntax

*Ausdruck* . Geerbt

*Ausdruck* Eine Variable, die ein **Property-** Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Bei integrierten **Property**-Objekten, die vordefinierte Eigenschaften darstellen, kann nur **False** zurückgegeben werden.

Mit der **Inherited**-Eigenschaft können Sie feststellen, ob für ein bestimmtes Objekt ein benutzerdefiniertes **Property**-Objekt erstellt wurde, oder ob das **Property**-Objekt von einem anderen Objekt geerbt wurde. Beispiel: Sie erstellen ein neues **Property**-Objekt für ein **[QueryDef](querydef-object-dao.md)**-Objekt und öffnen dann über das **QueryDef**-Objekt ein **[Recordset](recordset-object-dao.md)**-Objekt. Dieses neue **Property**-Objekt ist Teil der  **[Properties](properties-collection-dao.md)**-Auflistung des **Recordset**-Objekts, und seine **Inherited**-Eigenschaft erhält den Wert **True**, da die Eigenschaft für das **QueryDef**-Objekt erstellt wurde und nicht für das **Recordset**-Objekt.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Inherited**-Eigenschaft verwendet, um festzustellen, ob ein benutzerdefiniertes **Property**-Objekt für ein **Recordset**-Objekt erstellt wurde oder für ein anderes zugrunde liegendes Objekt.

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

