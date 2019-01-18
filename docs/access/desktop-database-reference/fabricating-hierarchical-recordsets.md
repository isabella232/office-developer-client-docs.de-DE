---
title: Fabrizieren hierarchischer Recordsets
TOCTitle: Fabricating hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f644f25a04c5573a93aa106884473fed6b45440e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715578"
---
# <a name="fabricating-hierarchical-recordsets"></a>Fabrizieren hierarchischer Recordsets


**Betrifft**: Access 2013, Office 2013

Im folgenden Beispiel wird veranschaulicht, wie ein hierarchisches Recordset ohne eine zugrunde liegende Datenquelle bereitzustellen, mit der Datenstrukturierungssyntax Spalten für übergeordnete und untergeordnete untergeordneten **Recordset-Objekte**definiert.

Zum Erstellen eines hierarchischen **Recordset** -Objekts müssen Sie den Microsoft Data Shaping Dienst für OLE DB (MSDataShape) angeben. Außerdem können Sie im Verbindungszeichenfolgen-Parameter der [Open](connection-object-ado.md)-Methode des [Connection](open-method-ado-connection.md)-Objekts NONE als Datenproviderwert angeben. Weitere Informationen finden Sie unter [Erforderliche Anbieter für die Datenstrukturierung](required-providers-for-data-shaping.md).

```vb
    Dim cn As New ADODB.Connection
    Dim rsCustomers As New ADODB.Recordset
    
    cn.Open "Provider=MSDataShape;Data Provider=NONE;"
     
    strShape = _
    "SHAPE APPEND NEW adInteger AS CustID," & _
                " NEW adChar(25) AS FirstName," & _
                " NEW adChar(25) AS LastName," & _
                " NEW adChar(12) AS SSN," & _
                " NEW adChar(50) AS Address," & _
             " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                            " NEW adInteger AS CustID," & _
                            " NEW adChar(20) AS BodyColor, " & _
                         " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                                        " NEW adChar(20) AS Make, " & _
                                        " NEW adChar(20) AS Model," & _
                                        " NEW adChar(4) AS Year) " & _
                            " AS VINS RELATE VIN_NO TO VIN_NO))" & _
                " AS Vehicles RELATE CustID TO CustID) "
     
    rsCustomers.Open strShape, cn, adOpenStatic, adLockOptimistic, -1
```

Nachdem das **Recordset-Objekt** erstellt haben, können werden aufgefüllt, bearbeitet oder in einer Datei gespeichert.

