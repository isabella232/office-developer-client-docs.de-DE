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
ms.openlocfilehash: 5b3b2da44d817885eb6190a8cbbfc73bf99e9e0a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538235"
---
# <a name="after-delete-macro-event"></a>Makroereignis "Nach Löschvorgang"

**Gilt für**: Access 2013, Office 2013

Das Ereignis **Nach Löschvorgang** tritt auf, nachdem ein Datensatz gelöscht wurde.

> [!NOTE]
> Das Ereignis **Nach Löschvorgang** ist nur in Datenmakros verfügbar.

## <a name="remarks"></a>Hinweise

Mit dem Ereignis **Nach Löschvorgang** führen Sie sämtliche Aktionen nach dem Löschen eines Datensatzes aus. Häufig wird **Nach Löschvorgang** verwendet, um Geschäftsregeln und Workflows zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.

Wenn das Ereignis **Nach Löschvorgang** aufgetreten ist, bleiben die im gelöschten Datensatz enthaltenen Werte verfügbar. Möglicherweise möchten Sie einen gelöschten Wert verwenden, um eine Summe zu erhöhen oder zu verringern, einen Überwachungspfad zu erstellen oder mit einem vorhandenen Wert in einem *WhereCondition* -Argument zu vergleichen.

Mithilfe der Funktion **Aktualisiert(„*Feldname*“) ** können Sie feststellen, ob sich ein Feld verändert hat. The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Mit der folgenden Syntax können Sie auf einen Wert im gelöschten Datensatz zugreifen.

`[Old].[Field Name]`

For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.

`[Old].[QuantityInStock]`

Am Ende des Ereignisses **Nach Löschvorgang** werden die Werte im gelöschten Datensatz dauerhaft gelöscht.

Die folgenden Makrobefehle können im **after DELETE** -Ereignis verwendet werden.

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
<td><p><a href="cancelrecordchange-macro-action.md">CancelRecordChange-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="deleterecord-macro-action.md">DeleteRecord-Makroaktion</a></p></td>
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


Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Löschvorgang** erfasst wird, führen Sie die folgenden Schritte aus.

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Löschvorgang** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Löschvorgang**.

Im Makro-Designer wird ein leeres Datenmakro angezeigt.

## <a name="example"></a>Beispiel

The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table. When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.

**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, das Sie in Makro-Designer einfügen können.**

Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Löschvorgang** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Löschvorgang**.

3.  Wählen Sie den unten dargestellten Code aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.

4.  Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="http://schemas.microsoft.com/office/accessservices/2009/04/application"> 
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
