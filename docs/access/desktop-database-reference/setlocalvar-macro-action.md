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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702460"
---
# <a name="setlocalvar-macro-action"></a>SetLocalVar-Makroaktion

**Betrifft**: Access 2013, Office 2013

Mit der **FestlegenLokaleVar** -Aktion erstellen Sie eine temporäre Variable und legen diese auf einen bestimmten Wert fest.

## <a name="setting"></a>Einstellung

Die **FestlegenLokaleVar** -Aktion kann mit den folgenden Argumenten verwendet werden.

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
<td><p><strong>Name</strong></p></td>
<td><p>Ja</p></td>
<td><p>Eine Zeichenfolge, die den Namen der Variablen angibt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ausdruck</strong></p></td>
<td><p>Ja</p></td>
<td><p>Ein Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen. Setzen Sie den Ausdruck mit dem Gleichheitszeichen (=). Sie können klicken Sie auf die Schaltfläche <strong>Erstellen</strong> , um den <strong>Ausdrucks-Generator</strong> verwenden, um dieses Argument festzulegen.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Hinweise

Mit der **FestlegenLokaleVar** -Aktion festgelegte Variablen können nur in dem Makro verwendet werden, in dem sie definiert sind. Verwenden Sie die **[FestlegenTempVar](settempvar-macro-action.md)** -Aktion, um eine Variable zu definieren, die in einem anderen Makro, einer Ereignisprozedur, einem Formular oder einem Bericht verwendet werden kann.

Auf eine erstellte temporäre Variable können Sie in einem Ausdruck verweisen. Wenn Sie beispielsweise die temporäre Variable Gesamtmenge erstellt haben, können Sie diese mithilfe der folgenden Syntax als Steuerelementquelle für ein Textfeld verwenden:

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> In einem Makro Daten müssen Sie keinen die LocalVars-Auflistung verwenden, um auf eine Variable verweisen. Angenommen, wenn Sie eine temporäre Variable eines Datenmakros, mit dem Namen TotalAmount erstellt haben, können die Variable als der Steuerelementquelle für ein Textfeld mit der folgenden Syntax: `=[TotalAmount]`.

