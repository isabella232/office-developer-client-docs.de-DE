---
title: GoToControl-Makroaktion
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fafa3ea40b492baf8b49dd240c6f7767ffad655
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926654"
---
# <a name="gotocontrol-macro-action"></a>GoToControl-Makroaktion


**Betrifft**: Access 2013, Office 2013



Sie können die **GeheZuSteuerelement** -Aktion verwenden, um den Fokus auf das angegebene Feld oder Steuerelement im aktuellen Datensatz des geöffneten Formulars, Datenblattes, Tabellendatenblatt oder Datenblatt Abfragen. Sie können diese Aktion verwenden, wenn ein bestimmtes Feld oder Steuerelement den Fokus haben soll. Dieses Feld oder Steuerelement kann dann für Vergleiche oder **SuchenDatensatz** -Aktionen verwendet. Sie können die Aktion auch zum Navigieren in einem Formular basierend auf bestimmten Bedingungen verwenden. Wenn der Benutzer z. B. im Steuerelement „Verheiratet“ auf einem Versicherungsformular „Nein“ angibt, kann der Fokus automatisch das Steuerelement „Name des Partners/der Partnerin“ überspringen und zum nächsten Steuerelement wechseln.

## <a name="setting"></a>Einstellung


> [!NOTE]
> <P>Diese Aktion ist nicht für die Verwendung mit Datenzugriffsseiten verfügbar.</P>



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
<td><p>Der Name des Felds oder Steuerelements, das den Fokus erhalten soll. Geben Sie den Namen Feld oder Steuerelement in das Feld <strong>Steuerelementname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators ein. Dies ist ein erforderliches Argument.</p>

> [!NOTE]
> <P>Geben Sie nur den Namen des Felds oder Steuerelements in das Argument <STRONG>Steuerelementname</STRONG> nicht den vollqualifizierten Bezeichner wie Formulare! Produkte! [Produkt-ID].</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können die **GeheZuSteuerelement** -Aktion um den Fokus auf ein Steuerelement in einem ausgeblendeten Formular zu verschieben.


> [!TIP]
> <P>Die <STRONG>GeheZuSteuerelement</STRONG> -Aktion können Sie auf ein Unterformular setzen, das eine Art von Steuerelement ist. Die <STRONG>GeheZuDatensatz</STRONG> -Aktion können dann um auf einen bestimmten Datensatz im Unterformular zu verschieben. Sie können auch auf ein Steuerelement eines Unterformulars verschieben, mit die <STRONG>GeheZuSteuerelement</STRONG> -Aktion um auf das Unterformular, und klicken Sie dann auf das Steuerelement des Unterformulars zuerst zu verschieben.</P>



Führen Sie die **GeheZuSteuerelement** -Aktion in einem Visual Basic für Applikationen (VBA) Modul mit **der GoToControl** -Methode des **DoCmd** -Objekts. Sie können auch die **SetFocus** -Methode verwenden, um den Fokus auf ein Steuerelement eines Formulars oder eines seiner Unterformulare oder an ein Feld in einer geöffneten Tabelle, Abfrage oder Formulardatenblatt.

## <a name="examples"></a>Beispiele

**Festlegen des Werts eines Steuerelements mithilfe eines Makros**

Mit dem folgende Makro wird das Formular Artikel Hinzufügen einer Schaltfläche auf dem Formular Lieferanten geöffnet. Es wird die Verwendung der **Echo**, **CloseWindow**, **ÖffnenFormular**, **SetzenWert**und **GeheZuSteuerelement** -Aktionen. Die **SetzenWert** -Aktion wird das Steuerelement Lieferanten-ID auf dem Formular auf den aktuellen Lieferanten im Formular Suppliers angezeigt. Klicken Sie dann die **GeheZuSteuerelement** -Aktion verschiebt den Fokus auf das Feld Kategorie-ID, beginnen Sie können Daten für das neue Produkt eingeben. Dieses Makro sollte der Schaltfläche Artikel hinzufügen im Formular Lieferanten zugeordnet werden.

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
<td><p><strong>Objekttyp</strong>: <strong>FormObject Name</strong>: Produkt Liste <strong>Speichern</strong>: <strong>Nein</strong></p></td>
<td><p>Produktliste Formular zu schließen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ÖffnenFormular</strong></p></td>
<td><p><strong>Formularname</strong>: Produkte <strong>Anzeigen</strong>: <strong>FormData Modus</strong>: <strong>Fenster hinzufügen Modus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen des Produktformulars</p></td>
</tr>
<tr class="even">
<td><p><strong>SetzenWert</strong></p></td>
<td><p><strong>Artikel</strong>: [Formulare]! [Artikel]! [Lieferanten-Nr] <strong>Ausdruck</strong>: SupplierID</p></td>
<td><p>Legen Sie das Steuerelement auf den aktuellen Lieferanten im Formular Suppliers angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: CategoryID</p></td>
<td><p>Wechseln Sie auf die Kategorie-ID-Steuerelement.</p></td>
</tr>
</tbody>
</table>


** Überprüfen der Gültigkeit von Daten mithilfe eines Makros**

Mit dem folgenden Gültigkeitsprüfungsmakro werden die Postleitzahlen überprüft, die im Lieferantenformular eingegeben werden. Es zeigt die Verwendung der Aktionen **StopMacro**, **MessageBox**, **CancelEvent** und **GoToControl**. Mit einem Bedingungsausdruck werden das Land, die Region und die Postleitzahl überprüft, die im Formular in einem Datensatz eingegeben werden. Wenn die Postleitzahl nicht das richtige Format für das Land/Region ist, wird das Makro ein Meldungsfeld angezeigt und Speichern des Datensatzes wird abgebrochen. Das Makro gibt dann Sie auf das Steuerelement Postleitzahl, in dem Sie den Fehler korrigieren. Dieses Makro sollte mit der **BeforeUpdate** -Eigenschaft des Lieferantenformulars verbunden sein.

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
<td><p>Wenn Land/Region <strong>Null</strong>ist, kann die Postleitzahl nicht überprüft werden.</p></td>
</tr>
<tr class="even">
<td><p>[Land/Region] In (&quot;Frankreich&quot;,&quot;Italien&quot;,&quot;Spanien&quot;) und Len ([Postleitzahl]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Die Postleitzahl muss 5 Zeichen lang sein. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl fehlerhaft</p></td>
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
<td><p>[Land/Region] In (&quot;Australien&quot;,&quot;Singapur&quot;) und Len ([Postleitzahl]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p>Message: Die Postleitzahl muss 4 Zeichen lang sein. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl fehlerhaft</p></td>
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
<td><p>([Land/Region] = &quot;Kanada&quot;) Und ([Postleitzahl] nicht wie&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Meldung</strong>: Die Postleitzahl ist ungültig. Beispiel für kanadische Postleitzahl: H1J 1 c 3 <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: PLZ Codefehler</p></td>
<td><p>Wenn die Postleitzahl nicht korrekt für Kanada ist, wird eine Meldung angezeigt. (Beispiel für eine kanadische Postleitzahl: H1J 1C3).</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
</tbody>
</table>

