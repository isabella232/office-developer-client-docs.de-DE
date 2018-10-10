---
title: NachschlagenDatensatz-Datenblock
TOCTitle: LookupRecord Data Block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd0db6e818ab79fc124760509d07d60b954d49e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474730"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="2abb6-102">NachschlagenDatensatz-Datenblock</span><span class="sxs-lookup"><span data-stu-id="2abb6-102">LookupRecord Data Block</span></span>

<span data-ttu-id="2abb6-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2abb6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2abb6-104">Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2abb6-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="2abb6-105">[!HINWEIS] Der **NachschlagenDatensatz** -Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2abb6-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="2abb6-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2abb6-106">Setting</span></span>

<span data-ttu-id="2abb6-107">Die **NachschlagenDatensatz** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2abb6-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2abb6-108">Argument</span><span class="sxs-lookup"><span data-stu-id="2abb6-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="2abb6-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="2abb6-109">Required</span></span></p></th>
<th><p><span data-ttu-id="2abb6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2abb6-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2abb6-111">In</span><span class="sxs-lookup"><span data-stu-id="2abb6-111">In</span></span></p></td>
<td><p><span data-ttu-id="2abb6-112">Ja</span><span class="sxs-lookup"><span data-stu-id="2abb6-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="2abb6-113">Eine Zeichenfolge, die den Datensatz für den Betrieb identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2abb6-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="2abb6-114">Das <em>im</em> Argument kann der Name der Tabelle, einer select-Abfrage oder eine SQL-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="2abb6-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p>

> [!NOTE]
> <span data-ttu-id="2abb6-115">Der angegebene Datensatz darf keine Daten enthalten, die in einer verknüpften Tabelle oder einer ODBC-Datenquelle gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="2abb6-115">The specified record cannot include data stored in a linked table or ODBC data source.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2abb6-116">Bedingung</span><span class="sxs-lookup"><span data-stu-id="2abb6-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="2abb6-117">Nein</span><span class="sxs-lookup"><span data-stu-id="2abb6-117">No</span></span></p></td>
<td><p><span data-ttu-id="2abb6-118">Ein Zeichenfolgenausdruck, der zum Einschränken des Bereichs der Daten auf dem des <strong>NachschlagenDatensatz</strong> -Datenblocks wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2abb6-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="2abb6-119">Häufig sind beispielsweise Kriterien entspricht der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort, in dem.</span><span class="sxs-lookup"><span data-stu-id="2abb6-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="2abb6-120">Wenn Kriterien Length angegeben werden, wirkt sich auf die gesamte Domäne, die durch das Argument <em>im</em> angegebenen <strong>NachschlagenDatensatz</strong> -Datenblock.</span><span class="sxs-lookup"><span data-stu-id="2abb6-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="2abb6-121">Jedes Feld, das im Argument Kriterien enthalten ist, muss auch ein Feld in <em>In</em>sein.</span><span class="sxs-lookup"><span data-stu-id="2abb6-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2abb6-122">Alias</span><span class="sxs-lookup"><span data-stu-id="2abb6-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="2abb6-123">Nein</span><span class="sxs-lookup"><span data-stu-id="2abb6-123">No</span></span></p></td>
<td><p><span data-ttu-id="2abb6-124">Eine Zeichenfolge, die einen alternativen Namen für den durch das Argument <em>im</em> angegebenen Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="2abb6-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="2abb6-125">Häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu verhindern, dass mögliche mehrdeutige Verweise zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="2abb6-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="2abb6-126">Wenn <em>Alias</em> nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</span><span class="sxs-lookup"><span data-stu-id="2abb6-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2abb6-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2abb6-127">Remarks</span></span>

<span data-ttu-id="2abb6-128">Wenn die durch die Argumente *In* und *Bedingung* angegebenen Kriterien mehrere Datensätze angegeben ist, wird das **NachschlagenDatensatz** -Datenblock nur für den ersten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2abb6-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="2abb6-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2abb6-129">Example</span></span>

<span data-ttu-id="2abb6-130">Das folgende Beispiel veranschaulicht die SetReturnVar-Aktion verwenden, um einen Wert aus ein benanntes Datenmakro zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="2abb6-130">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="2abb6-131">Eine mit dem Namen **CurrentServiceRequest** ReturnVar wird an das Makro oder Visual Basic für Applikationen (VBA) Unterroutine zurückgegeben, die das benanntes Datenmakro aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2abb6-131">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="2abb6-132">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="2abb6-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```

<br/>

<span data-ttu-id="2abb6-133">Das folgende Beispiel veranschaulicht die Auslösenfehler-Aktion verwenden, um das Ereignis vor Änderung Daten Makro abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="2abb6-133">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="2abb6-134">Wenn das Feld AssignedTo aktualisiert wird, wird mit einem NachschlagenDatensatz-Datenblock verwendet, um festzustellen, ob der zugewiesene Techniker eine open Service-Anforderung derzeit zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="2abb6-134">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="2abb6-135">Wenn dies der Fall ist, wird das Ereignis vor Änderung abgebrochen, und der Datensatz nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2abb6-135">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
