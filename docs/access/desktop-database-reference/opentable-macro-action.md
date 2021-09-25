---
title: OpenTable-Makroaktion
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: fa0a62d24c67e64aeb25db4819df6a35e9fbfbff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565212"
---
# <a name="opentable-macro-action"></a>OpenTable-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **ÖffnenTabelle** -Aktion verwenden, um eine Tabelle in der Datenblattansicht, der Entwurfsansicht oder der Seitenansicht zu öffnen. Sie können auch einen Dateneingabemodus für die Tabelle auswählen.

## <a name="setting"></a>Einstellung

Die **ÖffnenTabelle**-Aktion verwendet die folgenden Argumente.

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
<td><p><strong>Tabellenname</strong></p></td>
<td><p>Der Name der zu öffnenden Tabelle. Im Feld <strong>Tabellenname</strong> im Abschnitt <strong>Aktionsargumente</strong> im Bereich Makro-Generator werden alle Tabellen in der aktuellen Datenbank angezeigt. Dies ist ein erforderliches Argument. Wenn Sie ein Makro in einer Bibliotheksdatenbank ausführen, das die <strong>ÖffnenTabelle</strong>-Aktion enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach der Tabelle mit diesem Namen und dann in der aktuellen Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der die Tabelle geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Datenmodus</strong></p></td>
<td><p>Der Dateneingabemodus für die Tabelle. Dies gilt nur für Tabellen, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, aber vorhandene Datensätze nicht bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>HinwBemerkungeneise

Diese Aktion ist mit dem Doppelklicken auf die Tabelle im Navigationsbereich, dem Klicken mit der rechten Maustaste auf die Tabelle im Navigationsbereich und dem Auswählen einer Ansicht vergleichbar.

> [!TIP]
> [!TIPP] Sie können eine Tabelle aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine **ÖffnenTabelle** -Aktion erstellt, die die Tabelle in der Datenblattansicht öffnet.

Verwenden Sie die **OpenTable** -Methode des **DoCmd** -Objekts, um die **ÖffnenTabelle** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

