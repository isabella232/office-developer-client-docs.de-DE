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
ms.openlocfilehash: e803ccc915a939878cf758698a98661c2a3f5283
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473889"
---
# <a name="after-delete-macro-event"></a>Makroereignis "Nach Löschvorgang"


**Betrifft**: Access 2013 | Office 2013

Das Ereignis **Nach Löschvorgang** tritt auf, nachdem ein Datensatz gelöscht wurde.


> [!NOTE]
> [!HINWEIS] Das Ereignis **Nach Löschvorgang** ist nur in Datenmakros verfügbar.



## <a name="remarks"></a>Hinweise

Mit dem Ereignis **Nach Löschvorgang** führen Sie sämtliche Aktionen nach dem Löschen eines Datensatzes aus. Häufig wird **Nach Löschvorgang** verwendet, um Geschäftsregeln und Workflows zu erzwingen, einen Aggregatgesamtwert zu aktualisieren oder Benachrichtigungen zu senden.

Wenn das Ereignis **Nach Löschvorgang** aufgetreten ist, bleiben die im gelöschten Datensatz enthaltenen Werte verfügbar. Sie möchten einen gelöschten Wert erhöhen oder verringern insgesamt, erstellen einen Überwachungspfad oder im Vergleich zu einem vorhandenen Wert in einem Argument *Bedingung* verwenden.

Mit der Funktion Updated("Feldname") ermitteln Sie, ob ein Feld geändert wurde. Das folgende Codebeispiel zeigt die Verwendung einer If-Anweisung zum Ermitteln, ob das PaidInFull-Feld geändert wurde.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Mit der folgenden Syntax können Sie auf einen Wert im gelöschten Datensatz zugreifen.

`[Old].[Field Name]`

Um den Wert des QuantityInStock-Felds im gelöschten Datensatz zugreifen möchten, verwenden Sie beispielsweise die folgende Syntax.

`[Old].[QuantityInStock]`

Am Ende des Ereignisses **Nach Löschvorgang** werden die Werte im gelöschten Datensatz dauerhaft gelöscht.

Die folgenden Makrobefehle verwenden, können das Ereignis **Nach Löschvorgang** verwendet werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Befehlstyp</p></th>
<th><p>Command</p></th>
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
<td><p><a href="editrecord-data-block.md">BearbeitenDatensatz-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenblock</p></td>
<td><p><a href="foreachrecord-data-block.md">FürJedenDatensatz-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenblock</p></td>
<td><p><a href="lookuprecord-data-block.md">NachschlagenDatensatz-Datenblock</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">AbbrechenDatensatzänderung-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="clearmacroerror-macro-action.md">LöschenMakroFehler-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="deleterecord-macro-action.md">DatensatzLöschen-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">BeendenFürJedenDatensatz-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="logevent-macro-action.md">ProtokollierenEreignis-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="onerror-macro-action.md">BeiFehler-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="raiseerror-macro-action.md">AuslösenFehler-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="rundatamacro-macro-action.md">AusführenDatenmakro-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="sendemail-macro-action.md">SendenEMail-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="setfield-macro-action.md">FestlegenFeld-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="setlocalvar-macro-action.md">FestlegenLokaleVar-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="stopallmacros-macro-action.md">StoppAlleMakros-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></p></td>
</tr>
</tbody>
</table>


Zum Erstellen eines Datenmakros, mit dem das Ereignis **Nach Löschvorgang** erfasst wird, führen Sie die folgenden Schritte aus.

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Löschvorgang** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Löschvorgang**.

Im Makro-Designer wird ein leeres Datenmakro angezeigt.

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird das Ereignis **Nach Löschvorgang** um einige Verarbeitung beim Löschen eines Datensatzes aus der Tabelle Spenden auszuführen, verwendet. Wenn ein Datensatz gelöscht wird, ist der Zeitraum der Spenden Subracted Formular das DonationsReceived-Feld in der Tabelle DonationsReceived und die TotalDonatedField in der Spender-Tabelle.

**Klicken Sie hier, um eine Kopie des Makros anzuzeigen, die Sie im Makro-Designer einfügen können.**

Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Nach Löschvorgang** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Nachfolgeereignisse** auf **Nach Löschvorgang**.

3.  Wählen Sie den unten dargestellten Code aus, und drücken Sie dann STRG+C, um diesen in die Zwischenablage zu kopieren.

4.  Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie dann STRG+V.

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
