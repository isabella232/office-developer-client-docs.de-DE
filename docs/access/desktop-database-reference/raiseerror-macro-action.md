---
title: RaiseError-Makroaktion
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b706ffed14fdb440f3c3192c7c36015343f2e134
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726036"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="41121-102">RaiseError-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="41121-102">RaiseError macro action</span></span>

<span data-ttu-id="41121-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41121-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="41121-104">Mit der **AuslösenFehler** -Aktion wird eine Ausnahme ausgelöst, die von der **[BeiFehler](onerror-macro-action.md)** -Makroaktion behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="41121-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="41121-105">[!HINWEIS] Die **AuslösenFehler** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41121-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="41121-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="41121-106">Setting</span></span>

<span data-ttu-id="41121-107">Die **AuslösenFehler** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41121-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41121-108">Argument</span><span class="sxs-lookup"><span data-stu-id="41121-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="41121-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="41121-109">Required</span></span></p></th>
<th><p><span data-ttu-id="41121-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41121-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41121-111">Fehlernummer</span><span class="sxs-lookup"><span data-stu-id="41121-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="41121-112">Ja</span><span class="sxs-lookup"><span data-stu-id="41121-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="41121-113">Eine Zahl oder ein Ausdruck, die bzw. der zu einem Long-Datentyp aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="41121-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41121-114">Fehlerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="41121-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="41121-115">Nein</span><span class="sxs-lookup"><span data-stu-id="41121-115">No</span></span></p></td>
<td><p><span data-ttu-id="41121-116">Ein Zeichenfolgenausdruck, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="41121-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="41121-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41121-117">Remarks</span></span>

<span data-ttu-id="41121-118">Bei einem Aufruf der **AuslösenFehler** -Aktion in einem Makroereignis des Typs **[Vor Änderung](before-change-macro-event.md)** oder **[Vor Löschung](before-delete-macro-event.md)** wird das Ereignis abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="41121-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="41121-p101">Wenn keine aktive **BeiFehler** -Anweisung zur Fehlerbehandlung vorhanden ist, wird der von der **AuslösenFehler** -Aktion ausgelöste Fehler der **USysApplicationLog** -Systemtabelle hinzugefügt. Wenn die **AuslösenFehler** -Aktion in der **USysApplicationLog** -Tabelle schreibt, wird die **Kategorie** -Spalte automatisch auf **Ausführung** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="41121-p101">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table. When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="41121-121">Zum Anzeigen der **USysApplicationLog** -Tabelle gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="41121-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="41121-122">Klicken Sie im Menü **Datei** auf, und klicken Sie dann auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="41121-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="41121-123">Klicken Sie im Dialogfeld **Access-Optionen** auf die Registerkarte **Aktuelle Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="41121-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="41121-124">Klicken Sie im Bereich **Navigation** auf **Navigationsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="41121-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="41121-125">Klicken Sie im Dialogfeld **Navigationsoptionen** auf **Systemobjekte anzeigen** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="41121-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="41121-126">Klicken Sie auf **OK**, um das Dialogfeld **Access-Optionen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="41121-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="41121-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="41121-127">Example</span></span>

<span data-ttu-id="41121-128">Das folgende Beispiel veranschaulicht die Auslösenfehler-Aktion verwenden, um das Ereignis vor Änderung Daten Makro abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="41121-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="41121-129">Wenn das Feld AssignedTo aktualisiert wird, wird mit einem NachschlagenDatensatz-Datenblock verwendet, um festzustellen, ob der zugewiesene Techniker eine open Service-Anforderung derzeit zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="41121-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="41121-130">Wenn dies der Fall ist, klicken Sie dann das Ereignis vor Änderung abgebrochen, und der Datensatz nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="41121-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="41121-131">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="41121-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
