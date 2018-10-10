---
title: Makroereignis 'Nach Eingabe'
TOCTitle: After Insert Macro Event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a343c9bb0ea498c3388eb5ce67c3e0692808824c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473891"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="96003-102">Makroereignis "Nach Eingabe"</span><span class="sxs-lookup"><span data-stu-id="96003-102">After Insert Macro Event</span></span>


<span data-ttu-id="96003-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="96003-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="96003-104">Das Ereignis **Nach Eingabe** tritt auf, wenn ein Datensatz hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="96003-104">The **After Insert** event occurs after a record is added.</span></span>


> [!NOTE]
> <span data-ttu-id="96003-105">[!HINWEIS] Das Ereignis **Nach Eingabe** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="96003-105">The **After Insert** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="96003-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="96003-106">Remarks</span></span>

<span data-ttu-id="96003-p101">Mit dem Ereignis **Nach Eingabe** führen Sie sämtliche Aktionen nach dem Hinzufügen eines Datensatzes zu einer Tabelle aus. Häufig wird **Nach Eingabe** verwendet, um Geschäftsregeln und Workflows zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="96003-p101">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table. Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="96003-p102">Mit der Funktion Updated("Feldname") ermitteln Sie, ob ein Feld geändert wurde. Das folgende Codebeispiel zeigt die Verwendung einer If-Anweisung zum Ermitteln, ob das PaidInFull-Feld geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="96003-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="96003-111">In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Nach Eingabe** verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="96003-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96003-112">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="96003-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="96003-113">Command</span><span class="sxs-lookup"><span data-stu-id="96003-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96003-114">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="96003-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="96003-115"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="96003-115"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-116">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="96003-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="96003-117"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="96003-117"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-118">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="96003-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="96003-119"><a href="if-then-else-macro-block.md">Wenn...Dann...Sonst-Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="96003-119"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-120">Datenblock</span><span class="sxs-lookup"><span data-stu-id="96003-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="96003-121"><a href="createrecord-data-block.md">DatensatzErstellen-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-121"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-122">Datenblock</span><span class="sxs-lookup"><span data-stu-id="96003-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="96003-123"><a href="editrecord-data-block.md">BearbeitenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-123"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-124">Datenblock</span><span class="sxs-lookup"><span data-stu-id="96003-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="96003-125"><a href="foreachrecord-data-block.md">FürJedenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-125"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-126">Datenblock</span><span class="sxs-lookup"><span data-stu-id="96003-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="96003-127"><a href="lookuprecord-data-block.md">NachschlagenDatensatz-Datenblock</a></span><span class="sxs-lookup"><span data-stu-id="96003-127"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-128">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-129"><a href="cancelrecordchange-macro-action.md">AbbrechenDatensatzänderung-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-130">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-131"><a href="clearmacroerror-macro-action.md">LöschenMakroFehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-131"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-132">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-133"><a href="deleterecord-macro-action.md">DatensatzLöschen-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-133"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-134">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-135"><a href="exitforeachrecord-macro-action.md">BeendenFürJedenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-136">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-137"><a href="logevent-macro-action.md">ProtokollierenEreignis-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-137"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-138">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-139"><a href="onerror-macro-action.md">BeiFehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-139"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-140">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-141"><a href="raiseerror-macro-action.md">AuslösenFehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-141"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-142">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-143"><a href="rundatamacro-macro-action.md">AusführenDatenmakro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-143"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-144">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-145"><a href="sendemail-macro-action.md">SendenEMail-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-145"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-146">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-147"><a href="setfield-macro-action.md">FestlegenFeld-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-147"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-148">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-149"><a href="setlocalvar-macro-action.md">FestlegenLokaleVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-149"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96003-150">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-151"><a href="stopallmacros-macro-action.md">StoppAlleMakros-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="96003-151"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96003-152">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="96003-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="96003-153"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="96003-153"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96003-154">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Eingabe** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="96003-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="96003-155">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Eingabe** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="96003-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="96003-156">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Eingabe**.</span><span class="sxs-lookup"><span data-stu-id="96003-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="96003-157">Im Makro-Designer wird ein leeres Datenmakro angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96003-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="96003-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="96003-158">Example</span></span>

<span data-ttu-id="96003-159">Im folgenden Codebeispiel wird das Ereignis **Nach Eingabe** auszuführenden einige verarbeiten, wenn die Spenden-Tabelle ein Datensatz hinzugefügt wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="96003-159">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table.</span></span> <span data-ttu-id="96003-160">Wenn ein Datensatz hinzugefügt wird, wird die Anzahl der Spenden Feld DonationsReceived in der Tabelle Kampagnen sowie die TotalDonatedField in der Spender-Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96003-160">When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="96003-161">**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, die Sie im Makro-Designer einfügen können.**</span><span class="sxs-lookup"><span data-stu-id="96003-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="96003-162">Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="96003-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="96003-163">Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Eingabe** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="96003-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="96003-164">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Eingabe**.</span><span class="sxs-lookup"><span data-stu-id="96003-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="96003-165">Wählen Sie den Code im folgenden Codebeispiel aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="96003-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="96003-166">Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.</span><span class="sxs-lookup"><span data-stu-id="96003-166">Activate the macro designer window and then press CTRL+V.</span></span>

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
