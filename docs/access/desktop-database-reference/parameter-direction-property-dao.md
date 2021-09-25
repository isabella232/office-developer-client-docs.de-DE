---
title: Parameter.Direction-Eigenschaft (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: e8b8168383433a9b35523dd866afe98396b1e9f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606576"
---
# <a name="parameterdirection-property-dao"></a>Parameter.Direction-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013


## <a name="syntax"></a>Syntax

*Ausdruck* . Richtung

*Ausdruck* Eine Variable, die ein **Parameter** -Objekt darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

The setting or return value is a Long that can be set to one of the **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** constants.

Bestimmen Sie mit der **Direction**-Eigenschaft, ob der Parameter ein Eingabeparameter und/oder ein Ausgabeparameter oder der Rückgabewert der Prozedur ist. Einige ODBC-Treiber geben keine Informationen zur Richtung der Parameter für eine SELECT-Anweisung oder einen Prozeduraufruf an. In diesen Fällen muss die Richtung vor dem Ausführen der Abfrage festgelegt werden.

Die folgende Prozedur gibt beispielsweise einen Wert aus einer gespeicherten Prozedur namens "get \_ employees" zurück:

{? = call get \_ employees}

Dieser Aufruf ergibt einen Parameter, und zwar den Rückgabewert. Sie müssen die Richtung dieses Parameters auf **dbParamOutput** oder **dbParamReturnValue** festlegen, bevor Sie **[QueryDef](querydef-object-dao.md)** ausführen.

Legen Sie die Richtung aller Parameter fest, ausgenommen **dbParamInput**, bevor Sie auf die Parameterwerte zugreifen oder die Werte festlegen und bevor Sie **QueryDef** ausführen.

Verwenden Sie **dbParamReturnValue** für Rückgabewerte. Falls diese Option jedoch vom Treiber oder dem Server nicht unterstützt wird, können Sie stattdessen **dbParamOutput** verwenden.

Der Microsoft SQL Server-Treiber legt die **Direction**-Eigenschaft automatisch für alle Prozedurparameter fest. Nicht alle ODBC-Treiber erkennen die Richtung eines Abfrageparameters. In diesen Fällen muss die Richtung vor dem Ausführen der Abfrage festgelegt werden.

## <a name="example"></a>Beispiel

Dieses Beispiel konfiguriert mit der **Direction**-Eigenschaft die Parameter einer Abfrage für eine ODBC-Datenquelle.

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

