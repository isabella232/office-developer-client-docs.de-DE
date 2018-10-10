---
title: Recordset.AbsolutePosition-Eigenschaft (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0140fc9895ae879296236161aee6776f9dbd850c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472869"
---
# <a name="recordsetabsoluteposition-property-dao"></a>Recordset.AbsolutePosition-Eigenschaft (DAO)

**Betrifft**: Access 2013 | Office 2013

Legt die relative Datensatznummer des aktuellen Datensatzes eines **Recordset** -Objekts fest oder gibt den betreffenden Wert zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . AbsolutePosition

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Hinweise

Sie können die **AbsolutePosition** -Eigenschaft verwenden, um den aktuellen Datensatzzeiger basierend auf seiner Position in einem **Recordset** -Objekt vom Typ Dynaset oder Momentaufnahme auf einen bestimmten Datensatz zu verschieben. Sie können auch die aktuelle Datensatznummer ermitteln, indem Sie die Einstellung der **AbsolutePosition** -Eigenschaft überprüfen.

Da es sich bei der **AbsolutePosition** -Eigenschaft um einen nullbasierten Wert handelt (d. h. die Einstellung 0 verweist auf den ersten Datensatz im **Recordset** -Objekt), können Sie keinen Wert festlegen, der größer oder gleich der Anzahl von im enthaltenen Datensätzen ist. Falls Sie das versuchen, tritt ein abfangbarer Fehler auf. Ermitteln Sie die Anzahl von im **Recordset** -Objekt enthaltenen Datensätzen, indem Sie die Einstellung der **RecordCount** -Eigenschaft überprüfen. Die maximal zulässige Einstellung für die **AbsolutePosition** -Eigenschaft entspricht dem Wert der **RecordCount** -Eigenschaft minus 1.

Wenn kein aktueller Datensatz vorhanden ist, als wenn keine Datensätze im **Recordset** -Objekt vorhanden sind, gibt **AbsolutePosition** -1 zurück. Wenn der aktuelle Datensatz gelöscht wird, der Wert der **AbsolutePosition** -Eigenschaft ist nicht definiert, und wenn auf sie verwiesen wird, tritt ein auffangbarer Fehler auf. Neue Datensätze werden am Ende der Sequenz hinzugefügt.

Verwenden Sie diese Eigenschaft nicht als Ersatz-Datensatznummer. Textmarken sind weiterhin die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Methode der Positionierung für alle Typen von **Recordset** -Objekten. Die Position eines Datensatzes ändert sich insbesondere dann, wenn einer oder mehrere vorausgehende Datensätze gelöscht werden. Außerdem kann nicht davon ausgegangen werden, dass ein bestimmter Datensatz beim erneuten Erstellen des **Recordset** -Objekts die gleiche absolute Position aufweist. Denn die Reihenfolge einzelner Datensätze in einem **Recordset** -Objekt ist nur dann sichergestellt, wenn es in einer SQL-Anweisung mit einer ORDER BY-Klausel erstellt wird.

> [!NOTE]
> - Wird die **AbsolutePosition**-Eigenschaft bei einem neu geöffneten, jedoch leeren **Recordset**-Objekt auf einen Wert größer als Null festgelegt, tritt ein abfangbarer Fehler auf. Füllen Sie das **Recordset**-Objekt zuerst mit der **MoveLast**-Methode auf.
> - Die **AbsolutePosition**-Eigenschaft ist bei **Recordset**-Objekten des Typs Vorwärts nicht verfügbar. Sie ist auch bei **Recordset**-Objekten nicht verfügbar, die von Pass-Through-Abfragen zu ODBC-Datenbanken, die mit dem Microsoft Access-Datenbankmodul verbunden sind, geöffnet werden.

## <a name="example"></a>Beispiel

Dieses Beispiel verwendet die **AbsolutePosition** -Eigenschaft, um den Status einer Schleife nachzuverfolgen, in der alle Datensätze eines **Recordset** -Objekts aufgezählt werden.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
