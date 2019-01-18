---
title: Recordset.Filter-Eigenschaft (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 7ab090dd6cf0b6e2676cf05907ac77c438f22652
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711707"
---
# <a name="recordsetfilter-property-dao"></a>Recordset.Filter-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der die in einem nachfolgend geöffneten **Recordset** -Objekt enthaltenen Datensätze bestimmt, oder gibt diesen Wert zurück (nur Microsoft Access-Arbeitsbereich). Lese-/Schreibzugriff **String**.

## <a name="syntax"></a>Syntax

*Ausdruck* . Filter

*Ausdruck* Ein Ausdruck, der ein **Recordset** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.

Verwenden Sie die **Filter** -Eigenschaft, um einen Filter auf ein Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt anwenden.

Mit der **Filter** -Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset** -Objekt basierend auf einem vorhandenen **Recordset** -Objekt geöffnet wird.

Verwenden Sie das US-Datumsformat (Monat-Tag-Jahr) Wenn Sie Felder mit Datumsangaben filtern, auch wenn Sie nicht die US-Version von Microsoft Access-Datenbankmodul verwenden (in diesem Fall Sie alle Datumsangaben durch Verketten von Zeichenfolgen, beispielsweise StrMonth & zusammensetzen müssen "-" _ aMP_ StrDay & "-" & erstellen). Andernfalls können die Daten nicht gefiltert werden, wie erwartet.

In vielen Fällen geht es schneller, ein neues **Recordset** -Objekt mithilfe einer SQL-Anweisung zu öffnen, die eine WHERE-Klausel enthält.

Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Ganzzahl-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrFilter = "PRICE \> " &-LngPrice und LngPrice = 125,50), ein Fehler tritt auf, wenn Sie versuchen, Öffnen Sie das nächste **Recordset-Objekt**. Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-amerikanische Dezimalzeichen akzeptiert.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt das Verwenden der Filter-Eigenschaft zum Ermitteln der Datensätze, die in einem danach geöffneten Recordset enthalten sein sollen.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```
