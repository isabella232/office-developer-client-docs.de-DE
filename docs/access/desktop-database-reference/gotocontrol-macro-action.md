---
title: GoToControl-Makroaktion
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f0b4fa9c3e764ac977f6ac28ca1233187c570c1a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626512"
---
# <a name="gotocontrol-macro-action"></a>GoToControl-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **GoToControl-Aktion** können Sie den Fokus auf das angegebene Feld oder Steuerelement im aktuellen Datensatz des geöffneten Formulars, Formulardatenblatts, Tabellendatenblatts oder Abfragedatenblatts verschieben. Sie können diese Aktion verwenden, wenn ein bestimmtes Feld oder Steuerelement den Fokus haben soll. Dieses Feld oder Steuerelement kann dann zu Vergleichszwecken oder für **FindRecord**-Aktionen verwendet werden. Sie können die Aktion auch zum Navigieren in einem Formular basierend auf bestimmten Bedingungen verwenden. Wenn der Benutzer z. B. im Steuerelement „Verheiratet“ auf einem Versicherungsformular „Nein“ angibt, kann der Fokus automatisch das Steuerelement „Name des Partners/der Partnerin“ überspringen und zum nächsten Steuerelement wechseln.

## <a name="setting"></a>Einstellung

> [!NOTE]
> Diese Aktion ist nicht für die Verwendung mit Datenzugriffsseiten verfügbar.

Die **GeheZuSteuerelement**-Aktion hat die folgenden Argumente.

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
<td><p><strong>Steuerelementname</strong></p></td>
<td><p>Der Name des Felds oder Steuerelements, das den Fokus erhalten soll. Geben Sie das Feld oder den Steuerelementnamen in das Feld <strong>"Steuerelementname"</strong> im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator" ein. Dies ist ein erforderliches Argument.</p>
<p><strong>HINWEIS:</strong>Geben Sie nur den Namen des Felds oder Steuerelements in das Argument <strong>"Steuerelementname"</strong> ein, nicht den vollqualifizierten Bezeichner, z. B. Formulare! Produkte! [Produkt-ID].</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können die **GoToControl-Aktion** nicht verwenden, um den Fokus auf ein Steuerelement in einem ausgeblendeten Formular zu verschieben.

> [!TIP]
> Mit der **GoToControl-Aktion** können Sie zu einem Unterformular wechseln, bei dem es sich um einen Steuerelementtyp handelt. Sie können dann die **GoToRecord-Aktion** verwenden, um zu einem bestimmten Datensatz im Unterformular zu wechseln. Sie können auch zu einem Steuerelement in einem Unterformular wechseln, indem Sie die **GoToControl-Aktion** verwenden, um zuerst zum Unterformular und dann zum Steuerelement im Unterformular zu wechseln.

Verwenden Sie die GoToControl-Methode des **DoCmd-Objekts,** um die **GoToControl-Aktion** in einem Visual Basic for Applications (VBA)-Modul auszuführen.  Sie können die **SetFocus-Methode** auch verwenden, um den Fokus auf ein Steuerelement eines Formulars oder eines seiner Unterformulare oder auf ein Feld in einer geöffneten Tabelle, Abfrage oder einem geöffneten Formulardatenblatt zu verschieben.

## <a name="examples"></a>Beispiele

**Festlegen des Werts eines Steuerelements mithilfe eines Makros**

Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten. Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, **SetzenWert** und **GeheZuSteuerelement**. Die Aktion **"SetValue"** legt das Lieferanten-ID-Steuerelement im Formular "Produkte" auf den aktuellen Lieferanten im Lieferantenformular fest. Die **GoToControl-Aktion** verschiebt dann den Fokus auf das Feld Kategorie-ID, in das Sie beginnen können, Daten für das neue Produkt einzugeben. Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.

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
<td><p>Schließen Sie das Formular "Produktliste".</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formularname</strong>: Produkte <strong>Ansicht</strong>: <strong>FormData-Modus</strong>: <strong>AddWindow-Modus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen des Produktformulars</p></td>
</tr>
<tr class="even">
<td><p><strong>SetzenWert</strong></p></td>
<td><p><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</p></td>
<td><p>Legen Sie das Lieferanten-ID-Steuerelement auf den aktuellen Lieferanten im Lieferantenformular fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: KategorieID</p></td>
<td><p>Wechseln Sie zum Kategorie-ID-Steuerelement.</p></td>
</tr>
</tbody>
</table>


**Validate data by using a macro**

Mit dem folgenden Gültigkeitsprüfungsmakro werden die Postleitzahlen überprüft, die im Lieferantenformular eingegeben werden. Es zeigt die Verwendung der Aktionen **StopMacro**, **MessageBox**, **CancelEvent** und **GoToControl**. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record. Das Makro gibt Sie dann an das Postleitzahlensteuerelement zurück, in dem Sie den Fehler beheben können. Dieses Makro sollte mit der  **BeforeUpdate**-Eigenschaft des Lieferantenformulars verbunden sein.

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
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Wenn CountryRegion <strong>null</strong>ist, kann die Postleitzahl nicht überprüft werden.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In ( &quot; Frankreich , Italien , Spanien ) und &quot; &quot; &quot; &quot; &quot; Len([Postleitzahl]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Die Postleitzahl muss 5 Zeichen lang sein. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl-Fehler</p></td>
<td><p>Wenn die Postleitzahl nicht 5 Zeichen lang ist, wird eine Meldung angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In ( &quot; Australien , Singapur ) und &quot; &quot; &quot; Len([Postleitzahl]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p>Meldung: Die Postleitzahl muss 4 Zeichen lang sein. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl-Fehler</p></td>
<td><p>Wenn die Postleitzahl nicht 4 Zeichen lang ist, wird eine Meldung angezeigt.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Kanada &quot; ) und ([Postleitzahl] nicht wie &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Meldung</strong>: Die Postleitzahl ist ungültig. Beispiel für kanadischen Code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Wenn die Postleitzahl für Kanada nicht korrekt ist, wird eine Meldung angezeigt. (Beispiel für eine kanadische Postleitzahl: H1J 1C3).</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
</tbody>
</table>

