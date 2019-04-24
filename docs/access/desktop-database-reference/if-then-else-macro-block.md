---
title: Wenn...Dann...Sonst-Makroblock
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fb6cbd6cc925a3e4841d9e7d6d77332cc36c7a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291894"
---
# <a name="ifthenelse-macro-block"></a>Wenn...Dann...Sonst-Makroblock


**Gilt für**: Access 2013, Office 2013

Mit dem **If**-Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a>Einstellung

Für **If** und für **Else If** sind jeweils die folgenden Argumente erforderlich.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Ausdruck</strong></p></td>
<td><p>Die Bedingung, die Sie testen möchten. Dies muss ein Ausdruck sein, der als "Wahr" oder "Falsch" ausgewertet wird.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn Sie den **If**-Makroblock auswählen, wird ein Textfeld eingeblendet, damit Sie einen Ausdruck zur Darstellung der Bedingung eingeben können, die Sie testen möchten. Darüber hinaus wird ein Kombinationsfeld angezeigt. Sie können darin eine Makroaktion einfügen, unter der der Text "End If" automatisch angezeigt wird. Das "If" und das "End If" klammern einen Bereich ein, in dem Sie eine Gruppe (Block) von Aktionen eingeben können. Der Block wird nur ausgeführt, wenn der eingegebene Ausdruck "Wahr" ist.

To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.

Sie können einem "If"-Block beliebig viele **Else If**-Blöcke hinzufügen.

Sie können auf **Add Else** klicken, um einen optionalen **Else** -Block hinzuzufügen. In diesem Fall bilden die unter **Else** eingegebenen Aktionen den **Else** -Block, der nur ausgeführt wird, wenn die darüber angegebenen Aktionen nicht ausgeführt werden. Einem **If** -Block können Sie nur einen **Else** -Block hinzufügen.

Im folgenden Codebeispiel werden die Makroaktionen im ersten Block ausgeführt, wenn der Wert von \[Status\] größer als 0 ist. Wenn der Wert von \[Status\] nicht größer als 0 ist, wird der Ausdruck nach **Else If** ausgewertet. Die Makroaktionen im **Else If**-Block werden ausgeführt, wenn der Wert von \[Status\] gleich 0 ist. Und schließlich: Wenn weder der erste noch der zweite Block ausgeführt werden, werden die Aktionen im **Else**-Block ausgeführt.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

Sie können **If**-Blöcke schachteln. Das Schachteln eines **If**-Blocks in einem **If**-Block sollten Sie erwägen, um einen zweiten Ausdruck auszuwerten, wenn der erste Ausdruck "Wahr" ist. Im nachstehenden Codebeispiel wird der innere **If**-Block nur dann ausgewertet, wenn der Wert von \[Status\] größer als "0" *and* größer als "100" ist.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
