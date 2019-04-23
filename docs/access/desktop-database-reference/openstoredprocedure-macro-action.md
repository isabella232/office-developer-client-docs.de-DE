---
title: OpenStoredProcedure-Makroaktion
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b972174e4fe7f3c0384b7483e17eb5ceb9e8bc15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288308"
---
# <a name="openstoredprocedure-macro-action"></a>OpenStoredProcedure-Makroaktion

**Gilt für**: Access 2013, Office 2013

In einem Access-Projekt können Sie die **ÖffnenGespeicherteProzedur**-Aktion zum Öffnen einer gespeicherten Prozedur in der Datenblattansicht, der Entwurfsansicht der gespeicherten Prozedur oder der Seitenansicht verwenden. Diese Aktion führt die gespeicherte benannte Prozedur aus, wenn sie in der Datenblattansicht geöffnet wird. Sie können den Dateneingabemodus für die gespeicherte Prozedur auswählen und die Datensätze einschränken, die von der gespeicherten Prozedur angezeigt werden.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **ÖffnenGespeicherteProzedur**-Aktion verwendet die folgenden Argumente.

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
<td><p><strong>Prozedurname</strong></p></td>
<td><p>Der Name der zu öffnenden gespeicherten Prozedur. Im <strong>Feld Prozedur Name</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator werden alle gespeicherten Prozeduren in der aktuellen Datenbank angezeigt. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, das die <strong>ÖffnenGespeicherteProzedur</strong>-Aktion in einer Bibliotheksdatenbank verwendet, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach der gespeicherten Prozedur mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der die gespeicherte Prozedur geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Datenmodus</strong></p></td>
<td><p>Der Dateneingabemodus für die gespeicherte Prozedur. Dieser gilt nur für gespeicherte Prozeduren, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, jedoch vorhandene Datensätze nicht anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Bemerkungen

Diese Aktion ist mit dem Doppelklicken auf die gespeicherte Prozedur im Navigationsbereich, dem Klicken auf die gespeicherte Prozedur im Navigationsbereich mit der rechten Maustaste und dem Auswählen des gewünschten Befehls vergleichbar.

Durch das Wechseln zur Entwurfsansicht, während die gespeicherte Prozedur geöffnet ist, wird die Einstellung des Arguments **Datenmodus** für die gespeicherte Prozedur entfernt. Diese Einstellung ist nicht aktiv, selbst wenn der Benutzer zur Datenblattansicht zurückkehrt.

> [!TIP]
> - Sie können eine gespeicherte Prozedur aus dem Navigationsbereich in eine Makroaktionszeile ziehen. Dadurch wird automatisch eine **ÖffnenGespeicherteProzedur**-Aktion erstellt, die die gespeicherte Prozedur in der Datenblattansicht öffnet.
> - Wenn Sie die Systemmeldungen nicht anzeigen möchten, die normalerweise angezeigt werden, wenn eine gespeicherten Prozedur ausgeführt wird (sie melden, dass es sich um eine gespeicherte Prozedur handelt und auf wie viele Datensätze sie sich auswirkt), können Sie die **Warnmeldungen**-Aktion verwenden, um die Anzeige dieser Meldungen zu unterdrücken.

Verwenden Sie die **OpenStoredProcedure**-Methode des **DoCmd**-Objekts, um die **ÖffnenGespeicherteProzedur**-Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

