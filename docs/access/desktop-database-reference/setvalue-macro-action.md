---
title: Makroaktion „SetzenWert“
TOCTitle: SetValue Macro Action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f845dc5512611aa948991ad2099169a25bbcb113
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472871"
---
# <a name="setvalue-macro-action"></a>Makroaktion „SetzenWert“


**Betrifft**: Access 2013 | Office 2013


Die **SetzenWert** -Aktion können Sie den Wert des Microsoft Access-Felds, eines Steuerelements oder einer Eigenschaft in einem Formular, einem Formulardatenblatt oder einen Bericht festzulegen.


> [!NOTE]
> <P>Sie können die Aktion <STRONG>SetzenWert</STRONG> nicht verwenden, um den Wert einer Access-Eigenschaft festzulegen, die ein Objekt zurückgibt.</P>




> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



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
<td><p><strong>Element</strong></p></td>
<td><p>Der Name des Felds, des Steuerelements oder der Eigenschaft, dessen bzw. deren Wert Sie festlegen möchten. Geben Sie den Namen des Felds, des Steuerelements oder der Eigenschaft im Abschnitt <strong>Aktionsargument </strong> des Makro-Generators in das Feld <strong>Element </strong> ein. Verwenden Sie die vollständige Syntax, um auf dieses Element verweisen, z. B.  <em>Steuerelementname </em> (für ein Steuerelement im Formular oder Bericht, in dem das Makro aufgerufen wurde) oder <strong>Formulare</strong>!<em>Formularname</em>!<em>Steuerelementname</em>. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Der Ausdruck, den Access verwendet, um den Wert für dieses Element festzulegen. Sie müssen immer die vollständige Syntax verwenden, um auf Objekte im Ausdruck zu verweisen. Um beispielsweise den Wert eines Steuerelements für das Gehalt in einem Formular für Mitarbeiter um 10 Prozent zu erhöhen, verwenden Sie Forms!Employees!Salary*1.1. Dies ist ein erforderliches Argument.</p>

> [!NOTE]
> <P>Verwenden Sie kein Gleichheitszeichen (<STRONG>=</STRONG>) vor dem Ausdruck in diesem Argument. In diesem Fall Access wertet den Ausdruck und verwendet diesen Wert als den Ausdruck in diesem Argument. Wenn der Ausdruck eine Zeichenfolge ist, können unerwartete Ergebnisse auftreten.</P>


<p>Beispiel: bei Eingabe <strong> = &quot;Zeichenfolge1&quot; </strong> für dieses Argument wertet Access zuerst den Ausdruck als Zeichenfolge1. Klicken Sie dann verwendet Zeichenfolge1 als Ausdruck, der in diesem Argument und erwartet ein Steuerelement oder eine Eigenschaft mit dem Namen String1 im Formular oder Bericht, der das Makro aufgerufen wird.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>Klicken Sie in einer Access-Datenbank (MDB oder ACCDB) auf die Schaltfläche <STRONG>Erstellen</STRONG> , um den Ausdrucks-Generator verwenden Sie zum Erstellen eines Ausdrucks für eines der folgenden Argumente.</P>



## <a name="remarks"></a>Hinweise

Sie können diese Aktion verwenden, um einen Wert für ein Feld oder Steuerelement in einem Formular, einem Formulardatenblatt oder einem Bericht festzulegen. Sie können außerdem den Wert für nahezu alle Steuerelement-, Formular- und Berichtseigenschaften in jeder Ansicht festlegen. Informationen dazu, ob eine bestimmte Eigenschaft mit einem Makro und in welchen Ansichten die Eigenschaft festgelegt werden kann, finden Sie im Hilfethema für die jeweilige Eigenschaft im Visual Basic-Editor.

Sie können auch den Wert für ein Feld in einem Formular zugrunde liegenden Tabelle festlegen, sogar dann, wenn das Formular ein Steuerelement, das an das Feld gebunden. Verwenden Sie die Syntax **Forms**\!*Formname*\!*Fieldname* im **Element** um den Wert für ein solches Feld festzulegen. Sie können auch auf ein Feld in einem Bericht zugrunde liegenden Tabelle verweisen, indem Sie mithilfe der Syntax **Berichte**\!*Reportname*\!*Fieldname*, aber es ein Steuerelement auf den Bericht an dieses Feld gebunden muss, oder das Feld werden, die in bezeichnet muss einer berechneten Steuerelement im Bericht.

Wenn Sie den Wert eines Steuerelements in einem Formular festlegen, löst die Aktion **SetzenWert** nicht die Gültigkeitsprüfungsregeln auf Formularebene des Steuerelements, sondern die Gültigkeitsprüfungsregeln auf Tabellenebene des zugrunde liegendenen Felds aus, wenn das Steuerelement ein gebundenes Steuerelement ist. Die Aktion **SetzenWert** löst außerdem eine Neuberechnung aus, die aber nicht unbedingt sofort erfolgt. Um eine sofortige Aktualisierung auszulösen und den Abschluss der Neuberechnung zu erzwingen, verwenden Sie die Aktion **AktualisierenObjekt**. Der Wert, den Sie in einem Steuerelement mithilfe der Aktion **SetzenWert ** festlegen, wird außerdem nicht vom Eingabeformat beeinflusst, das in der Eigenschaft **InputMask** des Steuerelements oder zugrunde liegenden Felds festgelegt ist.

