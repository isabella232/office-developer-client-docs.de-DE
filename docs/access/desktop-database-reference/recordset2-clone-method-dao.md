---
title: Recordset2.Clone Method (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 47aa31bf6b32b674d7701b6572cc411eb88cc301
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603287"
---
# <a name="recordset2clone-method-dao"></a>Recordset2.Clone Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Erstellt ein doppeltes **[Recordset](recordset-object-dao.md)** -Objekt, das auf das ursprüngliche **Recordset2**-Objekt verweist.

## <a name="syntax"></a>Syntax

*Ausdruck* . Wenn Sie den Klon

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

<<<<<<< Kopf
### <a name="return-value"></a>Rückgabewert
=======
### <a name="return-value"></a>Rückgabewert
>>>>>>> master

Recordset

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Clone**-Methode zum Erstellen mehrerer **Recordset**-Objektduplikate. Jede Datensatzgruppe kann über einen eigenen aktuellen Datensatz verfügen. Die Verwendung von **Clone** führt noch nicht dazu, dass Daten in den Objekten oder in ihren zugrunde liegenden Strukturen geändert werden. Mit der **Clone**-Methode können Sie Lesezeichen in mehreren **Recordset2**-Objekten gemeinsam verwenden, da ihre Lesezeichen austauschbar sind.

Die **Clone**-Methode können Sie verwenden, um eine Operation für eine Datensatzgruppe auszuführen, die mehrere aktuelle Datensätze erfordert. Das geht schneller und ist effizienter, als eine zweite Datensatzgruppe zu öffnen. Wenn Sie eine Datensatzgruppe mit der **Clone**-Methode erstellen, fehlt zunächst ein aktueller Datensatz. Legen Sie zuerst die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft fest, oder verwenden Sie eine der **[Move](recordset-movefirst-method-dao.md)** -Methoden, eine der **[Find](recordset2-findfirst-method-dao.md)** -Methoden oder die **[Seek](recordset2-seek-method-dao.md)** -Methode, um einen Datensatz zum aktuellen Datensatz zu machen, bevor Sie den Klon der Datensatzgruppe verwenden.

Das Anwenden der **[Close](connection-close-method-dao.md)** -Methode auf das ursprüngliche oder das duplizierte Objekt wirkt sich nicht auf das jeweils andere Objekt aus. Angenommen, Sie verwenden **Close** für die ursprüngliche Datensatzgruppe, so wird der Klon nicht geschlossen.


> [!NOTE]
> <UL>
> <LI>
> <P>Wenn Sie den Klon einer Datensatzgruppe in einer ausstehenden Transaktion schließen, wird eine implizite <STRONG>Rollback</STRONG>-Operation verursacht.</P>
> <LI>
> <P>Wenn Sie ein <STRONG>Recordset</STRONG>-Tabellenobjekt in einem Microsoft Access-Arbeitsbereich klonen, wird die <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG>-Eigenschafteneinstellung nicht in die neue Kopie des Recordset geklont. Sie müssen die <STRONG>Index</STRONG>-Eigenschafteneinstellung manuell kopieren.</P></LI></UL>



## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Clone**-Methode zum Erstellen von Kopien einer Datensatzgruppe verwendet. Dann kann der Benutzer den Datensatzzeiger für jede Kopie unabhängig positionieren.

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```