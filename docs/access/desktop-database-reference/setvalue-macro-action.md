---
title: SetValue-Makroaktion
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 7228c7ccac02cea2c959f968c0e24e1bdfdefadd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617440"
---
# <a name="setvalue-macro-action"></a>SetValue-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die Aktion **SetzenWert** verwenden, um den Wert eines Microsoft Access-Felds, eines Steuerelements oder einer Eigenschaft in einem Formular, einem Formulardatenblatt oder einen Bericht festzulegen.

> [!NOTE]
> - Sie können die Aktion **SetzenWert** nicht verwenden, um den Wert einer Access-Eigenschaft festzulegen, die ein Objekt zurückgibt.
> - Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die Aktion **SetzenWert** kann mit den folgenden Argumenten verwendet werden.

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
<td><p><strong>Item</strong></p></td>
<td><p>Der Name des Felds, des Steuerelements oder der Eigenschaft, dessen bzw. deren Wert Sie festlegen möchten. Geben Sie den Namen des Felds, des Steuerelements oder der Eigenschaft im Abschnitt <strong>Aktionsargument </strong> des Makro-Generators in das Feld <strong>Element </strong> ein. Verwenden Sie die vollständige Syntax, um auf dieses Element verweisen, z. B.  <em>Steuerelementname </em> (für ein Steuerelement im Formular oder Bericht, in dem das Makro aufgerufen wurde) oder <strong>Formulare</strong>!<em>Formularname</em>!<em>Steuerelementname</em>. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ausdruck</strong></p></td>
<td><p>Der Ausdruck, den Access verwendet, um den Wert für dieses Element festzulegen. Sie müssen immer die vollständige Syntax verwenden, um auf Objekte im Ausdruck zu verweisen. Um beispielsweise den Wert eines Steuerelements für das Gehalt in einem Formular für Mitarbeiter um 10 Prozent zu erhöhen, verwenden Sie Forms!Employees!Salary*1.1. Dies ist ein erforderliches Argument.</p><p><strong>HINWEIS</strong>: Sie sollten kein Gleichheitszeichen (=) vor dem Ausdruck in diesem Argument verwenden. Wenn Sie dies tun, wertet Access den Ausdruck aus und verwendet diesen Wert dann als Ausdruck in diesem Argument. Dies kann zu unerwarteten Ergebnissen führen, wenn der Ausdruck eine Zeichenfolge ist.</p>
<p>Wenn Sie z. B. <strong>=&quot;String1&quot;</strong> für dieses Argument eingeben, wertet Access zuerst den Ausdruck als String1 aus. Anschließend wird String1 als Ausdruck in diesem Argument verwendet und es wird erwartet, dass ein Steuerelement oder eine Eigenschaft mit dem Namen String1 im Formular oder Bericht gefunden wird, das bzw. der das Makro aufgerufen hat.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Klicken Sie in einer Access-Datenbank (MDB oder ACCDB) auf die Schaltfläche **Erstellen**, um den Ausdrucks-Generator zum Erstellen eines Ausdrucks für eines dieser Argumente zu verwenden.

## <a name="remarks"></a>Hinweise

Sie können diese Aktion verwenden, um einen Wert für ein Feld oder Steuerelement in einem Formular, einem Formulardatenblatt oder einem Bericht festzulegen. Sie können außerdem den Wert für nahezu alle Steuerelement-, Formular- und Berichtseigenschaften in jeder Ansicht festlegen. Informationen dazu, ob eine bestimmte Eigenschaft mit einem Makro und in welchen Ansichten die Eigenschaft festgelegt werden kann, finden Sie im Hilfethema für die jeweilige Eigenschaft im Visual Basic-Editor.

Sie können den Wert für ein Feld auch dann in der zugrunde liegenden Tabelle eines Formulars festlegen, wenn das Formular kein an das Feld gebundenes Steuerelement enthält. Verwenden Sie die Syntax **Formulare**\!*Formularnamen*\!*Feldnamens* im Feld **Element**, um den Wert für ein solches Feld festzulegen. Sie können auch auf ein Feld in der zugrunde liegenden Tabelle eines Berichts verweisen, indem Sie die Syntax **Berichte**\!*Berichtsname*\!*Feldname* verwenden. Es muss jedoch ein Steuerelement für den Bericht vorhanden sein, das an dieses Feld gebunden ist, oder auf das Feld muss in einem berechneten Steuerelement im Bericht verwiesen werden.

