---
title: Makroereignis „Nach Eingabe“
TOCTitle: After Insert macro event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c84a737d08b791bfe560bfe6af6bcc59a14d2678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297221"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="babc7-102">Makroereignis „Nach Eingabe“</span><span class="sxs-lookup"><span data-stu-id="babc7-102">After Insert macro event</span></span>

<span data-ttu-id="babc7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="babc7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="babc7-104">Das Ereignis **Nach Eingabe** tritt auf, wenn ein Datensatz hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="babc7-104">The **After Insert** event occurs after a record is added.</span></span>

> [!NOTE]
> <span data-ttu-id="babc7-105">Das Ereignis **Nach Eingabe** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="babc7-105">The **After Insert** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="babc7-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="babc7-106">Remarks</span></span>

<span data-ttu-id="babc7-p101">Mit dem Ereignis **Nach Eingabe** führen Sie sämtliche Aktionen nach dem Hinzufügen eines Datensatzes zu einer Tabelle aus. Häufig wird **Nach Eingabe** verwendet, um Geschäftsregeln und Workflows zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="babc7-p101">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table. Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="babc7-109">Mithilfe der Funktion **Aktualisiert("*Feldname*")** können Sie feststellen, ob sich ein Feld verändert hat.</span><span class="sxs-lookup"><span data-stu-id="babc7-109">You can use the \*\*Updated(" Field Name  ") \*\* function to determine whether a field has changed.</span></span> <span data-ttu-id="babc7-110">Das folgende Codebeispiel zeigt, wie man eine **Wenn**-Anweisung verwendet, um zu ermitteln, ob das Feld "VollständigBezahlt" geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="babc7-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="babc7-111">In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Nach Eingabe** verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="babc7-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="babc7-112">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="babc7-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="babc7-113">Befehl</span><span class="sxs-lookup"><span data-stu-id="babc7-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="babc7-114">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="babc7-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="babc7-115"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="babc7-115"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-116">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="babc7-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="babc7-117"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="babc7-117"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-118">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="babc7-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="babc7-119"><a href="if-then-else-macro-block.md">Wenn...Dann...Sonst-Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="babc7-119"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-120">Datenblock</span><span class="sxs-lookup"><span data-stu-id="babc7-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="babc7-121"><a href="createrecord-data-block.md">DatensatzErstellen-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-121"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-122">Datenblock</span><span class="sxs-lookup"><span data-stu-id="babc7-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="babc7-123"><a href="editrecord-data-block.md">DatensatzBearbeiten-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-123"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-124">Datenblock</span><span class="sxs-lookup"><span data-stu-id="babc7-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="babc7-125"><a href="foreachrecord-data-block.md">FürJedenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-125"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-126">Datenblock</span><span class="sxs-lookup"><span data-stu-id="babc7-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="babc7-127"><a href="lookuprecord-data-block.md">LookupRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-127"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-128">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-129"><a href="cancelrecordchange-macro-action.md">AbbrechenDatensatzÄnderung-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-130">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-131"><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-132">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-133"><a href="deleterecord-macro-action.md">DatensatzLöschen-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-133"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-134">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-136">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-137"><a href="logevent-macro-action.md">LogEvent-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-137"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-138">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-139"><a href="onerror-macro-action.md">OnError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-139"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-140">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-141"><a href="raiseerror-macro-action.md">RaiseError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-141"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-142">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-143"><a href="rundatamacro-macro-action.md">RunDataMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-143"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-144">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-145"><a href="sendemail-macro-action.md">SendEmail-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-145"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-146">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-147"><a href="setfield-macro-action.md">SetField-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-147"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-148">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-149"><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-149"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babc7-150">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-151"><a href="stopallmacros-macro-action.md">StopAllMacros-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-151"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babc7-152">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="babc7-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="babc7-153"><a href="stopmacro-macro-action.md">StopMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="babc7-153"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="babc7-154">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Eingabe** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="babc7-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="babc7-155">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Eingabe** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="babc7-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="babc7-156">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Eingabe**.</span><span class="sxs-lookup"><span data-stu-id="babc7-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="babc7-157">Im Makro-Designer wird ein leeres Datenmakro angezeigt.</span><span class="sxs-lookup"><span data-stu-id="babc7-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="babc7-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="babc7-158">Example</span></span>

<span data-ttu-id="babc7-p103">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table. When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span><span class="sxs-lookup"><span data-stu-id="babc7-p103">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table. When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="babc7-161">**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, das Sie in Macro Designer einfügen können.**</span><span class="sxs-lookup"><span data-stu-id="babc7-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="babc7-162">Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="babc7-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="babc7-163">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Eingabe** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="babc7-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="babc7-164">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Eingabe**.</span><span class="sxs-lookup"><span data-stu-id="babc7-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="babc7-165">Wählen Sie den Code im folgenden Codebeispiel aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="babc7-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="babc7-166">Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.</span><span class="sxs-lookup"><span data-stu-id="babc7-166">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <DataMacros> 
      <DataMacro Event="AfterInsert"> 
        <Statements> 
          <Comment>This data macro increments the DonationsReceived field in Campaigns and theAmountCollected field in Pledges </Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Donations].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]+[varAmount]</Argument> 
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
              <Condition>Not (IsNull([DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Donations].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]+[varAmount]</Argument> 
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
                  Name   varAmount 
            Expression   =[Amount] 
     
    If   Not (IsNull([CampaignID]))   Then 
     
         For Each Record In   Campaigns 
            Where Condition   =[ID]=[Donations].[CampaignID] 
                      Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [DonationsReceived] 
                                Value   =[DonationsReceived]+[varAmount] 
                End EditRecord 
    End If 
     
    If   Not (IsNull([DonorID]))   Then 
     
         For Each Record In  Donors 
            WhereCondition   =[ID]=[Donations].[DonorID] 
                     Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [TotalDonated] 
                                Value   =[TotalDonated]+[varAmount] 
                 End EditRecord 
    End If
```
