---
title: RunSavedImportExport-Makroaktion
TOCTitle: RunSavedImportExport Macro Action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 48e808fa27e468dd7cb651cb5784627d5064fea0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870933"
---
# <a name="runsavedimportexport-macro-action"></a>RunSavedImportExport-Makroaktion


**Betrifft**: Access 2013, Office 2013

Mit der **RunSavedImportExport** -Aktion können Sie eine gespeicherte Import- oder Exportspezifikation ausführen, die Sie mit dem Import- bzw. Export-Assistenten erstellt haben.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



## <a name="setting"></a>Einstellung

Die **RunSavedImportExport** -Aktion hat das folgende Argument.

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


## <a name="remarks"></a>Hinweise

  - Diese Makroaktion hat denselben Effekt wie das Ausführen der folgenden Prozedur in Access:
    
    1.  Klicken Sie auf der Registerkarte **Externe Daten** auf **Gespeicherte Importe** oder **Gespeicherte Exporte**.
    
    2.  Klicken Sie im Dialogfeld **Datentasks verwalten** auf der Registerkarte **Gespeicherte Importe** oder **Gespeicherte Exporte** (abhängig von Ihrer Auswahl im vorherigen Schritt) auf die Spezifikation, die Sie ausführen möchten.
    
    3.  Klicken Sie auf **Ausführen**.

  - Vergewissern Sie sich vor der Ausführung der **RunSavedImportExport** -Aktion, dass die Quell- und Zieldateien vorhanden sind, die Datenquelle zum Importieren bereit ist und der Vorgang nicht versehentlich Daten in der Zieldatei überschreibt.

  - Links zu weiteren Informationen über das Speichern und Ausführen von Import- und Exportspezifikationen finden Sie im Abschnitt **Siehe auch**.

  - Wenn die gespeicherte Import- oder Exportspezifikation, die Sie auswählen, für das Argument **Gespeichert importieren exportieren Name** gelöscht wird, nachdem das Makro erstellt wird, zeigt Access die folgende Fehlermeldung angezeigt, wenn das Makro ausgeführt wird: **die Spezifikation mit dem angegebenen Index ist nicht vorhanden. Geben Sie einen anderen Index. ' *** Spezifikation Namen ***'.**

