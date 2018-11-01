---
title: Makroereignis 'Vor Änderung'
TOCTitle: Before Change Macro Event
ms:assetid: da456d55-a773-abeb-1fac-ef58e3331cb5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835322(v=office.15)
ms:contentKeyID: 48548077
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm19867
dev_langs:
- xml
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 09188378ff75944f6dc8acccc64b621ea2bca1f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887859"
---
# <a name="before-change-macro-event"></a><span data-ttu-id="7cdc7-102">Makroereignis "Vor Änderung"</span><span class="sxs-lookup"><span data-stu-id="7cdc7-102">Before Change Macro Event</span></span>

<span data-ttu-id="7cdc7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cdc7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7cdc7-104">Das Ereignis **Vor Änderung** tritt ein, wenn ein Datensatz geändert wird, jedoch bevor der Commit für die Änderung erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-104">The **Before Change** event occurs when a record changes, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="7cdc7-105">[!HINWEIS] Das Ereignis **Vor Änderung** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-105">The **Before Change** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cdc7-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7cdc7-106">Remarks</span></span>

<span data-ttu-id="7cdc7-p101">Mit dem Ereignis **Vor Änderung** führen Sie sämtliche Aktionen vor dem Ändern eines Datensatzes aus. Das Ereignis **Vor Änderung** wird häufig verwendet, um Überprüfungen auszuführen und benutzerdefinierte Fehlermeldungen auszugeben.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-p101">Use the **Before Change** event to perform any actions that you want to occur before a record is changed. The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="7cdc7-109">Die **aktualisierte ("der*Name des Felds*")** -Funktion können bestimmen, ob ein Feld geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="7cdc7-110">Im folgenden Codebeispiel wird veranschaulicht, wie eine **If** -Anweisung verwenden, um festzustellen, ob das Feld PaidInFull geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-110">The following code example shows how to use an **If** statement to determine whether the PaidInFull field has been changed.</span></span>

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

<span data-ttu-id="7cdc7-p103">Mit der **IstEingefügt** -Eigenschaft ermitteln Sie, ob das Ereignis **Vor Änderung** durch das Erstellen eines neuen Datensatzes oder eine Änderung an einem vorhandenen Datensatz ausgelöst wurde. Die **IstEingefügt** -Eigenschaft enthält **True**, wenn das Ereignis durch einen neuen Datensatz ausgelöst wurde, und **False**, wenn das Ereignis durch eine Änderung an einem vorhandenen Datensatz ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-p103">Use the **IsInsert** property to determine whether the **Before Change** event was triggered by a new record being created or a change to an existing record. They **IsInsert** property contains **True** if the event was triggered by a new record, **False** if the event was triggered by a change to en existing record.</span></span>

<span data-ttu-id="7cdc7-113">Das folgende Codebeispiel veranschaulicht die Syntax der **IstEingefügt** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-113">The following code example shows the syntax for using the **IsInsert** property.</span></span>

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

<span data-ttu-id="7cdc7-114">Mit der folgenden Syntax können Sie auf einen vorherigen Wert in einem Feld zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-114">You can use access a the previous value in a field by using the following syntax.</span></span>

```vb
    [Old].[Field Name]
```

<span data-ttu-id="7cdc7-115">Zugriff auf den vorherigen Wert des QuantityInStock-Felds verwenden Sie beispielsweise die folgende Syntax.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-115">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

```vb
    [Old].[QuantityInStock]
```

<span data-ttu-id="7cdc7-116">Am Ende des Ereignisses **Vor Änderung** werden die vorherigen Werte dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-116">The previous values are deleted permanently when the **Before Change** event ends.</span></span>

<span data-ttu-id="7cdc7-p104">Mit der **AuslösenFehler** -Aktion können Sie das Ereignis **Vor Änderung** abbrechen. Bei einem Fehler werden die Änderungen im Ereignis **Vor Änderung** verworfen.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-p104">You can cancel the **Before Change** event by using the **RaiseError** action. When an error is raised the changes contained in the **Before Change** event are discarded.</span></span>

