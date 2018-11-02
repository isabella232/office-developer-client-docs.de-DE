---
title: Makroereignis "Nach Aktualisierung"
TOCTitle: After Update macro event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 237b3633ab70bcdbe84ce52f7d25b2203091cb1e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919136"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="809ca-102">Makroereignis "Nach Aktualisierung"</span><span class="sxs-lookup"><span data-stu-id="809ca-102">After Update macro event</span></span>


<span data-ttu-id="809ca-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="809ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="809ca-104">Das Ereignis **Nach Aktualisierung** tritt auf, wenn ein Datensatz geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="809ca-104">The **After Update** event occurs after a record is changed.</span></span>


> [!NOTE]
> <span data-ttu-id="809ca-105">[!HINWEIS] Das Ereignis **Nach Aktualisierung** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="809ca-105">The **After Update** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="809ca-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809ca-106">Remarks</span></span>

<span data-ttu-id="809ca-p101">Mit dem Ereignis **Nach Aktualisierung** führen Sie sämtliche Aktionen nach dem Ändern eines Datensatzes aus. Häufig wird **Nach Aktualisierung** verwendet, um Geschäftsregeln zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="809ca-p101">Use the **After Update** event to perform any actions that you want to occur when a record is changed. Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="809ca-p102">Mit der Funktion Updated("Feldname") ermitteln Sie, ob ein Feld geändert wurde. Das folgende Codebeispiel zeigt die Verwendung einer If-Anweisung zum Ermitteln, ob das PaidInFull-Feld geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="809ca-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="809ca-111">Mit der folgenden Syntax können Sie auf einen vorherigen Wert in einem Feld zugreifen.</span><span class="sxs-lookup"><span data-stu-id="809ca-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="809ca-112">Zugriff auf den vorherigen Wert des QuantityInStock-Felds verwenden Sie beispielsweise die folgende Syntax.</span><span class="sxs-lookup"><span data-stu-id="809ca-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="809ca-113">Am Ende des Ereignisses **Nach Aktualisierung** werden die vorherigen Werte dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="809ca-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="809ca-114">In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Nach Aktualisierung** verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="809ca-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="809ca-115">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="809ca-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="809ca-116">Command</span><span class="sxs-lookup"><span data-stu-id="809ca-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="809ca-117">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="809ca-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="809ca-118"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="809ca-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-119">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="809ca-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="809ca-120"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="809ca-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-121">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="809ca-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="809ca-122"><a href="if-then-else-macro-block.md">Wenn...Dann...Sonst-Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="809ca-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-123">Datenblock</span><span class="sxs-lookup"><span data-stu-id="809ca-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="809ca-124"><a href="createrecord-data-block.md">DatensatzErstellen-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-124"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-125">Datenblock</span><span class="sxs-lookup"><span data-stu-id="809ca-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="809ca-126"><a href="editrecord-data-block.md">BearbeitenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-126"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-127">Datenblock</span><span class="sxs-lookup"><span data-stu-id="809ca-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="809ca-128"><a href="foreachrecord-data-block.md">FürJedenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-128"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-129">Datenblock</span><span class="sxs-lookup"><span data-stu-id="809ca-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="809ca-130"><a href="lookuprecord-data-block.md">NachschlagenDatensatz-Datenblock</a></span><span class="sxs-lookup"><span data-stu-id="809ca-130"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-131">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-133">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-134"><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-134"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-135">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-136"><a href="deleterecord-macro-action.md">DeleteRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-136"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-137">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-139">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-140"><a href="logevent-macro-action.md">LogEvent-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-140"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-141">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-142"><a href="onerror-macro-action.md">OnError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-142"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-143">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-144"><a href="raiseerror-macro-action.md">RaiseError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-144"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-145">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-146"><a href="rundatamacro-macro-action.md">RunDataMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-146"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-147">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-148"><a href="sendemail-macro-action.md">SendEmail-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-148"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-149">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-150"><a href="setfield-macro-action.md">SetField-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-150"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-151">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-152"><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-152"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="809ca-153">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-154"><a href="stopallmacros-macro-action.md">StopAllMacros-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-154"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809ca-155">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="809ca-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="809ca-156"><a href="stopmacro-macro-action.md">StopMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="809ca-156"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="809ca-157">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Aktualisierung** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="809ca-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="809ca-158">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Aktualisierung** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="809ca-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="809ca-159">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Aktualisierung**.</span><span class="sxs-lookup"><span data-stu-id="809ca-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="809ca-160">Im Makro-Designer wird ein leeres Datenmakro angezeigt.</span><span class="sxs-lookup"><span data-stu-id="809ca-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="809ca-161">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809ca-161">Example</span></span>

<span data-ttu-id="809ca-162">Im folgenden Codebeispiel wird das Ereignis **Nach Aktualisierung** verwendet, um ein benanntes Datenmakro auszuführen, mit dem der Kommentar-Tabelle stets ein Datensatz hinzugefügt wird, wenn der Status eines Problems aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="809ca-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="809ca-163">**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, die Sie im Makro-Designer einfügen können.**</span><span class="sxs-lookup"><span data-stu-id="809ca-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="809ca-164">Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="809ca-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="809ca-165">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Aktualisierung** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="809ca-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="809ca-166">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Aktualisierung**.</span><span class="sxs-lookup"><span data-stu-id="809ca-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="809ca-167">Wählen Sie den Code im folgenden Codebeispiel aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="809ca-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="809ca-168">Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.</span><span class="sxs-lookup"><span data-stu-id="809ca-168">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterUpdate"> 
        <Statements> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Status")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Status changed to &quot; &amp; [Status]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Resolution")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Issue resolved as &quot; &amp; [Resolution]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
``` 

<br/>

```vb
If  Updated("Status")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
         prmComment   ="--Status Changes to "&[Status] 
          prmUserID   =[ChangedByUserID] 
End If 
 
If   Updated("Resolution")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
          prmUserID   =[ChangedByUserID] 
         prmComment   ="--Issue Resolved as "&[Status] 
End If 
```