Wenn Sie den Wert eines Steuerelements in einem Formular festlegen, löst die Aktion **SetzenWert** nicht die Gültigkeitsprüfungsregeln auf Formularebene des Steuerelements, sondern die Gültigkeitsprüfungsregeln auf Tabellenebene des zugrunde liegendenen Felds aus, wenn das Steuerelement ein gebundenes Steuerelement ist. Die Aktion **SetzenWert** löst außerdem eine Neuberechnung aus, die aber nicht unbedingt sofort erfolgt. Um eine sofortige Aktualisierung auszulösen und den Abschluss der Neuberechnung zu erzwingen, verwenden Sie die Aktion **AktualisierenObjekt**. Der Wert, den Sie in einem Steuerelement mithilfe der Aktion **SetzenWert** festlegen, wird außerdem nicht vom Eingabeformat beeinflusst, das in der Eigenschaft **InputMask** des Steuerelements oder zugrunde liegenden Felds festgelegt ist.

Um den Wert eines Steuerelements zu ändern, können Sie die Aktion **SetzenWert** Aktion in einem Makro verwenden, das durch die Ereigniseigenschaft **NachAktualisierung** des Steuerelements angegeben ist. Sie können Aktion **SetzenWert** jedoch nicht in einem Makro verwenden, das durch die Ereigniseigenschaft **VorAktualisierung** eines Steuerelements angegeben ist, um den Wert des Steuerelements zu ändern (Sie können die Aktion **SetzenWert** aber zum Ändern des Werts anderer Steuerelemente verwenden). Sie können die Aktion **SetzenWert** außerdem in einem von der Eigenschaft **VorAktualisieurng** oder **NachAktualisierung** eines Formulars angegebenem Makro verwenden, um den Wert eines beliebigen Steuerelements im aktuellen Datensatz zu ändern.

> [!NOTE]
> Die Werte der folgenden Steuerelemente können nicht mit der Aktion **SetzenWert** festgelegt werden:
> - Gebundene Steuerelemente und berechnete Steuerelemente in Berichten
> - Berechnete Steuerelemente in Formularen

> [!TIP]
> Sie können die Aktion **SetValue** verwenden, um ein Formular in der Formularansicht auszublenden oder anzuzeigen. Geben Sie **Formulare**!*Formularname***.Sichtbar}** im Feld **Element** und **Nein** oder **Ja** im Feld **Ausdruck** an. Wenn Sie die Eigenschaft **Sichtbar** eines modalen Formulars auf **Nein** festlegen, wird das Formular ausgeblendet und moduslos gemacht. Durch Festlegen der Eigenschaft auf **Ja** wird das Formular angezeigt und wieder modal.

Wenn Sie über die Aktion **SetzenWert** in einem Makro den Wert eines Steuerelements ändern oder neue Daten in einem Steuerelement hinzufügen, werden keine Ereignisse wie **VorAktualisierung**, **VorEingabe** oder **Änderung** ausgelöst, die auftreten, wenn Sie in diesen Steuerelementen in der Benutzeroberfläche Daten ändern oder Daten eingeben. Diese Ereignisse treten ebenfalls nicht auf, wenn Sie den Wert des Steuerelements mithilfe eines VBA-Moduls (Visual Basic for Applications) festlegen.

Diese Aktion ist in einem VBA-Modul nicht verfügbar. Legen Sie den Wert direkt in VBA fest.

## <a name="example"></a>Beispiel

**Festlegen des Werts eines Steuerelements mithilfe eines Makros**

Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten. Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, **SetzenWert** und **GeheZuSteuerelement**. Die Aktion **SetzenWert** legt das SupplierID-Steuerelement im Produktformular auf den aktuellen Lieferanten im Lieferantenformular fest. Die Aktion **GeheZuSteuerelement** verschiebt dann den Fokus auf das Feld „CategoryID“, in dem Sie beginnen können, Daten für das neue Produkt einzugeben. Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktion</p></th>
<th><p>Argumente: Einstellung</p></th>
<th><p>Kommentar</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo</strong>: <strong>Nein</strong></p></td>
<td><p>Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</p></td>
</tr>
<tr class="even">
<td><p><strong>FensterSchließen</strong></p></td>
<td><p><strong>Objekttyp</strong>: <strong>FormularObjektname</strong>: Produktliste <strong>Speichern</strong>: <strong>Nein</strong></p></td>
<td><p>Schließen des Produktlistenformulars</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formularname</strong>: Produkte <strong>Ansicht</strong>: <strong>FormData-Modus</strong>: <strong>AddWindow-Modus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen des Produktformulars</p></td>
</tr>
<tr class="even">
<td><p><strong>SetzenWert</strong></p></td>
<td><p><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</p></td>
<td><p>Festlegen des SupplierID-Steuerelements auf den aktuellen Lieferanten im Formular für Lieferanten</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: KategorieID</p></td>
<td><p>Wechseln zum CategoryID-Steuerelement</p></td>
</tr>
</tbody>
</table>

