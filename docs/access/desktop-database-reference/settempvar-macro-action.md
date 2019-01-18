---
title: SetTempVar-Makroaktion
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705230"
---
# <a name="settempvar-macro-action"></a>SetTempVar-Makroaktion


**Betrifft**: Access 2013, Office 2013



Sie können die **FestlegenTempVar** -Aktion verwenden, um eine temporäre Variable zu erstellen und auf einen bestimmten Wert festzulegen. Die Variable kann dann als Bedingung oder Argument in nachfolgenden Aktionen verwendet werden. Sie können die Variable auch in einem anderen Makro, in einer Ereignisprozedur oder in einem Formular bzw. Bericht verwenden.

## <a name="setting"></a>Einstellung

Die **FestlegenTempVar** -Aktion verwendet die folgenden Argumente.

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
<td><p>Geben Sie den Namen der temporären Variable ein.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ausdruck</strong></p></td>
<td><p>Geben Sie einen Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen. Setzen Sie den Ausdruck mit dem Gleichheitszeichen (<strong>=</strong>) anmelden. Klicken Sie auf die <strong>Generator</strong> -Schaltfläche <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> , um das Argument mithilfe des Ausdrucks-Generators festzulegen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

- Es können bis zu 255 temporäre Variablen gleichzeitig definiert sein. Eine temporäre Variable, die Sie nicht entfernen, verbleibt bis zum Schließen der Datenbank im Speicher. Es empfiehlt sich, temporäre Variablen zu entfernen, die nicht mehr benötigt werden. Wenn Sie eine einzelne temporäre Variable entfernen möchten, verwenden Sie die **[EntfernenTempVar](removetempvar-macro-action.md)** -Aktion. Legen Sie deren Argument auf den Namen der temporären Variable fest, die entfernt werden soll. Falls Sie mit mehreren temporären Variablen arbeiten und alle gleichzeitig entfernen möchten, verwenden Sie die **EntfernenAlleTempVar** -Aktion.

- Temporäre Variablen sind global. Nachdem eine temporäre Variable erstellt wurde, können Sie es in einer Ereignisprozedur einem Visual Basic für Applikationen (VBA) Modul, einer Abfrage oder einem Ausdruck verweisen. Angenommen, wenn Sie eine temporäre Variable mit dem Namen *Meinevar*erstellt, können die Variable als Steuerelementinhalt für ein Textfeld Sie mithilfe der folgenden Syntax:
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > [!HINWEIS] In Makros, Abfragen und Ereignisprozeduren müssen Sie dem Ausdruck kein Gleichheitszeichen voranstellen.
 
  Sie können in allen Add-Ins und referenzierten Datenbanken auf temporäre Variablen verweisen.

- Wenn Sie die **FestlegenTempVar** -Aktion in einem VBA-Modul ausführen möchten, verwenden Sie die **Add** -Methode des Objekts **TempVars**.

## <a name="example"></a>Beispiel

Das folgende Makro veranschaulicht, wie Sie mithilfe der **FestlegenTempVar** -Aktion eine temporäre Variable erstellen, diese dann in einer Bedingung und einem Meldungsfeld verwenden und sie anschließend entfernen.

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