<span data-ttu-id="7cdc7-119">In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Vor Änderung** verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-119">The following table lists macro commands that can be used in the**Before Change** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cdc7-120">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="7cdc7-120">Command Type</span></span></p></th>
<th><p><span data-ttu-id="7cdc7-121">Command</span><span class="sxs-lookup"><span data-stu-id="7cdc7-121">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cdc7-122">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="7cdc7-122">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-123"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-123"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cdc7-124">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="7cdc7-124">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-125"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-125"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cdc7-126">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="7cdc7-126">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-127"><a href="if-then-else-macro-block.md">If... Im Anschluss: Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-127"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cdc7-128">Datenblock</span><span class="sxs-lookup"><span data-stu-id="7cdc7-128">Data Block</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-129"><a href="lookuprecord-data-block.md">NachschlagenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-129"><a href="lookuprecord-data-block.md">LookupRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cdc7-130">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="7cdc7-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-131"><a href="clearmacroerror-macro-action.md">Löschenmakrofehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-131"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cdc7-132">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="7cdc7-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-133"><a href="onerror-macro-action.md">BeiFehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-133"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cdc7-134">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="7cdc7-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-135"><a href="raiseerror-macro-action.md">Auslösenfehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-135"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cdc7-136">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="7cdc7-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-137"><a href="setfield-macro-action.md">SetField-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-137"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cdc7-138">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="7cdc7-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-139"><a href="setlocalvar-macro-action.md">FestlegenLokaleVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-139"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cdc7-140">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="7cdc7-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7cdc7-141"><a href="stopmacro-macro-action.md">StoppMakro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="7cdc7-141"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7cdc7-142">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Vor Änderung** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-142">To create a Data Macro that captures the **Before Change** event, use the following steps:</span></span>

1.  <span data-ttu-id="7cdc7-143">Öffnen Sie die Tabelle, für die Sie das Ereignis **Vor Änderung** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-143">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="7cdc7-144">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Vorabereignisse** auf **Vor Änderung**.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-144">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

<span data-ttu-id="7cdc7-145">Im Makro-Designer wird ein leeres Datenmakro angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-145">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="7cdc7-146">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7cdc7-146">Example</span></span>

<span data-ttu-id="7cdc7-147">Im folgenden Codebeispiel wird wird das Ereignis **Vor Änderung** verwendet, um die Felder Status überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-147">The following code example uses the **Before Change** event to validate the Status fields.</span></span> <span data-ttu-id="7cdc7-148">Ein Fehler wird ausgelöst, wenn ein ungültiger Wert in das Feld Auflösung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-148">An error is raised if an inappropriate value is contained in the Resolution field.</span></span>

```vb 
 
/* Check to ensure that if the bug is resloved that the user has selected a resolution      */ 
If   [Status]="3 - Resolved" And IsNull([Resolution])   Then 
 
     RaiseError 
             Error Number   1 
        Error Description   You must select a resolution. 
End If 
 
/* Check to ensure that if a bug is closed that the user has selected a resolution first     */ 
If   [Status]="4 - Closed" And IsNull([Resolution])   Then 
 
      RaiseError 
             Error Number   2 
        Error Description   An issue must be resolved before it can be closed. 
End If 
 
If   [Status]<>"3 - Resolved" And [Status]<>"4 - Closed"   Then 
 
      SetField 
             Name   Resolution 
            Value   =Null 
End If 
 
```

<span data-ttu-id="7cdc7-149">Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="7cdc7-149">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="7cdc7-150">Öffnen Sie die Tabelle, für die Sie das Ereignis **Vor Änderung** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-150">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="7cdc7-151">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Vorabereignisse** auf **Vor Änderung**.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-151">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

3.  <span data-ttu-id="7cdc7-152">Wählen Sie den Code im folgenden Codebeispiel wird ein, und drücken Sie **STRG + C** , um ihn in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-152">Select the code in the following code example and then press **CTRL+C** to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="7cdc7-153">Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie **STRG + V**.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-153">Activate the macro designer window and then press **CTRL+V**.</span></span>



```xml
<DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
  <DataMacro Event="BeforeChange"> 
    <Statements> 
      <Comment>Check to ensure that if the bug is resloved that the user has selected a resolution </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="3 - Resolved" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">1</Argument> 
              <Argument Name="Description">You must select a resolution.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <Comment>Check to ensure that if a bug is closed that the user has selected a resolution first </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="4 - Closed" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">2</Argument> 
              <Argument Name="Description">An issue must be resolved before it can be closed.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]&lt;&gt;"3 - Resolved" And [Status]&lt;&gt;"4 - Closed"</Condition> 
          <Statements> 
            <Action Name="SetField"> 
              <Argument Name="Field">Resolution</Argument> 
              <Argument Name="Value">Null</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
    </Statements> 
  </DataMacro> 
</DataMacros>
```

<span data-ttu-id="7cdc7-154">Das folgende Beispiel veranschaulicht die Auslösenfehler-Aktion verwenden, um das Ereignis vor Änderung Daten Makro abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-154">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="7cdc7-155">Wenn das Feld AssignedTo aktualisiert wird, wird mit einem NachschlagenDatensatz-Datenblock verwendet, um festzustellen, ob der zugewiesene Techniker eine open Service-Anforderung derzeit zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-155">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="7cdc7-156">Wenn dies der Fall ist, klicken Sie dann das Ereignis vor Änderung abgebrochen, und der Datensatz nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7cdc7-156">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="7cdc7-157">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="7cdc7-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
