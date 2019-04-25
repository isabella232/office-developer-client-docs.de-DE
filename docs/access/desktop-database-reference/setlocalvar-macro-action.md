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
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314588"
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
<td><p>Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird. Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran. Sie können auf die Schaltfläche <strong>Erstellen</strong> klicken, um das Argument mithilfe des <strong>Ausdrucks-Generators</strong> festzulegen.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Bemerkungen

Mit der **FestlegenLokaleVar** -Aktion festgelegte Variablen können nur in dem Makro verwendet werden, in dem sie definiert sind. Verwenden Sie die **[FestlegenTempVar](settempvar-macro-action.md)** -Aktion, um eine Variable zu definieren, die in einem anderen Makro, einer Ereignisprozedur, einem Formular oder einem Bericht verwendet werden kann.

Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> In einem Datenmakro müssen Sie nicht die LocalVars-Sammlung verwenden, um auf eine Variable zu verweisen. Wenn Sie beispielsweise eine temporäre Variable namens "TotalAmount" in einem Datenmakro verwenden, können Sie die Variable über die folgende Syntax als Steuerelementquelle für ein Textfeld verwenden: `=[TotalAmount]`.

