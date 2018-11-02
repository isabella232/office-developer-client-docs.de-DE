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
ms.openlocfilehash: 50346ce66d32d91a4f902adbb5600438d214e1fb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921327"
---
# <a name="openview-macro-action"></a>OpenView-Makroaktion


**Betrifft**: Access 2013, Office 2013

In einem Access-Projekt können Sie die **ÖffnenSicht** -Aktion zum Öffnen einer Sicht in der Datenblattansicht, der Entwurfsansicht oder der Seitenansicht verwenden. Wenn die benannte Ansicht in der Datenblattansicht geöffnet wird, wird sie mit dieser Aktion ausgeführt. Für diese Ansicht können Sie die Dateneingabe auswählen und die in der Ansicht angezeigten Datensätze einschränken.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



## <a name="setting"></a>Einstellung

Die **ÖffnenSicht** -Aktion verwendet die folgenden Argumente.

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
<td><p>Der Name der Ansicht zu öffnen. Das Feld <strong>Sichtname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Ansichten in der aktuellen Datenbank. Dies ist ein erforderliches Argument. Wenn Sie ein Makro, das die <strong>ÖffnenSicht</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Diagramm mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der die Sicht geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode</strong></p></td>
<td><p>Der Dateneingabemodus für die Sicht. Dies gilt nur für Sichten, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, jedoch keine vorhandenen Datensätze anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Diese Aktion ist mit dem Doppelklicken auf eine Ansicht im Navigationsbereich, dem Klicken mit der rechten Maustaste auf die Ansicht im Navigationsbereich und dem Klicken auf den gewünschten Befehl vergleichbar.

**Tipps**

  - Sie können eine Tabelle aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine **ÖffnenSicht** -Aktion erstellt, die die Tabelle in der Datenblattansicht öffnet.

  - Wenn Sie die Systemmeldungen nicht anzeigen möchten, die normalerweise angezeigt werden, wenn eine Ansicht ausgeführt wird (sie melden, dass es sich um eine Sicht handelt und wie viele Datensätze betroffen sind), können Sie die **Warnmeldungen** -Aktion verwenden, um die Anzeige dieser Meldungen zu unterdrücken.

Verwenden Sie die **OpenView** -Methode des **DoCmd** -Objekts, um die **ÖffnenSicht** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

