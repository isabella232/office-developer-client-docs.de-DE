---
title: RemoveTempVar-Makroaktion
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5051cfd74f2a745ee430f2ed8a20445d2f9965f3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716306"
---
# <a name="removetempvar-macro-action"></a>RemoveTempVar-Makroaktion


**Betrifft**: Access 2013, Office 2013



Mit der **EntfernenTempVar** -Aktion können Sie eine einzelne mit der **FestlegenTempVar** -Aktion erstellte temporäre Variable entfernen.

## <a name="setting"></a>Einstellung

Die **EntfernenTempVar** -Aktion hat das folgende Argument.

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
<td><p><strong>Name</strong></p></td>
<td><p>Geben Sie den Namen der zu entfernenden temporären Variable ein.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

  - Es können bis zu 255 temporäre Variablen gleichzeitig definiert sein. Wenn eine temporäre Variable nicht entfernt wird, verbleibt diese bis zum Schließen der Datenbank im Arbeitsspeicher. Es empfiehlt sich, temporäre Variablen zu entfernen, sobald Sie deren Verwendung beendet haben.

  - Beim Schließen der Datenbank oder des Projekts werden von Access automatisch alle temporären Variablen entfernt.

  - Wenn der Name der zu entfernenden Variable falsch geschrieben wird, wird von Access kein Fehler angezeigt. Die zu entfernende Variable verbleibt bis zum Schließen der Datenbank im Arbeitsspeicher.

  - Wenn Sie mehr als eine temporäre Variable erstellt haben und alle gleichzeitig entfernt werden sollen, verwenden Sie die **EntfernenAlleTempVar** -Aktion.

  - Verwenden Sie zum Ausführen der **EntfernenTempVar** -Aktion in einem VBA-Modul die **Remove** -Methode des **TempVars** -Objekts.

## <a name="example"></a>Beispiel

Im folgenden Makro wird die Vorgehensweise zum Erstellen einer temporären Variable, zum Verwenden der Variable in einer Bedingung und einem Meldungsfeld und zum anschließenden Entfernen der temporären Variable mit der **EntfernenTempVar** -Aktion gezeigt.

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
<td><p><strong>Name</strong>: Meinevar<strong>Ausdruck</strong>: InputBox (&quot;Geben Sie eine Zahl ungleich NULL.&quot;)</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]! [Meinevar] &lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Meldung</strong>: =&quot;eingegebene &quot; &amp; [TempVars]! [Meinevar] &amp; &quot;. &quot; <strong>Signalton</strong>: <strong>YesType</strong>: <strong>Informationen</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>EntfernenTempVar</strong></p></td>
<td><p><strong>Name</strong>: MeineVar</p></td>
</tr>
</tbody>
</table>

