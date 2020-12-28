---
title: Nachschlagendatensatz-Datenblock
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734210"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="6dd1c-102">Nachschlagendatensatz-Datenblock</span><span class="sxs-lookup"><span data-stu-id="6dd1c-102">LookupRecord data block</span></span>

<span data-ttu-id="6dd1c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dd1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6dd1c-104">Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="6dd1c-105">Der **NachschlagenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="6dd1c-106">Setting</span><span class="sxs-lookup"><span data-stu-id="6dd1c-106">Setting</span></span>

<span data-ttu-id="6dd1c-107">Die **NachschlagenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6dd1c-108">Argument</span><span class="sxs-lookup"><span data-stu-id="6dd1c-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="6dd1c-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6dd1c-109">Required</span></span></p></th>
<th><p><span data-ttu-id="6dd1c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dd1c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dd1c-111">In</span><span class="sxs-lookup"><span data-stu-id="6dd1c-111">In</span></span></p></td>
<td><p><span data-ttu-id="6dd1c-112">Ja</span><span class="sxs-lookup"><span data-stu-id="6dd1c-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="6dd1c-113">Eine Zeichenfolge, die den Datensatz bezeichnet, für den eine Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="6dd1c-114">Das <em>in</em> -Argument kann den Namen der Tabelle, eine SELECT-Abfrage oder eine SQL-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="6dd1c-115"><strong>Hinweis</strong>: der angegebene Datensatz darf keine Daten enthalten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd1c-116">Bedingung</span><span class="sxs-lookup"><span data-stu-id="6dd1c-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="6dd1c-117">Nein</span><span class="sxs-lookup"><span data-stu-id="6dd1c-117">No</span></span></p></td>
<td><p><span data-ttu-id="6dd1c-118">Ein Zeichenfolgenausdruck, der verwendet wird, um den Datenbereich einzuschränken, für den der <strong>nachschlagendatensatz</strong> -Datenblock ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="6dd1c-119">Beispielsweise entsprechen Kriterien häufig der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort WHERE.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="6dd1c-120">Wenn Kriterien ausgelassen werden, funktioniert der <strong>nachschlagendatensatz</strong> -Datenblock für die gesamte Domäne, die durch das Argument <em>in</em> angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="6dd1c-121">Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in <em>in</em>sein.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dd1c-122">Alias</span><span class="sxs-lookup"><span data-stu-id="6dd1c-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="6dd1c-123">Nein</span><span class="sxs-lookup"><span data-stu-id="6dd1c-123">No</span></span></p></td>
<td><p><span data-ttu-id="6dd1c-124">Eine Zeichenfolge, die einen alternativen Namen für den durch das <em>in</em> -Argument angegebenen Datensatz bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="6dd1c-125">Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="6dd1c-126">Wenn <em>Alias</em> nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6dd1c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dd1c-127">Remarks</span></span>

<span data-ttu-id="6dd1c-128">Wenn die durch die Argumente *in* und *WHERE Bedingung* angegebenen Kriterien mehr als einen Datensatz zurückgeben, wird der **nachschlagendatensatz** -Datenblock nur für den ersten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-128">If the criteria specified by the *In* and *Where Condition* arguments returns more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>  <span data-ttu-id="6dd1c-129">Wenn keine Datensätze mit den angegebenen Kriterien übereinstimmen, springt Access über die Gruppe von Aktionen, die im **nachschlagendatensatz** -Block enthalten sind, als ob es sich um einen **[if](if-then-else-macro-block.md)** -Makroblock Ausdruck handelt, der als false ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-129">In the case that no records match the specified criteria, Access will skip over the set of actions contained within the **LookupRecord** block, as if it had been an **[If](if-then-else-macro-block.md)** macro block expression that evaluated as false.</span></span>

## <a name="example"></a><span data-ttu-id="6dd1c-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6dd1c-130">Example</span></span>

<span data-ttu-id="6dd1c-131">Im folgenden Beispiel wird gezeigt, wie Sie mit der SetReturnVar-Aktion einen Wert aus einem benannten datenmakro zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-131">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="6dd1c-132">Ein ReturnVar mit dem Namen **CurrentServiceRequest** wird an das Makro oder Visual Basic for Applications (VBA) Unterroutine zurückgegeben, die das benannte datenmakro aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-132">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="6dd1c-133">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6dd1c-133">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="6dd1c-134">Im folgenden Beispiel wird gezeigt, wie Sie mit der auslösenfehler-Aktion das makroereignis vor Änderungsdaten abbrechen.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-134">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="6dd1c-135">Wenn das Feld AssignedTo aktualisiert wird, wird ein nachschlagendatensatz-Datenblock verwendet, um zu bestimmen, ob der zugewiesene Techniker derzeit einer offenen Dienstanforderung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-135">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="6dd1c-136">Wenn dies der Fall ist, wird das Before Change-Ereignis abgebrochen, und der Datensatz wird nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-136">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

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
