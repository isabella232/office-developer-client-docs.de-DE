---
title: ÖffnenTabelle-Makroaktion
TOCTitle: OpenTable Macro Action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 729c1f14d49b3f80ec6307ce775066d3291b96de
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474505"
---
# <a name="opentable-macro-action"></a>ÖffnenTabelle-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Sie können die **ÖffnenTabelle** -Aktion verwenden, um eine Tabelle in der Datenblattansicht, der Entwurfsansicht oder der Seitenansicht zu öffnen. Sie können auch einen Dateneingabemodus für die Tabelle auswählen.

## <a name="setting"></a>Einstellung

Die **ÖffnenTabelle** -Aktion verwendet die folgenden Argumente.

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
<td><p>Der Name der zu öffnenden Tabelle. Das Feld <strong>Tabellenname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Tabellen in der aktuellen Datenbank. Dies ist ein erforderliches Argument. Wenn Sie ein Makro in einer Bibliotheksdatenbank ausführen, das die <strong>ÖffnenTabelle</strong>-Aktion enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach der Tabelle mit diesem Namen und dann in der aktuellen Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der die Tabelle geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode</strong></p></td>
<td><p>Der Dateneingabemodus für die Tabelle. Dies gilt nur für Tabellen, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, aber vorhandene Datensätze nicht bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Diese Aktion ist mit dem Doppelklicken auf die Tabelle im Navigationsbereich, dem Klicken mit der rechten Maustaste auf die Tabelle im Navigationsbereich und dem Auswählen einer Ansicht vergleichbar.


> [!TIP]
> <P>[!TIPP] Sie können eine Tabelle aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine <STRONG>ÖffnenTabelle</STRONG> -Aktion erstellt, die die Tabelle in der Datenblattansicht öffnet.</P>



Verwenden Sie die **OpenTable** -Methode des **DoCmd** -Objekts, um die **ÖffnenTabelle** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

