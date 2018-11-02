---
title: Wenn...Dann...Sonst-Makroblock
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c671ced7d3de2ce461af3bcf0a5d832e092bbf17
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922937"
---
# <a name="ifthenelse-macro-block"></a>Wenn...Dann...Sonst-Makroblock


**Betrifft**: Access 2013, Office 2013

Mit dem **If** -Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.

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

**Wenn** sowohl **Sonst wenn**sind die folgenden Argumente erforderlich.

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
<td><p><strong>Expression</strong></p></td>
<td><p>Die Bedingung, die Sie testen möchten. Es muss ein Ausdruck, der True oder False ausgewertet wird.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Wenn Sie den If-Makroblock auswählen, wird ein Textfeld angezeigt, sodass Sie einen Ausdruck eingeben können, der die Bedingung darstellt, auf die Sie testen möchten. Zudem wird ein Kombinationsfeld angezeigt, in dem Sie eine Makroaktion einfügen können. Darunter wird automatisch der Text "End If" angezeigt. "If" und "End If" begrenzen einen Bereich, in dem Sie eine Gruppe oder einen Block von Aktionen eingeben können. Der Block wird nur ausgeführt, wenn der von Ihnen eingegebene Ausdruck True ist.

Um einen anderen Ausdruck auswerten, wenn der erste Ausdruck auf false festgelegt ist, können Sie **Andere Person hinzufügen Wenn** , um einen optionalen **Else If** -Block einzufügen klicken. Sie müssen einen Ausdruck, der ausgewertet wird auf True oder False, eingeben. -Block wird in diesem Fall nur, wenn der Ausdruck True ist und der erste Ausdruck False ist.

In einem If-Block können Sie beliebig viele Else If-Blöcke eingeben.

Sie können auf **Add Else** klicken, um einen optionalen **Else** -Block hinzuzufügen. In diesem Fall bilden die unter **Else** eingegebenen Aktionen den **Else** -Block, der nur ausgeführt wird, wenn die darüber angegebenen Aktionen nicht ausgeführt werden. Einem **If** -Block können Sie nur einen **Else** -Block hinzufügen.

Im folgenden Codebeispiel wird die Makroaktionen in der erste Block ausgeführt werden, wenn der Wert der \[Status\] größer als 0 ist. Wenn der Wert der \[Status\] ist nicht größer als 0 ist, wird der Ausdruck, der die **Sonst wenn** befolgt ausgewertet. Die Makroaktionen im **Else If** -Block ausgeführt werden, wenn der Wert der \[Status\] ist gleich 0. Wenn letztlich weder der erste noch der zweite Block ausgeführt wird, werden die Aktionen im **Else** -Block ausgeführt.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

Sie können **Wenn** Blöcke schachteln. Sie sollten einen **If** -Block innerhalb einer **If** -Block schachteln, wenn Sie möchten einen zweiten Ausdruck ausgewertet werden soll, wenn der erste Ausdruck true festgelegt ist. Im folgenden Codebeispiel wird der innere **If** -Block nur wird ausgeführt, wenn der Wert der \[Status\] ist sowohl größer als 0 *und* größer als 100.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
