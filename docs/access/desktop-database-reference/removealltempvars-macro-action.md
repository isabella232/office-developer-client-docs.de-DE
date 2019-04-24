---
title: RemoveAllTempVars-Makroaktion
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: eade809a6e3982dc0dc4cf94ae382af72e8f454e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306797"
---
# <a name="removealltempvars-macro-action"></a>RemoveAllTempVars-Makroaktion


**Gilt für**: Access 2013, Office 2013


Mit der **EntfernenAlleTempVar**-Aktion können Sie alle mit der **FestlegenTempVar**-Aktion erstellten temporären Variablen entfernen.

## <a name="setting"></a>Einstellung

Die **EntfernenAlleTempVar**-Aktion hat keine Argumente.

## <a name="remarks"></a>Bemerkungen

  - Es können bis zu 255 temporäre Variablen gleichzeitig definiert sein. Wenn eine temporäre Variable nicht entfernt wird, verbleibt diese bis zum Schließen der Datenbank oder des Projekts im Arbeitsspeicher. Es empfiehlt sich, temporäre Variablen zu entfernen, sobald Sie deren Verwendung beendet haben.

  - Beim Schließen der Datenbank oder des Projekts werden von Access automatisch alle temporären Variablen entfernt.

  - Verwenden Sie zum Entfernen einer einzelnen temporären Variable die **EntfernenTempVar** -Aktion, und legen Sie die Argumente auf den Namen der zu entfernenden temporären Variable fest.

  - Verwenden Sie zum Ausführen der **EntfernenAlleTempVar** -Aktion in einem VBA-Modul die **RemoveAll** -Methode des **TempVars** -Objekts.

## <a name="example"></a>Beispiel

Im folgenden Makro wird die Vorgehensweise zum Erstellen einer temporären Variable, zum Verwenden der Variable in einer Bedingung und einem Meldungsfeld und zum folgenden Entfernen der Variable mit der **EntfernenAlleTempVar** -Aktion gezeigt.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bedingung</p></th>
<th><p>Aktion</p></th>
<th><p>Argumente</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>FestlegenTempVar</strong></p></td>
<td><p><strong>Name</strong>: MeineVar<strong>Ausdruck</strong>: InputBox (&quot;geben Sie eine Zahl ungleich NULL&quot;ein.)</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]! MeineVar &lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Meldung</strong>: =&quot;Sie haben &quot; &amp; [TempVars] eingegeben! MeineVar &amp; &quot;. &quot; <strong>Beep</strong>: <strong>jatyp</strong>: <strong>Informationen</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>EntfernenAlleTempVar</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

