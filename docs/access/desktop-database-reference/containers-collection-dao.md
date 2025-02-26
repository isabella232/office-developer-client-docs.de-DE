---
title: Containers-Auflistung (DAO)
TOCTitle: Containers Object
ms:assetid: 4996ee39-ea13-f560-3069-dd7bc6022119
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193464(v=office.15)
ms:contentKeyID: 48544642
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f71bd90d6538c7a7ebb06b9f345ecd5cc16009da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626967"
---
# <a name="containers-collection-dao"></a>Containers-Auflistung (DAO)

**Gilt für**: Access 2013, Office 2013

Eine **Containers** -Auflistung enthält alle **Container** -Objekte, die in einer Datenbank definiert sind.

## <a name="remarks"></a>Bemerkungen

Jedes **Database-Objekt** verfügt über eine **Containers-Auflistung,** die aus integrierten **Containerobjekten** besteht. Einige dieser **Container**-Objekte werden durch das Microsoft Access-Datenbankmodul und einige möglicherweise durch andere Anwendungen definiert.

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
                Debug.Print "  " & prpLoop.Name _
                   & " = " prpLoop
             Next prpLoop
    
          Next ctrLoop
    
          .Close
       End With
    
    End Sub
```
