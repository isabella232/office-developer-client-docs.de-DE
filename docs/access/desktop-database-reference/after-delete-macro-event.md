---
title: Makroereignis "Nach Löschvorgang"
TOCTitle: After Delete macro event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f524a544736f68bcfa6bd15e3bcc720ffa2bc4d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297214"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="9586d-102">Makroereignis "Nach Löschvorgang"</span><span class="sxs-lookup"><span data-stu-id="9586d-102">After Delete macro event</span></span>

<span data-ttu-id="9586d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9586d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9586d-104">Das Ereignis **Nach Löschvorgang** tritt auf, nachdem ein Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="9586d-104">The **After Delete** event occurs after a record is deleted.</span></span>

> [!NOTE]
> <span data-ttu-id="9586d-105">Das Ereignis **Nach Löschvorgang** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9586d-105">The **After Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="9586d-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9586d-106">Remarks</span></span>

<span data-ttu-id="9586d-p101">Mit dem Ereignis **Nach Löschvorgang** führen Sie sämtliche Aktionen nach dem Löschen eines Datensatzes aus. Häufig wird **Nach Löschvorgang** verwendet, um Geschäftsregeln und Workflows zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="9586d-p101">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted. Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="9586d-109">Wenn das Ereignis **Nach Löschvorgang** aufgetreten ist, bleiben die im gelöschten Datensatz enthaltenen Werte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9586d-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="9586d-110">Möglicherweise möchten Sie einen gelöschten Wert verwenden, um eine Summe zu erhöhen oder zu dekrementieren, einen Überwachungspfad zu erstellen oder mit einem vorhandenen Wert in einem *Bedingung* -Argument zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="9586d-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="9586d-111">Sie können die **aktualisierte ("*Feldname*")-** Funktion verwenden, um zu bestimmen, ob ein Feld geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9586d-111">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="9586d-112">The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span><span class="sxs-lookup"><span data-stu-id="9586d-112">The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="9586d-113">Mit der folgenden Syntax können Sie auf einen Wert im gelöschten Datensatz zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9586d-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="9586d-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span><span class="sxs-lookup"><span data-stu-id="9586d-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="9586d-115">Am Ende des Ereignisses **Nach Löschvorgang** werden die Werte im gelöschten Datensatz dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9586d-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="9586d-116">Die folgenden Makrobefehle können im Ereignis **nach Lösch** Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9586d-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9586d-117">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="9586d-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="9586d-118">Befehl</span><span class="sxs-lookup"><span data-stu-id="9586d-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9586d-119">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="9586d-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="9586d-120"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="9586d-120"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-121">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="9586d-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="9586d-122"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="9586d-122"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-123">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="9586d-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="9586d-124"><a href="if-then-else-macro-block.md">Wenn...Dann...Sonst-Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="9586d-124"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-125">Datenblock</span><span class="sxs-lookup"><span data-stu-id="9586d-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="9586d-126"><a href="createrecord-data-block.md">CreateRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-126"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-127">Datenblock</span><span class="sxs-lookup"><span data-stu-id="9586d-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="9586d-128"><a href="editrecord-data-block.md">Bearbeitendatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-128"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-129">Datenblock</span><span class="sxs-lookup"><span data-stu-id="9586d-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="9586d-130"><a href="foreachrecord-data-block.md">Fürjedendatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-130"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-131">Datenblock</span><span class="sxs-lookup"><span data-stu-id="9586d-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="9586d-132"><a href="lookuprecord-data-block.md">LookupRecord-Datenblock</a></span><span class="sxs-lookup"><span data-stu-id="9586d-132"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-133">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-135">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-136"><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-136"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-137">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-138"><a href="deleterecord-macro-action.md">DeleteRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-138"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-139">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-141">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-142"><a href="logevent-macro-action.md">LogEvent-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-142"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-143">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-144"><a href="onerror-macro-action.md">OnError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-144"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-145">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-146"><a href="raiseerror-macro-action.md">RaiseError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-146"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-147">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-148"><a href="rundatamacro-macro-action.md">RunDataMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-148"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-149">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-150"><a href="sendemail-macro-action.md">SendEmail-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-150"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-151">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-152"><a href="setfield-macro-action.md">SetField-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-152"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-153">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-154"><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-154"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9586d-155">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-156"><a href="stopallmacros-macro-action.md">StopAllMacros-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-156"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9586d-157">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="9586d-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9586d-158"><a href="stopmacro-macro-action.md">StopMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="9586d-158"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9586d-159">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Löschvorgang** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="9586d-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="9586d-160">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Löschvorgang** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="9586d-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="9586d-161">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Löschvorgang**.</span><span class="sxs-lookup"><span data-stu-id="9586d-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="9586d-162">Im Makro-Designer wird ein leeres Datenmakro angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9586d-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="9586d-163">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9586d-163">Example</span></span>

<span data-ttu-id="9586d-p104">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table. When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span><span class="sxs-lookup"><span data-stu-id="9586d-p104">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table. When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="9586d-166">**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, die Sie im Makro-Designer einfügen können.**</span><span class="sxs-lookup"><span data-stu-id="9586d-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="9586d-167">Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="9586d-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="9586d-168">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Löschvorgang** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="9586d-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="9586d-169">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Löschvorgang**.</span><span class="sxs-lookup"><span data-stu-id="9586d-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="9586d-170">Wählen Sie den unten dargestellten Code aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="9586d-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="9586d-171">Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.</span><span class="sxs-lookup"><span data-stu-id="9586d-171">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterDelete"> 
        <Statements> 
          <Comment>Initialize a variable and assign the old</Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Old].[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Old].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Collapsed="true" Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Old].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
```

<br/>

```vb
    SetLocalVar 
                    Name    varAmount 
              Expression   =[Old].[Amount] 
     
    If   Not(IsNull([Old].[CampaignID]]))   Then 
     
         For Each Record In     Campaigns 
            Where Condition     =[ID]=[Old].[CampaignID] 
                      Alias 
            EditRecord 
                      Alias 
                  SetField   ([DonationsReceived], [DonationsReceived] - [varAmount]) 
            End EditRecord 
     
    End If 
     
    If   Not(IsNull([Old].[DonorID]]))   Then 
     
         For Each Record In    Donors 
            Where Condition     =[ID]=[Old].[DonorID] 
                      Alias 
            EditRecord 
                      Alias 
     
              SetField 
                             Name   [TotalDonated] 
                            Value   =[TotalDonated]-[varAmount] 
            End EditRecord 
    End If
```
