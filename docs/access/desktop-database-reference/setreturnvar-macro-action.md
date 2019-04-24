---
title: SetReturnVar-Makroaktion
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308673"
---
# <a name="setreturnvar-macro-action"></a>SetReturnVar-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **SetReturnVar** -Aktion wird eine Rückgabevariable erstellt und auf einen bestimmten Wert festgelegt.

> [!NOTE]
> Die **SetReturnVar** -Aktion ist nur in datenmakros verfügbar.

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
<td><p>Ausdruck</p></td>
<td><p>Ja</p></td>
<td><p>Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird. Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran. Sie können auf die <strong>Generator</strong> -Schaltfläche klicken, um den <strong>Ausdrucks-Generator</strong> zum Festlegen dieses Arguments zu verwenden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die **SetReturnVar** -Aktion wird verwendet, um eine **ReturnVar**zu erstellen, die von Makros verwendet werden kann, die ein datenmakro mithilfe der **ausführendatenmakro** -Aktion aufrufen.

Nachdem ein **ReturnVar** durch die **SetReturnVar** -Aktion erstellt wurde, kann es in einem Ausdruck vom aufrufenden Makro verwendet werden. Wenn Sie beispielsweise einen **ReturnVar** mit dem Namen **UpdateSuccess**erstellt haben, können Sie die Variable mithilfe der folgenden Syntax verwenden:

```vb
    =[ReturnVars]![UpdateSuccess]
```

Die **SetReturnVar** -Aktion kann nur in benannten datenmakros verwendet werden. Sie ist in datenmakros, die an ein datenmakro Ereignis angefügt sind, nicht verfügbar.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie die SetReturnVar-Aktion verwenden, um einen Wert aus einem benannten datenmakro zurückzugeben. Ein ReturnVar mit dem Namen **CurrentServiceRequest** wird an das Makro oder die VBA-Unterroutine (Visual Basic für Applikationen) zurückgegeben, die das benannte datenmakro aufgerufen hat.

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
