---
title: CancelEvent-Makroaktion
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a1f5882119a52c0c3f73d4d4da96e4e8ec8f8377
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558597"
---
# <a name="cancelevent-macro-action"></a>CancelEvent-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **CancelEvent-Aktion** verwenden, um das Ereignis abzubrechen, durch das Access das Makro ausgeführt hat, das diese Aktion enthält. Der Makroname entspricht der Einstellung einer Ereigniseigenschaft, z. B. **VorAktualisierung**, **BeimÖffnen**, **BeiEntladen** oder **BeimDrucken**.

## <a name="setting"></a>Einstellung

Die **AbbrechenEreignis**-Aktion hat keine Argumente.

## <a name="remarks"></a>HinwBemerkungeneise

In einem Formular verwenden Sie die **AbbrechenEreignis**-Aktion üblicherweise in einem Gültigkeitsprüfungsmakro mit der **VorAktualisierung**-Ereigniseigenschaft. Wenn ein Benutzer Daten in ein Steuerelement oder in einen Datensatz eingibt, führt Access zunächst das Makro aus und fügt dann der Datenbank die Daten hinzu. Wenn die Daten die Bedingungen der Gültigkeitsprüfung im Makro nicht erfüllen, bricht die **AbbrechenEreignis**-Aktion den Aktualisierungsvorgang vor dem Starten ab.

Diese Aktion wird häufig zusammen mit der **Meldungsfeld** -Aktion verwendet, um anzugeben, dass die Daten die Bedingungen der Gültigkeitsprüfung nicht erfüllen, und um nützliche Informationen zu der Art von Daten bereitzustellen, die eingegeben werden sollen.

Die folgenden Ereignisse können von der **AbbrechenEreignis**-Aktion abgebrochen werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Dirty</strong></p></td>
<td><p><strong>MouseDown</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeDelConfirm</strong></p></td>
<td><p><strong>Exit</strong></p></td>
<td><p><strong>NoData</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>BeforeInsert</strong></p></td>
<td><p><strong>Filter</strong></p></td>
<td><p><strong>Öffnen</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeUpdate</strong></p></td>
<td><p><strong>Format</strong></p></td>
<td><p><strong>Print</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>DblClick</strong></p></td>
<td><p><strong>KeyPress</strong></p></td>
<td><p><strong>Unload</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Löschen</strong></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Sie können die **AbbrechenEreignis**-Aktion mit dem **MouseDown**-Ereignis nur dazu verwenden, das Ereignis abzubrechen, das beim Klicken mit der rechten Maustaste auftritt.

Wenn die **BeimDoppelklicken**-Ereigniseigenschaft ein Makro angibt, das die **AbbrechenEreignis**-Aktion enthält, wird durch diese Aktion das **DblClick**-Ereignis abgebrochen.

Nachdem das Makro für das Ereignis ausgeführt wurde, tritt für Ereignisse, die abgebrochen werden können, das Standardverhalten für das Ereignis ein (d. h. das Verhalten, das Access normalerweise zeigt, wenn das Ereignis eintritt). Auf diese Weise können Sie das Standardverhalten abbrechen. Wenn Sie beispielsweise auf ein Wort doppelklicken, auf dem sich die Einfügemarke in einem Textfeld befindet, wird das Wort normalerweise in Access markiert. Sie können dieses Standardverhalten in dem Makro für das **DblClick** -Ereignis abbrechen und eine andere Aktion ausführen, z. B. das Öffnen eines Formulars, das Information zu den Daten in dem Textfeld enthält. Für Ereignisse, die nicht abgebrochen werden können, tritt das Standardverhalten ein, bevor das Makro ausgeführt wird.

> [!NOTE]
> [!HINWEIS] Wenn die **BeiEntladen** -Ereigniseigenschaft eines Formulars ein Makro angibt, das eine **AbbrechenEreignis** -Aktion ausführt, können Sie das Formular nicht schließen. Sie müssen entweder die Bedingung berichtigen, die das Ausführen der **AbbrechenEreignis** -Aktion verursacht hat, oder das Makro öffnen und die **AbbrechenEreignis** -Aktion löschen. Wenn es sich bei dem Formular um ein modales Formular handelt, können Sie das Makro nicht öffnen.

Verwenden Sie die **CancelEvent**-Methode des **DoCmd**-Objekts, um die **AbbrechenEreignis**-Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

## <a name="example"></a>Beispiel

Überprüfen der Gültigkeit von Daten mithilfe eines Makros

The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record. It then returns you to the Postal Code control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bedingung</p></th>
<th><p>Aktion</p></th>
<th><p>Argumente: Einstellung</p></th>
<th><p>Kommentar</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IsNull([CountryRegion])</p></td>
<td><p>StopMacro</p></td>
<td><p></p></td>
<td><p>Wenn CountryRegion <strong>null</strong>ist, kann die Postleitzahl nicht überprüft werden.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In ( &quot; Frankreich , Italien , Spanien ) und &quot; &quot; &quot; &quot; &quot; Len([Postleitzahl]) &lt; &gt; 5</p></td>
<td><p>MessageBox</p></td>
<td><p>Meldung: Die Postleitzahl muss 5 Zeichen lang sein. Signalton: <strong>Ja</strong> Typ: <strong>Informationstitel:</strong> Postleitzahl-Fehler</p></td>
<td><p>Zeigt eine Meldung an, wenn die Postleitzahl nicht 5 Zeichen lang ist.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>AbbrechenEreignis</p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Steuerelementname: Postleitzahl</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In ( &quot; Australien , Singapur ) und &quot; &quot; &quot; Len([Postleitzahl]) &lt; &gt; 4</p></td>
<td><p>MessageBox</p></td>
<td><p>Meldung: Die Postleitzahl muss 4 Zeichen lang sein. Signalton: <strong>Ja</strong> Typ: <strong>Informationstitel:</strong> Postleitzahl-Fehler</p></td>
<td><p>Zeigt eine Meldung an, wenn die Postleitzahl nicht 4 Zeichen lang ist.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p>AbbrechenEreignis</p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Steuerelementname: Postleitzahl</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Kanada &quot; ) und ([Postleitzahl] nicht wie &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p>MessageBox</p></td>
<td><p>Meldung: Die Postleitzahl ist ungültig. Beispiel für kanadischen Code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</p></td>
<td><p>Zeigt eine Meldung an, wenn eine für Kanada ungültige Postleitzahl angegeben wird. (Beispiel für eine kanadische Postleitzahl: H1J 1C3).</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>AbbrechenEreignis</p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
</tbody>
</table>

