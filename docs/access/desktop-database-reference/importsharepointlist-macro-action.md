---
title: ImportierenSharePointListe-Makroaktion
TOCTitle: ImportSharePointList Macro Action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 57c6630b1e9145c158a32a331ae91157e8e5e8f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883071"
---
# <a name="importsharepointlist-macro-action"></a>ImportierenSharePointListe-Makroaktion

**Betrifft**: Access 2013, Office 2013

Mit der **ImportierenSharePointListe** -Aktion können Sie Daten von einer Microsoft SharePoint Foundation-Website importieren oder verknüpfen.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.

## <a name="setting"></a>Einstellung

Die **ImportierenSharePointListe** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Transfertyp</strong></p></td>
<td><p>Wählen Sie den Übertragungstyp aus.</p>
<ul>
<li><p>Wählen Sie <strong>Importieren</strong> , kopieren Sie die SharePoint Foundation-Daten in eine Tabelle in Microsoft Access. Updates für die Daten in Access haben keinen Einfluss auf die Daten in SharePoint Foundation. Aktualisierung der Daten in SharePoint Foundation wirken sich dagegen nicht auf die Daten in Access aus.</p></li>
<li><p>Wählen Sie <strong>Link</strong> erstellen Sie eine verknüpfte Tabelle in Access, die eine Verknüpfung mit den Daten in SharePoint Foundation. Aktualisierung der Daten in Access werden in SharePoint Foundation übernommen. Dementsprechend werden Updates mit den Daten in SharePoint Foundation in Access wiedergegeben.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Websiteadresse</strong></p></td>
<td><p>Geben Sie den vollständigen Pfad der SharePoint-Website ein.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Listen-ID</strong></p></td>
<td><p>Geben Sie den Namen oder die GUID der zu übertragenden Liste ein. Erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Sicht-ID</strong></p></td>
<td><p>Geben Sie die GUID der Ansicht für die Liste ein, die Sie verwenden möchten. Lassen Sie das Argument leer, um alle Zeilen und Spalten in der Liste zu übertragen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Tabellenname</strong></p></td>
<td><p>Geben Sie den Namen ein, der in Access für die Tabelle oder die verknüpfte Tabelle angezeigt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nachschlageanzeigewerte abrufen</strong></p></td>
<td><p>Wählen Sie <strong>Ja</strong>, um Anzeigewerte für Nachschlagefelder statt der ID zu übertragen, um die Suche durchzuführen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

- Diese Aktion hat den gleichen Effekt wie das Klicken auf **SharePoint-Liste** in der Gruppe **Importieren** auf der Registerkarte **Externe Daten**. Die Argumente für die Aktion entsprechen den Optionen, die Sie im Assistenten für externe Daten auswählen.

- Verwenden Sie die **TransferSharePointList** -Methode des **DoCmd** -Objekts, um die **ImportierenSharePointListe** -Aktion in einem VBA-Modul auszuführen.

- Wenn Sie eine nicht vorhandene Liste oder Ansicht angeben, tritt kein Fehler auf, und es werden keine Daten übertragen.

- Eine GUID ist ein eindeutiger hexadezimaler Bezeichner für eine Liste oder eine Ansicht. Eine GUID muss im folgenden Format eingegeben werden, in dem jedes "F" eine hexadezimale Nummer ist (0 bis 9 oder A bis F).
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  Sie erhalten die GUID für eine Liste oder Ansicht von der SharePoint-Website mithilfe der folgenden Prozedur:
    
  1. Öffnen Sie die Liste in SharePoint Foundation.
    
  2. Wenn die gewünschte Ansicht nicht angezeigt wird, klicken Sie auf den Dropdownpfeil **Ansicht**, und markieren Sie dann die gewünschte Ansicht.
    
  3. Klicken Sie auf den Dropdownpfeil **Ansicht**, und markieren Sie dann **Diese Ansicht ändern**.Die Adresse in der Adressleiste des Browsers enthält die GUIDs sowohl für die Liste als auch für die Ansicht. Die GUID für die Liste befolgt **Liste=**, und die GUID für die Ansicht befolgt **Ansicht=**. In der Adresse wird jedoch jedes **{** -Zeichen (linke Klammer) durch die Zeichenfolge **%7B** dargestellt, jeder **-** (Bindestrich) durch die Zeichenfolge **%2D**, und jedes **}** -Zeichen (rechte Klammer) wird durch die Zeichenfolge **%7D** dargestellt. Beispiel:
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  Bevor Sie die GUIDs der Absenderadresse als Argumente in dieser Makroaktion verwenden können, müssen Sie jede **% 7 b** -Zeichenfolge mit dem Zeichen **{** ersetzen, ersetzen Sie jedes **% 2D** string mit der **-** Zeichen, und Ersetzen Sie jede **% 7 D** Zeichenfolge mit der **}** Zeichen. Fügen Sie nicht das **&** -Zeichen (kaufmännisches Und-Zeichen) ein, das auf die **%7D** -Zeichenfolge in der Listen-GUID folgt.