Um den Wert eines Steuerelements zu ändern, können Sie die Aktion **SetzenWert** Aktion in einem Makro verwenden, das durch die Ereigniseigenschaft **NachAktualisierung** des Steuerelements angegeben ist. Sie können Aktion **SetzenWert** jedoch nicht in einem Makro verwenden, das durch die Ereigniseigenschaft **VorAktualisierung** eines Steuerelements angegeben ist, um den Wert des Steuerelements zu ändern (Sie können die Aktion **SetzenWert ** aber zum Ändern des Werts anderer Steuerelemente verwenden). Sie können die Aktion **SetzenWert** außerdem in einem von der Eigenschaft **VorAktualisieurng** oder **NachAktualisierung** eines Formulars angegebenem Makro verwenden, um den Wert eines beliebigen Steuerelements im aktuellen Datensatz zu ändern.


> [!NOTE]
> <P>Die Werte der folgenden Steuerelemente können nicht mit der Aktion <STRONG>SetzenWert </STRONG> festgelegt werden:</P>
> <UL>
> <LI>
> <P>Gebundene Steuerelemente und berechnete Steuerelemente in Berichten</P>
> <LI>
> <P>Berechnete Steuerelemente in Formularen</P></LI></UL>




> [!TIP]
> <P>Sie können die Aktion <STRONG>SetzenWert</STRONG> verwenden, um ein Formular in der Formularansicht ein- oder auszublenden. Geben Sie <STRONG>Formulare</STRONG>!<EM>Formularname</EM><STRONG>Sichtbar</STRONG> in das Feld <STRONG>Element</STRONG> und <STRONG>Nein</STRONG> oder <STRONG>Ja</STRONG> in das Feld <STRONG>Ausdruck</STRONG> ein. Wenn Sie die Eigenschaft <STRONG>Sichtbar</STRONG> eines modalen Formulars auf <STRONG>Nein</STRONG> festlegen, wird das Formular ausgeblendet und nicht modal. Wenn Sie die Eigenschaft auf <STRONG>Ja</STRONG>, wird das Formular eingeblendet und wieder modal.</P>



Wenn Sie über die Aktion **SetzenWert** in einem Makro den Wert eines Steuerelements ändern oder neue Daten in einem Steuerelement hinzufügen, werden keine Ereignisse wie **VorAktualisierung**, **VorEingabe** oder **Änderung** ausgelöst, die auftreten, wenn Sie in diesen Steuerelementen in der Benutzeroberfläche Daten ändern oder Daten eingeben. Diese Ereignisse treten ebenfalls nicht auf, wenn Sie den Wert des Steuerelements mithilfe eines VBA-Moduls (Visual Basic for Applications) festlegen.

Diese Aktion ist in einem VBA-Modul nicht verfügbar. Legen Sie den Wert direkt in VBA fest.

## <a name="example"></a>Beispiel

**Festlegen des Werts eines Steuerelements mithilfe eines Makros**

Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten. Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, **SetzenWert ** und **GeheZuSteuerelement**. Die Aktion **SetzenWert** legt das SupplierID-Steuerelement im Produktformular auf den aktuellen Lieferanten im Lieferantenformular fest. Die Aktion **GeheZuSteuerelement** verschiebt dann den Fokus auf das Feld „CategoryID“, in dem Sie beginnen können, Daten für das neue Produkt einzugeben. Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.

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
<td><p>Schließen des Produktlistenformulars</p></td>
</tr>
<tr class="odd">
<td><p><strong>ÖffnenFormular</strong></p></td>
<td><p><strong>Formularname</strong>: Produkte <strong>Anzeigen</strong>: <strong>FormData Modus</strong>: <strong>Fenster hinzufügen Modus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen des Produktformulars</p></td>
</tr>
<tr class="even">
<td><p><strong>SetzenWert</strong></p></td>
<td><p><strong>Artikel</strong>: [Formulare]! [Artikel]! [Lieferanten-Nr] <strong>Ausdruck</strong>: SupplierID</p></td>
<td><p>Festlegen des SupplierID-Steuerelements auf den aktuellen Lieferanten im Formular für Lieferanten</p></td>
</tr>
<tr class="odd">
<td><p><strong>GeheZuSteuerelement</strong></p></td>
<td><p><strong>Steuerelementname</strong>: CategoryID</p></td>
<td><p>Wechseln zum CategoryID-Steuerelement</p></td>
</tr>
</tbody>
</table>

