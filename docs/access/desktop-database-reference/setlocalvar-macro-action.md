---
title: SetLocalVar-Makroaktion
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: d552874568fe0e081ab4fe86e4f8a73c36281bc7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580846"
---
# <a name="setlocalvar-macro-action"></a>SetLocalVar-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **FestlegenLokaleVar**-Aktion erstellen Sie eine temporäre Variable und legen diese auf einen bestimmten Wert fest.

## <a name="setting"></a>Einstellung

Die **FestlegenLokaleVar**-Aktion kann mit den folgenden Argumenten verwendet werden.

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
<td><p><strong>Name</strong></p></td>
<td><p>Ja</p></td>
<td><p>Eine Zeichenfolge, die den Namen der Variablen angibt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ausdruck</strong></p></td>
<td><p>Ja</p></td>
<td><p>Ein Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen. Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran. Sie können auf die Schaltfläche <strong>Erstellen</strong> klicken, um dieses Argument mithilfe des <strong>Ausdrucks-Generators</strong> festzulegen.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Bemerkungen

Mit der **FestlegenLokaleVar** -Aktion festgelegte Variablen können nur in dem Makro verwendet werden, in dem sie definiert sind. Verwenden Sie die **[FestlegenTempVar](settempvar-macro-action.md)** -Aktion, um eine Variable zu definieren, die in einem anderen Makro, einer Ereignisprozedur, einem Formular oder einem Bericht verwendet werden kann.

Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> In einem Datenmakro müssen Sie nicht die LocalVars-Sammlung verwenden, um auf eine Variable zu verweisen. Wenn Sie beispielsweise eine temporäre Variable namens "TotalAmount" in einem Datenmakro verwenden, können Sie die Variable über die folgende Syntax als Steuerelementquelle für ein Textfeld verwenden: `=[TotalAmount]`.

