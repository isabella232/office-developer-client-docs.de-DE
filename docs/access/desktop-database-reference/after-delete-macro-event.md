---
title: Makroereignis 'Nach Löschvorgang'
TOCTitle: After Delete Macro Event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b180acb99ab2ac406a7b60fdecf8aff5d63eb71f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869113"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="80b0b-102">Makroereignis "Nach Löschvorgang"</span><span class="sxs-lookup"><span data-stu-id="80b0b-102">After Delete Macro Event</span></span>


<span data-ttu-id="80b0b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80b0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80b0b-104">Das Ereignis **Nach Löschvorgang** tritt auf, nachdem ein Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="80b0b-104">The **After Delete** event occurs after a record is deleted.</span></span>


> [!NOTE]
> <span data-ttu-id="80b0b-105">[!HINWEIS] Das Ereignis **Nach Löschvorgang** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="80b0b-105">The **After Delete** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="80b0b-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80b0b-106">Remarks</span></span>

<span data-ttu-id="80b0b-p101">Mit dem Ereignis **Nach Löschvorgang** führen Sie sämtliche Aktionen nach dem Löschen eines Datensatzes aus. Häufig wird **Nach Löschvorgang** verwendet, um Geschäftsregeln und Workflows zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="80b0b-p101">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted. Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="80b0b-109">Wenn das Ereignis **Nach Löschvorgang** aufgetreten ist, bleiben die im gelöschten Datensatz enthaltenen Werte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="80b0b-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="80b0b-110">Sie möchten einen gelöschten Wert erhöhen oder verringern insgesamt, erstellen einen Überwachungspfad oder im Vergleich zu einem vorhandenen Wert in einem Argument *Bedingung* verwenden.</span><span class="sxs-lookup"><span data-stu-id="80b0b-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="80b0b-p103">Mit der Funktion Updated("Feldname") ermitteln Sie, ob ein Feld geändert wurde. Das folgende Codebeispiel zeigt die Verwendung einer If-Anweisung zum Ermitteln, ob das PaidInFull-Feld geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="80b0b-p103">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="80b0b-113">Mit der folgenden Syntax können Sie auf einen Wert im gelöschten Datensatz zugreifen.</span><span class="sxs-lookup"><span data-stu-id="80b0b-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="80b0b-114">Um den Wert des QuantityInStock-Felds im gelöschten Datensatz zugreifen möchten, verwenden Sie beispielsweise die folgende Syntax.</span><span class="sxs-lookup"><span data-stu-id="80b0b-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="80b0b-115">Am Ende des Ereignisses **Nach Löschvorgang** werden die Werte im gelöschten Datensatz dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="80b0b-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="80b0b-116">Die folgenden Makrobefehle verwenden, können das Ereignis **Nach Löschvorgang** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80b0b-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80b0b-117">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="80b0b-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="80b0b-118">Command</span><span class="sxs-lookup"><span data-stu-id="80b0b-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-119">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="80b0b-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="80b0b-120"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-120"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-121">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="80b0b-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="80b0b-122"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-122"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-123">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="80b0b-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="80b0b-124"><a href="if-then-else-macro-block.md">If... Im Anschluss: Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-124"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-125">Datenblock</span><span class="sxs-lookup"><span data-stu-id="80b0b-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="80b0b-126"><a href="createrecord-data-block.md">DatensatzErstellen-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-126"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-127">Datenblock</span><span class="sxs-lookup"><span data-stu-id="80b0b-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="80b0b-128"><a href="editrecord-data-block.md">BearbeitenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-128"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-129">Datenblock</span><span class="sxs-lookup"><span data-stu-id="80b0b-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="80b0b-130"><a href="foreachrecord-data-block.md">FürJedenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-130"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-131">Datenblock</span><span class="sxs-lookup"><span data-stu-id="80b0b-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="80b0b-132"><a href="lookuprecord-data-block.md">LookupRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-132"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-133">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-134"><a href="cancelrecordchange-macro-action.md">Abbrechendatensatzänderung-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-135">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-136"><a href="clearmacroerror-macro-action.md">Löschenmakrofehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-136"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-137">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-138"><a href="deleterecord-macro-action.md">DatensatzLöschen-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-138"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-139">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-140"><a href="exitforeachrecord-macro-action.md">BeendenFürJedenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-141">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-142"><a href="logevent-macro-action.md">Protokollierenereignis-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-142"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-143">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-144"><a href="onerror-macro-action.md">BeiFehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-144"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-145">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-146"><a href="raiseerror-macro-action.md">Auslösenfehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-146"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-147">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-148"><a href="rundatamacro-macro-action.md">AusführenDatenmakro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-148"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-149">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-150"><a href="sendemail-macro-action.md">SendenEMail-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-150"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-151">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-152"><a href="setfield-macro-action.md">SetField-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-152"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-153">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-154"><a href="setlocalvar-macro-action.md">FestlegenLokaleVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-154"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80b0b-155">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-156"><a href="stopallmacros-macro-action.md">StoppAlleMakros-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-156"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80b0b-157">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="80b0b-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="80b0b-158"><a href="stopmacro-macro-action.md">StoppMakro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="80b0b-158"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80b0b-159">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Löschvorgang** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="80b0b-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="80b0b-160">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Löschvorgang** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="80b0b-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="80b0b-161">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Löschvorgang**.</span><span class="sxs-lookup"><span data-stu-id="80b0b-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="80b0b-162">Im Makro-Designer wird ein leeres Datenmakro angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80b0b-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="80b0b-163">Beispiel</span><span class="sxs-lookup"><span data-stu-id="80b0b-163">Example</span></span>

<span data-ttu-id="80b0b-164">Im folgenden Codebeispiel wird das Ereignis **Nach Löschvorgang** um einige Verarbeitung beim Löschen eines Datensatzes aus der Tabelle Spenden auszuführen, verwendet.</span><span class="sxs-lookup"><span data-stu-id="80b0b-164">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table.</span></span> <span data-ttu-id="80b0b-165">Wenn ein Datensatz gelöscht wird, ist der Zeitraum der Spenden Subracted Formular das DonationsReceived-Feld in der Tabelle DonationsReceived und die TotalDonatedField in der Spender-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="80b0b-165">When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="80b0b-166">**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, die Sie im Makro-Designer einfügen können.**</span><span class="sxs-lookup"><span data-stu-id="80b0b-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="80b0b-167">Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="80b0b-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="80b0b-168">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Löschvorgang** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="80b0b-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="80b0b-169">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Löschvorgang**.</span><span class="sxs-lookup"><span data-stu-id="80b0b-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="80b0b-170">Wählen Sie den unten dargestellten Code aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="80b0b-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="80b0b-171">Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.</span><span class="sxs-lookup"><span data-stu-id="80b0b-171">Activate the macro designer window and then press CTRL+V.</span></span>

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
