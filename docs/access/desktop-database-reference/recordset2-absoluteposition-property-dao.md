---
title: Recordset2.AbsolutePosition Property (DAO)
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
ms.openlocfilehash: 4f521daab352e090c52fd7a94bdd28abb0e34291
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475032"
---
# <a name="recordset2absoluteposition-property-dao"></a>Recordset2.AbsolutePosition Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Legt die relative Datensatznummer des aktuellen Datensatzes eines **Recordset2**-Objekts fest oder gibt die Nummer zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . AbsolutePosition

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Mit der AbsolutePosition-Eigenschaft können Sie den aktuellen Datensatzzeiger basierend auf seiner Ordnungsposition in einem Recordset2-Objekt vom Typ Dynaset oder Momentaufnahme auf einen bestimmten Datensatz festlegen. Sie können die aktuelle Datensatznummer auch feststellen, indem Sie die AbsolutePosition-Eigenschaft überprüfen.

Da der Wert der **AbsolutePosition**-Eigenschaft auf Null basiert (d. h. der Wert 0 bezieht sich auf den ersten Datensatz im **Recordset2**-Objekt), kann er nicht auf einen Wert gesetzt werden, der größer oder gleich der Anzahl der enthaltenen Datensätze ist. Falls dies geschieht, wird ein auffangbarer Fehler verursacht. Sie können die Anzahl der gefüllten Datensätze im **Recordset2**-Objekt feststellen, indem Sie den Wert der **RecordCount**-Eigenschaft überprüfen. Der maximale Wert der **AbsolutePosition**-Eigenschaft ist der Wert der **RecordCount**-Eigenschaft minus 1.

Wenn kein aktueller Datensatz vorhanden ist, als wenn im **Recordset2** -Objekt keine Datensätze vorhanden sind, gibt **AbsolutePosition** -1 zurück. Wenn der aktuelle Datensatz gelöscht wird, der Wert der **AbsolutePosition** -Eigenschaft ist nicht definiert, und wenn auf sie verwiesen wird, tritt ein auffangbarer Fehler auf. Neue Datensätze werden am Ende der Sequenz hinzugefügt.

Sie sollten diese Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Lesezeichen sind weiterhin die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Möglichkeit, den aktuellen Datensatz in allen Typen von **Recordset2**-Objekten zu positionieren. Die Position eines Datensatzes ändert sich, wenn ein oder mehr vorangehende Datensätze gelöscht werden. Außerdem gibt es keine Gewähr, dass ein Datensatz die gleiche absolute Position hat, wenn das **Recordset2**-Objekt neu erstellt wird, da die Reihenfolge einzelner Datensätze innerhalb eines **Recordset**-Objekts nicht garantiert ist, außer das Objekt wird mit einer SQL-Anweisung unter Verwendung einer ORDER BY-Klausel erstellt.


> [!NOTE]
> <UL>
> <LI>
> <P>Wenn Sie die <STRONG>AbsolutePosition</STRONG>-Eigenschaft für ein soeben geöffnetes und noch nicht aufgefülltes <STRONG>Recordset2</STRONG>-Objekt auf einen größeren Wert als Null festlegen, wird ein auffangbarer Fehler verursacht. Füllen Sie das <STRONG>Recordset2</STRONG>-Objekt zuerst mit der <STRONG>MoveLast</STRONG>-Methode.</P>
> <LI>
> <P>Die <STRONG>AbsolutePosition</STRONG> -Eigenschaft ist nicht verfügbar, auf Forward Typ <STRONG>Recordset2</STRONG> -Objekte oder auf <STRONG>Recordset2</STRONG> -Objekte, die von Pass-Through-Abfragen für Microsoft Access-Datenbankmodul verbundene ODBC-Datenbanken geöffnet.</P></LI></UL>



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