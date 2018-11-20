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
ms.openlocfilehash: 24a6bbd951fd19e7fdd25f4f1ab8bd8e9dcd2ade
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026190"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="d733d-102">Makroereignis "Nach Aktualisierung"</span><span class="sxs-lookup"><span data-stu-id="d733d-102">After Update macro event</span></span>

<span data-ttu-id="d733d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d733d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d733d-104">Das Ereignis **Nach Aktualisierung** tritt auf, wenn ein Datensatz geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d733d-104">The **After Update** event occurs after a record is changed.</span></span>

> [!NOTE]
> <span data-ttu-id="d733d-105">[!HINWEIS] Das Ereignis **Nach Aktualisierung** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d733d-105">The **After Update** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="d733d-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d733d-106">Remarks</span></span>

<span data-ttu-id="d733d-p101">Mit dem Ereignis **Nach Aktualisierung** führen Sie sämtliche Aktionen nach dem Ändern eines Datensatzes aus. Häufig wird **Nach Aktualisierung** verwendet, um Geschäftsregeln zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="d733d-p101">Use the **After Update** event to perform any actions that you want to occur when a record is changed. Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="d733d-p102">Mit der Funktion Updated("Feldname") ermitteln Sie, ob ein Feld geändert wurde. Das folgende Codebeispiel zeigt die Verwendung einer If-Anweisung zum Ermitteln, ob das PaidInFull-Feld geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d733d-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="d733d-111">Mit der folgenden Syntax können Sie auf einen vorherigen Wert in einem Feld zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d733d-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="d733d-112">Zugriff auf den vorherigen Wert des QuantityInStock-Felds verwenden Sie beispielsweise die folgende Syntax.</span><span class="sxs-lookup"><span data-stu-id="d733d-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="d733d-113">Am Ende des Ereignisses **Nach Aktualisierung** werden die vorherigen Werte dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d733d-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="d733d-114">In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Nach Aktualisierung** verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d733d-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d733d-115">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="d733d-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="d733d-116">Befehl</span><span class="sxs-lookup"><span data-stu-id="d733d-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d733d-117">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="d733d-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="d733d-118"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="d733d-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-119">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="d733d-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="d733d-120"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="d733d-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-121">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="d733d-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="d733d-122"><a href="if-then-else-macro-block.md">Wenn...Dann...Sonst-Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="d733d-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-123">Datenblock</span><span class="sxs-lookup"><span data-stu-id="d733d-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="d733d-124"><a href="createrecord-data-block.md">DatensatzErstellen-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-124"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-125">Datenblock</span><span class="sxs-lookup"><span data-stu-id="d733d-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="d733d-126"><a href="editrecord-data-block.md">BearbeitenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-126"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-127">Datenblock</span><span class="sxs-lookup"><span data-stu-id="d733d-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="d733d-128"><a href="foreachrecord-data-block.md">FürJedenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-128"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-129">Datenblock</span><span class="sxs-lookup"><span data-stu-id="d733d-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="d733d-130"><a href="lookuprecord-data-block.md">NachschlagenDatensatz-Datenblock</a></span><span class="sxs-lookup"><span data-stu-id="d733d-130"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-131">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-133">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-134"><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-134"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-135">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-136"><a href="deleterecord-macro-action.md">DeleteRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-136"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-137">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-139">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-140"><a href="logevent-macro-action.md">LogEvent-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-140"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-141">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-142"><a href="onerror-macro-action.md">OnError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-142"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-143">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-144"><a href="raiseerror-macro-action.md">RaiseError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-144"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-145">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-146"><a href="rundatamacro-macro-action.md">RunDataMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-146"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-147">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-148"><a href="sendemail-macro-action.md">SendEmail-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-148"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-149">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-150"><a href="setfield-macro-action.md">SetField-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-150"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-151">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-152"><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-152"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d733d-153">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-154"><a href="stopallmacros-macro-action.md">StopAllMacros-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-154"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d733d-155">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="d733d-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d733d-156"><a href="stopmacro-macro-action.md">StopMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="d733d-156"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d733d-157">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Aktualisierung** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="d733d-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="d733d-158">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Aktualisierung** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="d733d-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="d733d-159">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Aktualisierung**.</span><span class="sxs-lookup"><span data-stu-id="d733d-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="d733d-160">Im Makro-Designer wird ein leeres Datenmakro angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d733d-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="d733d-161">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d733d-161">Example</span></span>

<span data-ttu-id="d733d-162">Im folgenden Codebeispiel wird das Ereignis **Nach Aktualisierung** verwendet, um ein benanntes Datenmakro auszuführen, mit dem der Kommentar-Tabelle stets ein Datensatz hinzugefügt wird, wenn der Status eines Problems aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d733d-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="d733d-163">**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, die Sie im Makro-Designer einfügen können.**</span><span class="sxs-lookup"><span data-stu-id="d733d-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="d733d-164">Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="d733d-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="d733d-165">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Aktualisierung** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="d733d-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="d733d-166">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Aktualisierung**.</span><span class="sxs-lookup"><span data-stu-id="d733d-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="d733d-167">Wählen Sie den Code im folgenden Codebeispiel aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d733d-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="d733d-168">Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.</span><span class="sxs-lookup"><span data-stu-id="d733d-168">Activate the macro designer window and then press CTRL+V.</span></span>

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

