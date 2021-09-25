---
title: SetReturnVar-Makroaktion
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f4dc72f0416094be8f76be846d94818bfc2bc64b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564891"
---
# <a name="setreturnvar-macro-action"></a>SetReturnVar-Makroaktion

**Gilt für**: Access 2013, Office 2013

Die **SetReturnVar-Aktion** erstellt eine Rückgabevariable und legt sie auf einen bestimmten Wert fest.

> [!NOTE]
> Die **SetReturnVar-Aktion** ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **SetReturnVar-Aktion** hat die folgenden Argumente.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Erforderlich</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Ja</p></td>
<td><p>Eine Zeichenfolge, die den Namen der Variablen angibt.</p></td>
</tr>
<tr class="even">
<td><p>Expression</p></td>
<td><p>Ja</p></td>
<td><p>Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird. Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran. Sie können auf die Schaltfläche <strong>Erstellen</strong> klicken, um das Argument mithilfe des <strong>Ausdrucks-Generators</strong> festzulegen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die **SetReturnVar-Aktion** wird verwendet, um eine **ReturnVar**-Variable zu erstellen, die von Makros verwendet werden kann, die ein Datenmakro mithilfe der **RunDataMacro-Aktion** aufrufen.

Sobald ein **ReturnVar** durch die **SetReturnVar-Aktion** erstellt wurde, kann das aufrufende Makro es in einem Ausdruck verwenden. Wenn Sie beispielsweise einen **ReturnVar** mit dem Namen **UpdateSuccess** erstellt haben, können Sie die Variable mit der folgenden Syntax verwenden:

```vb
    =[ReturnVars]![UpdateSuccess]
```

Die **SetReturnVar-Aktion** kann nur in benannten Datenmakros verwendet werden. Sie ist in Datenmakros, die an ein Datenmakroereignis angefügt sind, nicht verfügbar.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie die SetReturnVar-Aktion verwenden, um einen Wert aus einem benannten Datenmakro zurückzugeben. Ein ReturnVar mit dem Namen **CurrentServiceRequest** wird an das Makro oder die Visual Basic for Applications (VBA)-Unterroutine zurückgegeben, die das benannte Datenmakro aufgerufen hat.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
