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
# <a name="after-insert-macro-event"></a>Makroereignis „Nach Eingabe“

**Gilt für**: Access 2013, Office 2013

Das Ereignis **Nach Eingabe** tritt auf, wenn ein Datensatz hinzugefügt wurde.

> [!NOTE]
> Das Ereignis **Nach Eingabe** ist nur in Datenmakros verfügbar.

## <a name="remarks"></a>Bemerkungen

Mit dem Ereignis **Nach Eingabe** führen Sie sämtliche Aktionen nach dem Hinzufügen eines Datensatzes zu einer Tabelle aus. Häufig wird **Nach Eingabe** verwendet, um Geschäftsregeln und Workflows zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.

Mithilfe der Funktion **Aktualisiert("*Feldname*")** können Sie feststellen, ob sich ein Feld verändert hat. Das folgende Codebeispiel zeigt, wie man eine **Wenn**-Anweisung verwendet, um zu ermitteln, ob das Feld "VollständigBezahlt" geändert wurde.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Nach Eingabe** verwendet werden können.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Befehlstyp</p></th>
<th><p>Befehl</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Programmablauf</p></td>
<td><p><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></p></td>
</tr>
<tr class="even">
<td><p>Programmablauf</p></td>
<td><p><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></p></td>
</tr>
<tr class="odd">
<td><p>Programmablauf</p></td>
<td><p><a href="if-then-else-macro-block.md">Wenn...Dann...Sonst-Makroblock</a></p></td>
</tr>
<tr class="even">
<td><p>Datenblock</p></td>
<td><p><a href="createrecord-data-block.md">DatensatzErstellen-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenblock</p></td>
<td><p><a href="editrecord-data-block.md">DatensatzBearbeiten-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenblock</p></td>
<td><p><a href="foreachrecord-data-block.md">FürJedenDatensatz-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenblock</p></td>
<td><p><a href="lookuprecord-data-block.md">LookupRecord-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">AbbrechenDatensatzÄnderung-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="deleterecord-macro-action.md">DatensatzLöschen-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">ExitForEachRecord-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="logevent-macro-action.md">LogEvent-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="onerror-macro-action.md">OnError-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="raiseerror-macro-action.md">RaiseError-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="rundatamacro-macro-action.md">RunDataMacro-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="sendemail-macro-action.md">SendEmail-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="setfield-macro-action.md">SetField-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="stopallmacros-macro-action.md">StopAllMacros-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro-Makroaktion</a></p></td>
</tr>
</tbody>
</table>


Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Eingabe** erfasst wird, führen Sie die folgenden Schritte aus.

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Eingabe** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Eingabe**.

Im Makro-Designer wird ein leeres Datenmakro angezeigt.

## <a name="example"></a>Beispiel

The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table. When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.

**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, das Sie in Macro Designer einfügen können.**

Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Eingabe** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Eingabe**.

3.  Wählen Sie den Code im folgenden Codebeispiel aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.

4.  Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.

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
