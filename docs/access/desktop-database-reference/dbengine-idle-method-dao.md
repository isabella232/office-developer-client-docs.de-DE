---
title: DBEngine.Idle-Methode (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f94d869cd04dc0b16e0b428abaf60e4be32dacb7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998056"
---
# <a name="dbengineidle-method-dao"></a>DBEngine.Idle-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Unterbricht die Datenverarbeitung und ermöglicht es dem Microsoft Access-Datenbankmodul, anstehende Aufgaben auszuführen, z. B. Speicheroptimierung oder Timeouts von Seiten (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Idle (***Aktion***)

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

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
<th><p>Erforderlich oder optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Action</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Gibt die auszuführende Aktion an. Kann eine der <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong>-Konstanten sein.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Mit der **Idle**-Methode kann das Microsoft Access-Datenbankmodul Hintergrundaufgaben ausführen, die wegen der umfangreichen Datenverarbeitung möglicherweise nicht mehr aktuell sind. Dies kommt oft in Multitaskingumgebungen mit mehreren Benutzern vor, in denen die Hintergrundverarbeitungszeit nicht ausreicht, um alls Datensätze in einem **[Recordset](recordset-object-dao.md)** auf dem aktuellen Stand zu halten.

In der Regel dürfen keine anderen Aktionen ausgeführt werden (einschließlich Bewegungen des Mauszeigers), damit Lesesperren entfernt und Daten in lokalen Recordset-Objekten vom Typ Dynaset aktualisiert werden können. Wenn Sie regelmäßig die Idle-Methode verwenden, kann das Microsoft Access-Datenbankmodul die Hintergrundverarbeitung durch das Freigeben von unnötigen Lesesperren beschleunigen.

Durch Angabe des optionalen Arguments **dbRefreshCache** wird der Speicher nur mit den aktuellsten Daten aus der Datenbank aktualisiert.

Sie müssen diese Methode nur dann in Einzelbenutzerumgebungen anrwenden, wenn mehrere Instanzen einer Anwendung ausgeführt werden. Durch die **Idle**-Methode kann die Leistung in einer Mehrbenutzerumgebung verbessert werden, da das Datenbankmodul gezwungen wird, Daten auf einen Datenträger zu schreiben und Sperren im Speicher freizugeben.


> [!NOTE]
> [!HINWEIS] Sie können Lesesperren auch dadurch freigeben, dass Sie Operationen zum Bestandteil einer Transaktion machen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die Idle-Methode verwendet, um sicherzustellen, dass eine Ausgabeprozedur auf die aktuellsten Daten zugreift, die in der Datenbank verfügbar sind. Zum Ausführen dieses Vorgangs ist die IdleOutput-Prozedur erforderlich.

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

