---
title: Recordset.Filter-Eigenschaft (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 906c3bd9e437ca5fc64067530ecbcaa033ea52d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474042"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="02530-102">Recordset.Filter-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="02530-102">Recordset.Filter Property (DAO)</span></span>

<span data-ttu-id="02530-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="02530-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="02530-p101">Legt einen Wert fest, der die in einem nachfolgend geöffneten **Recordset** -Objekt enthaltenen Datensätze bestimmt, oder gibt diesen Wert zurück (nur Microsoft Access-Arbeitsbereich). Lese-/Schreibzugriff **String**.</span><span class="sxs-lookup"><span data-stu-id="02530-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="02530-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="02530-106">Syntax</span></span>

<span data-ttu-id="02530-107">*Ausdruck* . Filter</span><span class="sxs-lookup"><span data-stu-id="02530-107">*expression* .Filter</span></span>

<span data-ttu-id="02530-108">*Ausdruck* Ein Ausdruck, der ein **Recordset** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="02530-108">*expression* An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="02530-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02530-109">Remarks</span></span>

<span data-ttu-id="02530-110">Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.</span><span class="sxs-lookup"><span data-stu-id="02530-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="02530-111">Verwenden Sie die **Filter** -Eigenschaft, um einen Filter auf ein Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt anwenden.</span><span class="sxs-lookup"><span data-stu-id="02530-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="02530-112">Mit der **Filter** -Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset** -Objekt basierend auf einem vorhandenen **Recordset** -Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="02530-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="02530-113">Verwenden Sie das US-Datumsformat (Monat-Tag-Jahr) Wenn Sie Felder mit Datumsangaben filtern, auch wenn Sie nicht die US-Version von Microsoft Access-Datenbankmodul verwenden (in diesem Fall Sie alle Datumsangaben durch Verketten von Zeichenfolgen, beispielsweise StrMonth zusammensetzen müssen & "-" & StrDay & "-" & erstellen).</span><span class="sxs-lookup"><span data-stu-id="02530-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="02530-114">Andernfalls können die Daten nicht gefiltert werden, wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="02530-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="02530-115">In vielen Fällen geht es schneller, ein neues **Recordset** -Objekt mithilfe einer SQL-Anweisung zu öffnen, die eine WHERE-Klausel enthält.</span><span class="sxs-lookup"><span data-stu-id="02530-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="02530-116">Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Ganzzahl-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrFilter = "PRICE \> " & LngPrice, und LngPrice = 125,50), ein Fehler tritt auf, wenn Sie versuchen, Öffnen Sie das nächste **Recordset-Objekt**.</span><span class="sxs-lookup"><span data-stu-id="02530-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="02530-117">Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-amerikanische Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="02530-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="02530-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="02530-118">Example</span></span>

<span data-ttu-id="02530-119">Das folgende Beispiel zeigt das Verwenden der Filter-Eigenschaft zum Ermitteln der Datensätze, die in einem danach geöffneten Recordset enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="02530-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="02530-120">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="02530-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
