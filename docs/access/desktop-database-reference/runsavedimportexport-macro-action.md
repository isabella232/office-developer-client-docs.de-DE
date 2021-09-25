---
title: RunSavedImportExport-Makroaktion
TOCTitle: RunSavedImportExport macro action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 697fd5e7c422be61f05cdb2ceaaa7f0f5e6ec4d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614934"
---
# <a name="runsavedimportexport-macro-action"></a>RunSavedImportExport-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **RunSavedImportExport** -Aktion können Sie eine gespeicherte Import- oder Exportspezifikation ausführen, die Sie mit dem Import- bzw. Export-Assistenten erstellt haben.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist.

## <a name="setting"></a>Einstellung

Die **RunSavedImportExport**-Aktion hat das folgende Argument.

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
<td><p><strong>Name des gespeicherten Imports oder Exports</strong></p></td>
<td><p>Wählen Sie den Namen einer gespeicherten Import- oder Exportspezifikation in der Dropdownliste aus.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

- Diese Makroaktion hat denselben Effekt wie das Ausführen der folgenden Prozedur in Access:
    
  1.  Klicken Sie auf der Registerkarte **Externe Daten** auf **Gespeicherte Importe** oder **Gespeicherte Exporte**.
    
  2.  Klicken Sie im Dialogfeld **Datentasks verwalten** auf der Registerkarte **Gespeicherte Importe** oder **Gespeicherte Exporte** (abhängig von Ihrer Auswahl im vorherigen Schritt) auf die Spezifikation, die Sie ausführen möchten.
    
  3.  Klicken Sie auf **Ausführen**.

- Vergewissern Sie sich vor der Ausführung der **RunSavedImportExport** -Aktion, dass die Quell- und Zieldateien vorhanden sind, die Datenquelle zum Importieren bereit ist und der Vorgang nicht versehentlich Daten in der Zieldatei überschreibt.

- Links zu weiteren Informationen über das Speichern und Ausführen von Import- und Exportspezifikationen finden Sie im Abschnitt **Siehe auch**.

- Wenn die gespeicherte Import- oder Exportspezifikation, die Sie für das Argument **Gespeicherter Importexportname** auswählen, nach dem Erstellen des Makros gelöscht wird, zeigt Access die folgende Fehlermeldung an, wenn das Makro ausgeführt wird: **Die Spezifikation mit dem angegebenen Index ist nicht vorhanden. Geben Sie einen anderen Index an. '**\Spezifikationsname**'.**

