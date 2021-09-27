---
title: Recordset.Filter-Eigenschaft (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 06/04/2019
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 12cff0909bba1821857ea07b0558c36f8e14c18b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597009"
---
# <a name="recordsetfilter-property-dao"></a>Recordset.Filter-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der die in einem nachfolgend geöffneten **Recordset**-Objekt enthaltenen Datensätze bestimmt, oder gibt diesen Wert zurück (nur für Microsoft Access-Arbeitsbereiche). Lesen/Schreiben **Zeichenfolge**.

## <a name="syntax"></a>Syntax

*Ausdruck*.**Filter**

*Ausdruck* Ein Ausdruck, der ein **Recordset**-Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.

Verwenden Sie die **Filter**-Eigenschaft zum Anwenden eines Filters auf ein **Recordset**-Objekt vom Typ "Dynaset", "Snapshot" oder "Forward-only".

Mit der **Filter**-Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset**-Objekt basierend auf einem vorhandenen **Recordset**-Objekt geöffnet wird.

Verwenden Sie beim Filtern von Feldern mit Datumsangaben das US-amerikanische Datumsformat (Monat-Tag-Jahr), selbst wenn Sie nicht mit der US-Version des Microsoft Access-Datenbankmoduls arbeiten (in diesem Fall müssen Sie alle Datumsangaben durch Verketten von Zeichenfolgen bilden, z. B. strMonth & "-" & strDay & "-" & strYear). Andernfalls werden die Daten möglicherweise nicht wie erwartet gefiltert.

In vielen Fällen geht es schneller, ein neues **Recordset**-Objekt mithilfe einer SQL-Anweisung zu öffnen, die eine WHERE-Klausel enthält.

Wenn Sie die Eigenschaft auf eine Zeichenfolge festlegen, die mit einem Wert verkettet ist, bei dem es sich nicht um eine Ganzzahl handelt, und die Systemparameter ein anderes als das US-amerikanische Dezimaltrennzeichen festlegen, wie etwa ein Komma (Beispiel: strFilter = "PRICE \> " & lngPrice und lngPrice = 125,50), tritt ein Fehler auf, wenn Sie versuchen, das nächste **Recordset**-Objekt zu öffnen. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt das Verwenden der Filter-Eigenschaft zum Ermitteln der Datensätze, die in einem danach geöffneten Recordset enthalten sein sollen.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
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
