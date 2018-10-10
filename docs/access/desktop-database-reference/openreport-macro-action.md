---
title: ÖffnenBericht-Makroaktion
TOCTitle: OpenReport Macro Action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 06828474aee961dd6df02f29c7d046805a1c764c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473784"
---
# <a name="openreport-macro-action"></a>ÖffnenBericht-Makroaktion

**Betrifft**: Access 2013 | Office 2013

Sie können die **ÖffnenBericht** -Aktion verwenden, um einen Bericht in der Entwurfsansicht oder in der Seitenansicht zu öffnen oder den Bericht direkt an den Drucker zu senden. Sie können die im Bericht gedruckten Datensätze außerdem einschränken.

## <a name="setting"></a>Einstellung

Die **ÖffnenBericht** -Aktion verwendet die folgenden Argumente.

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
<td><p>Berichtsname</p></td>
<td><p>Der Name des zu öffnenden Berichts. Im Feld <strong>Berichtsname</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs <strong>Makro-Generator</strong> werden alle Berichte angezeigt, die in der aktuellen Datenbank enthalten sind. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, das die OpenReport-Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach dem Bericht mit diesem Namen und anschließend in der aktuellen Datenbank.  </p></td>
</tr>
<tr class="even">
<td><p>Ansicht</p></td>
<td><p>Die Ansicht, in der der Bericht geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Drucken</strong> (Bericht wird sofort gedruckt), <strong>Entwurf</strong> oder <strong>Seitenansicht</strong>. Die Standardeinstellung ist <strong>Drucken</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p>Filter Name</p></td>
<td><p>Ein Filter, der die Datensätze des Berichts einschränkt. Sie können den Namen einer vorhandenen Abfrage oder eines Filters, der als eine Abfrage gespeichert wurde, eingeben. Die Abfrage muss jedoch alle Felder in dem Bericht enthalten, den Sie öffnen, oder die <strong>AlleFelderAusgeben</strong> -Eigenschaft muss auf <strong>Ja</strong> festgelegt sein.  </p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Eine gültige SQL WHERE-Klausel (ohne das Wort WHERE) oder ein Ausdruck, den Access zur Auswahl der Datensätze der dem Bericht zugrunde liegenden Tabelle oder Abfrage verwendet. Wenn Sie einen Filter mit dem Argument Filtername auswählen, wendet Access diese WHERE-Klausel auf die Ergebnisse des Filters. Verwenden Sie den folgenden Ausdruck, um einen Bericht zu öffnen und seine Datensätze auf diejenigen zu beschränken, die durch den Wert eines Steuerelements in einem Formular angegeben sind:<br />
<strong>[</strong><em>Feldname</em><strong>] = Forms![</strong><em>Formularname</em><strong>]![</strong><em>Steuerelementname in Formular</em><strong>]</strong><br />
Ersetzen Sie <em>Fieldname</em> durch den Namen eines Felds in der zugrunde liegenden Tabelle oder Abfrage des Berichts, den Sie öffnen möchten. Ersetzen Sie <em>Formname</em> und <em>Steuerelementname in Formular</em> mit dem Namen des Formulars und das Steuerelement im Formular, das den Wert enthält, den Datensätze im Bericht übereinstimmen sollen.</p>
<p><b>Hinweis</b>: die maximale Länge des Arguments Bedingung beträgt 255 Zeichen. Wenn Sie eine komplexere SQL WHERE-Klausel eingeben müssen, verwenden Sie die <b>OpenReport</b> -Methode des <b>DoCmd</b> -Objekts in einem Visual Basic für Applikationen (VBA) Modul stattdessen. Sie können in VBA SQL WHERE-Klausel Anweisungen von bis zu 32.768 Zeichen eingeben.</p>
</td>
</tr>
<tr class="odd">
<td><p>Window Mode</p></td>
<td><p>Der Modus, in dem der Bericht geöffnet wird. Klicken Sie im Feld <strong>Fenstermodus</strong> auf <strong>Normal</strong>, auf <strong>Ausgeblendet</strong>, auf <strong>Symbol</strong> oder auf <strong>Dialogfeld</strong>. Die Standardeinstellung ist <strong>Normal</strong>.  </p>
<p><b>Hinweis</b>: Einstellungen für einige Window Mode-Argument beim Verwenden von Dokumenten im Registerkartenformat nicht angewendet. So wechseln Sie zu überlappenden Fenstern:
<ol>
<li><p>Klicken Sie auf <strong>Optionen</strong>.</p></li>
<li><p>Klicken Sie im Dialogfeld <strong>Access-Optionen</strong> auf <strong>Aktuelle Datenbank</strong>.</p></li>
<li><p>Klicken Sie im Abschnitt <strong>Anwendungsoptionen</strong> unter <strong>Dokumentfensteroptionen</strong> auf <strong>Überlappende Fenster</strong>.</p></li>
<li><p>Klicken Sie auf <strong>OK</strong>, und schließen und öffnen Sie die Datenbank erneut.</p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die Einstellung **Drucken** des Arguments **Ansicht** druckt sofort den Bericht mit den aktuellen Druckereinstellungen, ohne dass das Dialogfeld **Drucken** geöffnet wird. Sie können auch die **ÖffnenBericht** -Aktion verwenden, um einen Bericht zu öffnen und einzurichten, und dann die PrintOut-Aktion zum Drucken verwenden. Dies empfiehlt sich beispielsweise, wenn Sie den Bericht vor dem Drucken ändern oder die **Drucken** -Aktion zum Ändern der Druckereinstellungen verwenden möchten.

Der von Ihnen angewendete Filter sowie die WHERE-Bedingung ergeben die Einstellung der Berichtseigenschaft **Filter**.

Die **ÖffnenBericht** -Aktion ist mit dem Doppelklicken auf den Bericht im Navigationsbereich, mit dem Klicken auf den Bericht im Navigationsbereich mit der rechten Maustaste und mit dem Auswählen einer Ansicht oder des Befehls **Drucken** vergleichbar.

> [!TIP] 
> - Verwenden Sie zum Drucken ähnlicher Berichte für verschiedene Datensätze einen Filter oder eine WHERE-Klausel, um die im Bericht gedruckten Datensätze einzuschränken. Bearbeiten Sie dann das Makro, um einen anderen Filter anzuwenden, oder ändern das Argument Bedingung.
> 
> - Sie können einen Bericht aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine **ÖffnenBericht** -Aktion erstellt, die den Bericht in der Berichtsansicht öffnet.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird erläutert, wie die OpenReport-Aktion verwendet werden kann, um einen Parameter zu übergeben, der einen geöffneten Bericht filtert. Der Bericht **RptChapters** zeigt die Datensätze für den angegebenen Autor, indem Sie ausgewählten Elements in das Kombinationsfeld **CboAuthors** an den SelectedAuthor-Parameter übergeben.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
