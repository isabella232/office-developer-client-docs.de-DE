---
title: Recordset2.AbsolutePosition-Eigenschaft (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 98a401552dfeda9a456a09a144cdd10246a0bc8a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611777"
---
# <a name="recordset2absoluteposition-property-dao"></a>Recordset2.AbsolutePosition-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt die relative Datensatznummer des aktuellen Datensatzes eines **Recordset2**-Objekts fest oder gibt die Nummer zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* .AbsolutePosition

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset2** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.

Da der Wert der **AbsolutePosition**-Eigenschaft auf Null basiert (d. h. der Wert 0 bezieht sich auf den ersten Datensatz im **Recordset2**-Objekt), kann er nicht auf einen Wert gesetzt werden, der größer oder gleich der Anzahl der enthaltenen Datensätze ist. Falls dies geschieht, wird ein auffangbarer Fehler verursacht. Sie können die Anzahl der gefüllten Datensätze im **Recordset2**-Objekt feststellen, indem Sie den Wert der **RecordCount**-Eigenschaft überprüfen. Der maximale Wert der **AbsolutePosition**-Eigenschaft ist der Wert der **RecordCount**-Eigenschaft minus 1.

Wenn kein aktueller Datensatz vorhanden ist, z. B. wenn das **Recordset2-Objekt** keine Datensätze enthält, gibt **AbsolutePosition** –1 zurück. Wenn der aktuelle Datensatz gelöscht wird, wird der **AbsolutePosition-Eigenschaftswert** nicht definiert, und es tritt ein auffangbarer Fehler auf, wenn darauf verwiesen wird. Neue Datensätze werden am Ende der Sequenz hinzugefügt.

Sie sollten diese Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Lesezeichen sind weiterhin die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Möglichkeit, den aktuellen Datensatz in allen Typen von **Recordset2**-Objekten zu positionieren. Die Position eines Datensatzes ändert sich, wenn ein oder mehr vorangehende Datensätze gelöscht werden. Außerdem gibt es keine Gewähr, dass ein Datensatz die gleiche absolute Position hat, wenn das **Recordset2**-Objekt neu erstellt wird, da die Reihenfolge einzelner Datensätze innerhalb eines **Recordset**-Objekts nicht garantiert ist, außer das Objekt wird mit einer SQL-Anweisung unter Verwendung einer ORDER BY-Klausel erstellt.

> [!NOTE]
> - Wenn Sie die **AbsolutePosition**-Eigenschaft für ein soeben geöffnetes und noch nicht aufgefülltes **Recordset2**-Objekt auf einen größeren Wert als Null festlegen, wird ein auffangbarer Fehler verursacht. Füllen Sie das **Recordset2**-Objekt zuerst mit der **MoveLast**-Methode.
> - Die **AbsolutePosition-Eigenschaft** ist für **Recordset2-Objekte** vom "forward-only"-Typ oder für **Recordset2-Objekte,** die aus Pass-Through-Abfragen für ODBC-Datenbanken geöffnet werden, die mit dem Microsoft Access-Datenbankmodul verbunden sind, nicht verfügbar.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die Verarbeitung einer Schleife, die alle Datensätze eines **Recordset2**-Objekts durchläuft, mit der **AbsolutePosition**-Eigenschaft verfolgt.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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
