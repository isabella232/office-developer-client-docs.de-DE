---
title: OpenView-Makroaktion
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: acb2420d4936350ed6816498cb54cc1a47cc8c5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626253"
---
# <a name="openview-macro-action"></a>OpenView-Makroaktion

**Gilt für**: Access 2013, Office 2013

In einem Access-Projekt können Sie die **ÖffnenSicht**-Aktion zum Öffnen einer Sicht in der Datenblattansicht, der Entwurfsansicht oder der Seitenansicht verwenden. Wenn die benannte Ansicht in der Datenblattansicht geöffnet wird, wird sie mit dieser Aktion ausgeführt. Für diese Ansicht können Sie die Dateneingabe auswählen und die in der Ansicht angezeigten Datensätze einschränken.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **ÖffnenSicht**-Aktion verwendet die folgenden Argumente.

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
<td><p><strong>Sichtname</strong></p></td>
<td><p>Der Name der zu öffnenden Ansicht. Im Feld <strong>Ansichtsname</strong> im Abschnitt <strong>Aktionsargumente</strong> im Bereich Makro-Generator werden alle Ansichten in der aktuellen Datenbank angezeigt. Dies ist ein erforderliches Argument. Wenn Sie ein Makro, das die <strong>ÖffnenSicht</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Diagramm mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der die Sicht geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Datenmodus</strong></p></td>
<td><p>Der Dateneingabemodus für die Sicht. Dies gilt nur für Sichten, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, jedoch keine vorhandenen Datensätze anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Diese Aktion ist mit dem Doppelklicken auf eine Ansicht im Navigationsbereich, dem Klicken mit der rechten Maustaste auf die Ansicht im Navigationsbereich und dem Klicken auf den gewünschten Befehl vergleichbar.

> [!TIP]
> - Sie können eine Tabelle aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine **ÖffnenSicht** -Aktion erstellt, die die Tabelle in der Datenblattansicht öffnet.
> - Wenn Sie die Systemmeldungen nicht anzeigen möchten, die normalerweise angezeigt werden, wenn eine Ansicht ausgeführt wird (sie melden, dass es sich um eine Sicht handelt und wie viele Datensätze betroffen sind), können Sie die **Warnmeldungen** -Aktion verwenden, um die Anzeige dieser Meldungen zu unterdrücken.

Verwenden Sie die **OpenView**-Methode des **DoCmd**-Objekts, um die **ÖffnenSicht**-Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

