---
title: SetReturnVar Macro Action
TOCTitle: SetReturnVar Macro Action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa4380904888194bf1d954ebf5619cab7d155047
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473814"
---
# <a name="setreturnvar-macro-action"></a>SetReturnVar Macro Action

**Betrifft**: Access 2013 | Office 2013

Die **SetReturnVar** -Aktion erstellt eine Variable zurückgegebene und platziert es in einem bestimmten Wert.

> [!NOTE]
> Die **SetReturnVar** -Aktion ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **SetReturnVar** -Aktion hat die folgenden Argumente.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Eingabe erforderlich</p></th>
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
<td><p>Ausdruck</p></td>
<td><p>Ja</p></td>
<td><p>Ein Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen. Setzen Sie den Ausdruck mit dem Gleichheitszeichen (=). Sie können klicken Sie auf die Schaltfläche <strong>Erstellen</strong> , um den <strong>Ausdrucks-Generator</strong> verwenden, um dieses Argument festzulegen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die Aktion **SetReturnVar** dient zum Erstellen einer **ReturnVar**die Variable, die von Makros kann, die ein Datenmakro Aufrufen verwendet werden, indem Sie mit der **AusführenDatenmakro** -Aktion ist.

Sobald ein **ReturnVar** durch die **SetReturnVar** -Aktion erstellt wurde, kann das aufrufende Makro in einem Ausdruck verwenden. Angenommen, wenn Sie eine **ReturnVar** mit dem Namen **UpdateSuccess**erstellt, können die Variable Sie mithilfe der folgenden Syntax:

```vb
    =[ReturnVars]![UpdateSuccess]
```

Die **SetReturnVar** -Aktion kann nur in benannten Datenmakros verwendet werden. Es ist nicht verfügbar in Datenmakros, die ein Ereignis eines Makro zugeordnet sind.

## <a name="example"></a>Beispiel

Das folgende Beispiel veranschaulicht die SetReturnVar-Aktion verwenden, um einen Wert aus ein benanntes Datenmakro zurückzugeben. Eine mit dem Namen **CurrentServiceRequest** ReturnVar wird an das Makro oder Visual Basic für Applikationen (VBA) Unterroutine zurückgegeben, die das benanntes Datenmakro aufgerufen.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
