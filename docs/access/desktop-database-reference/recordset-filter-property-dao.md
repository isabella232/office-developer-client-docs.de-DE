---
title: Recordset.Filter-Eigenschaft (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 06/04/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 43afbfda8c560eafb90e6a53d85207e19e5b1170
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675750"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="d178b-102">Recordset.Filter-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="d178b-102">Recordset.Filter property (DAO)</span></span>

<span data-ttu-id="d178b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d178b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d178b-104">Legt einen Wert fest, der feststellt, welche Datensätze in einem nachfolgend geöffneten **Recordset**-Objekt einbezogen werden, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="d178b-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="d178b-105">**Zeichenfolge** mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d178b-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d178b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d178b-106">Syntax</span></span>

<span data-ttu-id="d178b-107">*Ausdruck*.**Filter**</span><span class="sxs-lookup"><span data-stu-id="d178b-107">expression .Filter</span></span>

<span data-ttu-id="d178b-108">*Ausdruck* Ein Ausdruck, der ein **Recordset**-Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d178b-108">*expression* An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d178b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d178b-109">Remarks</span></span>

<span data-ttu-id="d178b-110">Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.</span><span class="sxs-lookup"><span data-stu-id="d178b-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="d178b-111">Verwenden Sie die **Filter**-Eigenschaft zum Anwenden eines Filters auf ein **Recordset**-Objekt vom Typ "Dynaset", "Snapshot" oder "Forward-only".</span><span class="sxs-lookup"><span data-stu-id="d178b-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="d178b-112">Mit der **Filter**-Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset**-Objekt basierend auf einem vorhandenen **Recordset**-Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d178b-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="d178b-113">Verwenden Sie beim Filtern von Feldern mit Datumsangaben das US-amerikanische Datumsformat (Monat-Tag-Jahr), selbst wenn Sie nicht mit der US-Version des Microsoft Access-Datenbankmoduls arbeiten (in diesem Fall müssen Sie alle Datumsangaben durch Verketten von Zeichenfolgen bilden, z. B. strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="d178b-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="d178b-114">Andernfalls werden die Daten möglicherweise nicht wie erwartet gefiltert.</span><span class="sxs-lookup"><span data-stu-id="d178b-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="d178b-115">In vielen Fällen geht es schneller, ein neues **Recordset**-Objekt mithilfe einer SQL-Anweisung zu öffnen, die eine WHERE-Klausel enthält.</span><span class="sxs-lookup"><span data-stu-id="d178b-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="d178b-116">Wenn Sie die Eigenschaft auf eine Zeichenfolge festlegen, die mit einem Wert verkettet ist, bei dem es sich nicht um eine Ganzzahl handelt, und die Systemparameter ein anderes als das US-amerikanische Dezimaltrennzeichen festlegen, wie etwa ein Komma (Beispiel: strFilter = "PRICE \> " & lngPrice und lngPrice = 125,50), tritt ein Fehler auf, wenn Sie versuchen, das nächste **Recordset**-Objekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d178b-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="d178b-117">Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d178b-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="d178b-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d178b-118">Example</span></span>

<span data-ttu-id="d178b-119">Das folgende Beispiel zeigt das Verwenden der Filter-Eigenschaft zum Ermitteln der Datensätze, die in einem danach geöffneten Recordset enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="d178b-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="d178b-120">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d178b-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
