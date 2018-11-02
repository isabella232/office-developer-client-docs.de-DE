---
title: Recordset.Clone-Methode (DAO)
TOCTitle: Clone Method
ms:assetid: 50cbc011-7e72-4dee-488d-96e681618e8e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193824(v=office.15)
ms:contentKeyID: 48544802
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052909
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7bce54b0cf7e589641eff35c3cbed2bd54dbe3d2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923000"
---
# <a name="recordsetclone-method-dao"></a>Recordset.Clone-Methode (DAO)


**Betrifft**: Access 2013, Office 2013

Erstellt ein dupliziertes **[Recordset](recordset-object-dao.md)** -Objekt, das auf das ursprüngliche **Recordset** -Objekt verweist.

## <a name="syntax"></a>Syntax

*Ausdruck* . Wenn Sie den Klon

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

### <a name="return-value"></a>Rückgabewert

Recordset

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Clone** -Methode, um mehrere duplizierte **Recordset** -Objekte zu erstellen. Jedes **Recordset** kann einen eigenen aktuellen Datensatz haben. Wenn Sie **Clone** alleine verwenden, werden die Daten in den Objekten oder in den zugrunde liegenden Strukturen nicht geändert. Bei Verwendung der **Clone** -Methode können Sie Lesezeichen zwischen zwei oder mehr **Recordset** -Objekten freigeben, da ihre Lesezeichen austauschbar sind.

Sie können die **Clone** -Methode verwenden, wenn Sie einen Vorgang für ein **Recordset** ausführen möchten, für den mehrere aktuelle Datensätze erforderlich ist. Dies ist schneller und effizienter, als ein zweites **Recordset** zu öffnen. Ein mit der **Clone** -Methode erstelltes **Recordset** hat zunächst keinen aktuellen Datensatz. Um einen Datensatz aktuell zu machen, bevor Sie das **Recordset** klonen, müssen Sie die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft festlegen oder eine der **[Move](recordset-movefirst-method-dao.md)** -Methoden, eine der **[Find](recordset-findfirst-method-dao.md)** -Methoden oder die **[Seek](recordset-seek-method-dao.md)** -Methode verwenden.

Die Anwendung der **[Close](connection-close-method-dao.md)** -Methode auf das ursprüngliche oder das duplizierte Objekt wirkt sich nicht auf das jeweils andere Objekt aus. Wenn Sie z. B. **Close** für das ursprüngliche **Recordset** ausführen, wird der Klon nicht geschlossen.


> [!NOTE]
> <UL>
> <LI>
> <P>Wenn Sie den Klon einer Datensatzgruppe in einer ausstehenden Transaktion schließen, wird eine implizite <STRONG>Rollback</STRONG>-Operation verursacht.</P>
> <LI>
> <P>Wenn Sie ein <STRONG>Recordset</STRONG>-Tabellenobjekt in einem Microsoft Access-Arbeitsbereich klonen, wird die <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG>-Eigenschafteneinstellung nicht in die neue Kopie des Recordset geklont. Sie müssen die <STRONG>Index</STRONG>-Eigenschafteneinstellung manuell kopieren.</P></LI></UL>



## <a name="example"></a>Beispiel

In diesem Beispiel werden mit der **Clone** -Methode Kopien eines **Recordset** erstellt. Anschließend kann der Benutzer den Datensatzzeiger jeder Kopie unabhängig positionieren.

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset 
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
