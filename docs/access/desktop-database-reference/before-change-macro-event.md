---
title: Makroereignis "Vor Änderung"
TOCTitle: Before Change macro event
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
localization_priority: Normal
ms.openlocfilehash: b37fb96ddfeaabc97c6f445f8951876e8026fbfe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703958"
---
# <a name="before-change-macro-event"></a>Makroereignis "Vor Änderung"

**Betrifft**: Access 2013, Office 2013

Das Ereignis **Vor Änderung** tritt ein, wenn ein Datensatz geändert wird, jedoch bevor der Commit für die Änderung erfolgt ist.

> [!NOTE]
> [!HINWEIS] Das Ereignis **Vor Änderung** ist nur in Datenmakros verfügbar.

## <a name="remarks"></a>Hinweise

Mit dem Ereignis **Vor Änderung** führen Sie sämtliche Aktionen vor dem Ändern eines Datensatzes aus. Das Ereignis **Vor Änderung** wird häufig verwendet, um Überprüfungen auszuführen und benutzerdefinierte Fehlermeldungen auszugeben.

Die **aktualisierte ("der*Name des Felds*")** -Funktion können bestimmen, ob ein Feld geändert hat. Im folgenden Codebeispiel wird veranschaulicht, wie eine **If** -Anweisung verwenden, um festzustellen, ob das Feld PaidInFull geändert wurde.

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

Mit der **IstEingefügt** -Eigenschaft ermitteln Sie, ob das Ereignis **Vor Änderung** durch das Erstellen eines neuen Datensatzes oder eine Änderung an einem vorhandenen Datensatz ausgelöst wurde. Die **IstEingefügt** -Eigenschaft enthält **True**, wenn das Ereignis durch einen neuen Datensatz ausgelöst wurde, und **False**, wenn das Ereignis durch eine Änderung an einem vorhandenen Datensatz ausgelöst wurde.

Das folgende Codebeispiel veranschaulicht die Syntax der **IstEingefügt** -Eigenschaft.

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

Mit der folgenden Syntax können Sie auf einen vorherigen Wert in einem Feld zugreifen.

```vb
    [Old].[Field Name]
```

Zugriff auf den vorherigen Wert des QuantityInStock-Felds verwenden Sie beispielsweise die folgende Syntax.

```vb
    [Old].[QuantityInStock]
```

Am Ende des Ereignisses **Vor Änderung** werden die vorherigen Werte dauerhaft gelöscht.

Mit der **AuslösenFehler** -Aktion können Sie das Ereignis **Vor Änderung** abbrechen. Bei einem Fehler werden die Änderungen im Ereignis **Vor Änderung** verworfen.

In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Vor Änderung** verwendet werden können.

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
<td><p><a href="lookuprecord-data-block.md">NachschlagenDatensatz-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="onerror-macro-action.md">OnError-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="raiseerror-macro-action.md">RaiseError-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="setfield-macro-action.md">SetField-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro-Makroaktion</a></p></td>
</tr>
</tbody>
</table>


Zum Erstellen eines Datenmakros, mit dem das Ereignis **Vor Änderung** erfasst wird, führen Sie die folgenden Schritte aus.

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Vor Änderung** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Vorabereignisse** auf **Vor Änderung**.

Im Makro-Designer wird ein leeres Datenmakro angezeigt.

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird wird das Ereignis **Vor Änderung** verwendet, um die Felder Status überprüfen. Ein Fehler wird ausgelöst, wenn ein ungültiger Wert in das Feld Auflösung enthalten ist.

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

Zum Anzeigen dieses Beispiels im Makro-Designer gehen Sie folgendermaßen vor:

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Vor Änderung** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Vorabereignisse** auf **Vor Änderung**.

3.  Wählen Sie den Code im folgenden Codebeispiel wird ein, und drücken Sie **STRG + C** , um ihn in die Zwischenablage zu kopieren.

4.  Aktivieren Sie das Makro-Designer-Fenster, und drücken Sie **STRG + V**.



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

Das folgende Beispiel veranschaulicht die Auslösenfehler-Aktion verwenden, um das Ereignis vor Änderung Daten Makro abzubrechen. Wenn das Feld AssignedTo aktualisiert wird, wird mit einem NachschlagenDatensatz-Datenblock verwendet, um festzustellen, ob der zugewiesene Techniker eine open Service-Anforderung derzeit zugewiesen ist. Wenn dies der Fall ist, klicken Sie dann das Ereignis vor Änderung abgebrochen, und der Datensatz nicht aktualisiert.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
