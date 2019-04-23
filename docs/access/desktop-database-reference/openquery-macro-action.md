---
title: OpenQuery-Makroaktion
TOCTitle: OpenQuery macro action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3294efe5ea1ab0f82be19f5c64a51287cc4df9b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288343"
---
# <a name="openquery-macro-action"></a>OpenQuery-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **ÖffnenAbfrage** -Aktion können Sie eine Auswahl- oder Kreuztabellenabfrage in der Datenblattansicht, in der Entwurfsansicht oder in der Seitenansicht öffnen. Mit dieser Aktion wird eine Aktionsabfrage ausgeführt. Sie können für die Abfrage auch einen Dateneingabemodus auswählen.

> [!NOTE]
> [!HINWEIS] Diese Aktion ist nur in einer Umgebung mit der Access-Datenbank (MDB oder ACCDB) verfügbar. Wenn Sie eine Umgebung mit einem Access-Projekt (ADP) verwenden, lesen Sie die Informationen zu den Aktionen **ÖffnenSicht**, **ÖffnenGespeicherteProzedur** oder **ÖffnenFunktion**.

## <a name="setting"></a>Einstellung

Die **ÖffnenAbfrage**-Aktion hat die folgenden Argumente.

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
<td><p><strong>Abfragename</strong></p></td>
<td><p>Der Name der Abfrage, die geöffnet werden soll. Im Feld <strong>Abfragename</strong> im Abschnitt <strong>Aktionsargumente</strong> im Bereich des Makro-Generators werden alle Abfragen in der aktuellen Datenbank angezeigt. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, das die <strong>OpenQuery</strong> -Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach der Abfrage mit diesem Namen und anschließend in der aktuellen Datenbank.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Ansicht</strong></p></td>
<td><p>Die Ansicht, in der die Abfrage geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Datenmodus</strong></p></td>
<td><p>Der Dateneingabemodus für die Abfrage. Wird nur auf Abfragen angewendet, die in der Datenblattansicht geöffnet sind. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht bearbeiten), auf <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue hinzufügen) oder auf <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn Sie **Datenblatt** für das Argument **Ansicht** verwenden, zeigt Access das Resultset an, sofern die Abfrage eine Auswahl-, Kreuztabellen-, Union- oder Pass-Through-Abfrage ist, deren **ReturnsRecords**-Eigenschaft auf **Ja** festgelegt ist. Zudem führt Access die Abfrage aus, wenn es sich um eine Aktions-, Datendefinitions- oder Pass-Through-Abfrage handelt, deren **ReturnsRecords**-Eigenschaft auf **Nein** festgelegt ist.

Die **ÖffnenAbfrage** -Aktion bewirkt dasselbe, wie wenn Sie auf die Abfrage im Navigationsbereich doppelklicken oder mit der rechten Maustaste auf die Abfrage im Navigationsbereich klicken und dann eine Ansicht auswählen. Mit dieser Aktion können Sie zusätzliche Optionen auswählen.

> [!TIP]
> - Sie können eine Abfrage aus dem Navigationsbereich in die Aktionszeile eines Makros ziehen. Damit wird automatisch eine **ÖffnenAbfrage** -Aktion erstellt, mit der die Abfrage in der Datenblattansicht geöffnet wird. Wenn Sie in die Entwurfsansicht wechseln, während die Abfrage geöffnet ist, werden die Einstellungen für das Argument **Datenmodus** für die Abfrage entfernt. Diese Einstellung ist nicht wirksam, auch wenn der Benutzer zur Datenblattansicht zurückkehrt.
> - Wenn Sie nicht möchten, dass die Systemmeldungen angezeigt werden, die normalerweise angezeigt werden (und anzeigen, dass es sich um eine Aktionsabfrage handelt, und angeben, wie viele Datensätze betroffen sind), wenn eine Aktionsabfrage ausgeführt wird, können Sie die Anzeige dieser Meldungen mithilfe der **Warnmeldungen** -Aktion unterdrücken.

Wenn Sie die **ÖffnenAbfrage** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) ausführen möchten, verwenden Sie die **OpenQuery** -Methode des **DoCmd** -Objekts.

