---
title: AbbrechenEreignis-Makroaktion
TOCTitle: CancelEvent Macro Action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0bc9f38e1f91a58fcfc7cedfdfb740a22477f649
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880670"
---
# <a name="cancelevent-macro-action"></a>AbbrechenEreignis-Makroaktion


**Betrifft**: Access 2013, Office 2013


Die **AbbrechenEreignis** -Aktion können Sie das Ereignis abzubrechen, das Zugriff auf das Makro mit dieser Aktion ausgeführt. Der Name des Makros ist die Einstellung einer Ereigniseigenschaft wie **BeforeUpdate**, **OnOpen**, **OnUnload**oder **OnPrint**.

## <a name="setting"></a>Einstellung

Die **AbbrechenEreignis** -Aktion hat keine Argumente.

## <a name="remarks"></a>Hinweise

In einem Formular verwenden Sie die **AbbrechenEreignis** -Aktion üblicherweise in einem Gültigkeitsprüfungsmakro mit der **VorAktualisierung** -Ereigniseigenschaft. Wenn ein Benutzer Daten in ein Steuerelement oder in einen Datensatz eingibt, führt Access zunächst das Makro aus und fügt dann der Datenbank die Daten hinzu. Wenn die Daten die Bedingungen der Gültigkeitsprüfung im Makro nicht erfüllen, bricht die **AbbrechenEreignis** -Aktion den Aktualisierungsvorgang vor dem Starten ab.

Diese Aktion wird häufig zusammen mit der **Meldungsfeld** -Aktion verwendet, um anzugeben, dass die Daten die Bedingungen der Gültigkeitsprüfung nicht erfüllen, und um nützliche Informationen zu der Art von Daten bereitzustellen, die eingegeben werden sollen.

Die folgenden Ereignisse können von der **AbbrechenEreignis** -Aktion abgebrochen werden.

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
<td><p><strong>Open</strong></p></td>
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
<td><p><strong>Delete</strong></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!HINWEIS] Sie können die **AbbrechenEreignis** -Aktion mit dem **MouseDown** -Ereignis nur dazu verwenden, das Ereignis abzubrechen, das beim Klicken mit der rechten Maustaste auftritt.

Wenn die **BeimDoppelklicken** -Ereigniseigenschaft ein Makro angibt, das die **AbbrechenEreignis** -Aktion enthält, wird durch diese Aktion das **DblClick** -Ereignis abgebrochen.

Nachdem das Makro für das Ereignis ausgeführt wurde, tritt für Ereignisse, die abgebrochen werden können, das Standardverhalten für das Ereignis ein (d. h. das Verhalten, das Access normalerweise zeigt, wenn das Ereignis eintritt). Auf diese Weise können Sie das Standardverhalten abbrechen. Wenn Sie beispielsweise auf ein Wort doppelklicken, auf dem sich die Einfügemarke in einem Textfeld befindet, wird das Wort normalerweise in Access markiert. Sie können dieses Standardverhalten in dem Makro für das **DblClick** -Ereignis abbrechen und eine andere Aktion ausführen, z. B. das Öffnen eines Formulars, das Information zu den Daten in dem Textfeld enthält. Für Ereignisse, die nicht abgebrochen werden können, tritt das Standardverhalten ein, bevor das Makro ausgeführt wird.

> [!NOTE]
> [!HINWEIS] Wenn die **BeiEntladen** -Ereigniseigenschaft eines Formulars ein Makro angibt, das eine **AbbrechenEreignis** -Aktion ausführt, können Sie das Formular nicht schließen. Sie müssen entweder die Bedingung berichtigen, die das Ausführen der **AbbrechenEreignis** -Aktion verursacht hat, oder das Makro öffnen und die **AbbrechenEreignis** -Aktion löschen. Wenn es sich bei dem Formular um ein modales Formular handelt, können Sie das Makro nicht öffnen.

Verwenden Sie die **CancelEvent** -Methode des **DoCmd** -Objekts, um die **AbbrechenEreignis** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

## <a name="example"></a>Beispiel

 Überprüfen der Gültigkeit von Daten mithilfe eines Makros

Mit dem folgenden Gültigkeitsprüfungsmakro werden die Postleitzahlen überprüft, die im Formular Lieferanten eingegeben werden. Es zeigt die Verwendung der Aktionen StoppMakro, Meldungsfeld, AbbrechenEreignis und GeheZuSteuerelement. Mit einem Bedingungsausdruck werden das Land, die Region und die Postleitzahl überprüft, die im Formular in einem Datensatz eingegeben werden. Wenn die Postleitzahl nicht das richtige Format für das Land oder die Region aufweist, wird vom Makro ein Meldungsfeld angezeigt, und das Speichern des Datensatzes wird abgebrochen. Sie kehren dann zum Steuerelement Postleitzahl zurück, in dem Sie den Fehler korrigieren können. Dieses Makro sollte mit der BeforeUpdate-Eigenschaft des Formulars Lieferanten verbunden sein.

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
<td><p>Wenn Land/Region den Wert Null hat, kann die Postleitzahl nicht überprüft werden.</p></td>
</tr>
<tr class="even">
<td><p>[Land/Region] In (&quot;Frankreich&quot;,&quot;Italien&quot;,&quot;Spanien&quot;) und Len ([Postleitzahl]) &lt; &gt; 5</p></td>
<td><p>MessageBox</p></td>
<td><p>Meldung: Die Postleitzahl muss 5 Zeichen lang sein. 

 Signalton: <strong>Ja</strong> Typ: <strong>Informationen</strong> Titel: Postleitzahl fehlerhaft</p></td>
<td><p>Zeigt eine Meldung an, wenn die Postleitzahl nicht 5 Zeichen lang ist.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
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
<td><p>[Land/Region] In (&quot;Australien&quot;,&quot;Singapur&quot;) und Len ([Postleitzahl]) &lt; &gt; 4</p></td>
<td><p>MessageBox</p></td>
<td><p>Meldung: Die Postleitzahl muss 4 Zeichen lang sein. 

 Signalton: <strong>Ja</strong> Typ: <strong>Informationen</strong> Titel: Postleitzahl fehlerhaft</p></td>
<td><p>Zeigt eine Meldung an, wenn die Postleitzahl nicht 4 Zeichen lang ist.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
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
<td><p>([Land/Region] = &quot;Kanada&quot;) Und ([Postleitzahl] nicht wie&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
<td><p>MessageBox</p></td>
<td><p>Meldung: Die Postleitzahl ist ungültig. Beispiel für Kanadische Code: H1J 1 c 3 Signalton: <strong>Ja</strong> Typ: <strong>Informationen</strong> Titel: Postleitzahl Codefehler</p></td>
<td><p>Zeigt eine Meldung an, wenn eine für Kanada ungültige Postleitzahl angegeben wird. (Beispiel für eine kanadische Postleitzahl: H1J 1C3).</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
</tbody>
</table>

