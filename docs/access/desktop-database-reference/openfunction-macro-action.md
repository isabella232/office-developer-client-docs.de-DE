---
title: ÖffnenFunktion-Makroaktion
TOCTitle: OpenFunction Macro Action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a64d7c44afd1531e0abf90a0372d39c742cff946
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474841"
---
# <a name="openfunction-macro-action"></a>ÖffnenFunktion-Makroaktion


**Betrifft**: Access 2013 | Office 2013

In einem Access-Projekt können Sie mithilfe der **ÖffnenFunktion** -Aktion eine benutzerdefinierte Funktion in der Datenblattansicht, in der Entwurfsansicht der Inlinefunktion, in der SQL-Texteditor-Ansicht (für eine benutzerdefinierte Skalarfunktion oder Tabellenfunktion) oder in der Seitenansicht öffnen. Mit dieser Aktion wird die benutzerdefinierte Funktion beim Öffnen in der Datenblattansicht ausgeführt. Sie können für die benutzerdefinierte Funktion auch den Dateneingabemodus auswählen und die von der benutzerdefinierten Funktion angezeigten Datensätze einschränken.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



## <a name="setting"></a>Einstellung

Die **ÖffnenFunktion** -Aktion verwendet die folgenden Argumente.

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
<td><p><strong>Funktionsname</strong></p></td>
<td><p>Der Name der benutzerdefinierten Funktion zu öffnen. Feld <strong>Funktionsname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators werden alle benutzerdefinierten Funktionen in der aktuellen Datenbank. Dies ist ein Argument erforderlich. Wenn Sie ein Makro mit der <strong>ÖffnenFunktion</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst die Funktion mit diesem Namen in der Bibliotheksdatenbank und dann in der aktuellen Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der die benutzerdefinierte Funktion geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode</strong></p></td>
<td><p>Der Dateneingabemodus für die benutzerdefinierte Funktion. Dieser gilt nur für benutzerdefinierte Funktionen, die in der Datenblattansicht geöffnet sind. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Diese Aktion bewirkt dasselbe, wie wenn Sie auf eine benutzerdefinierte Funktion im Navigationsbereich doppelklicken oder mit der rechten Maustaste auf die Funktion im Navigationsbereich klicken und dann eine Ansicht auswählen.

Wenn Sie zur Entwurfsansicht wechseln, während die benutzerdefinierte Funktion geöffnet ist, wird die Einstellung des Arguments **Datenmodus** für die benutzerdefinierte Funktion entfernt. Diese Einstellung ist nicht wirksam, auch wenn der Benutzer zur Datenblattansicht zurückkehrt.

**Tipps**

  - Sie können eine benutzerdefinierte Funktion im Navigationsbereich auswählen und in die Aktionszeile eines Makros ziehen. Damit wird automatisch eine **ÖffnenFormular** -Aktion erstellt, mit der die benutzerdefinierte Funktion in der Datenblattansicht geöffnet wird.

  - Wenn Sie nicht möchten, dass die Systemmeldungen angezeigt werden, die normalerweise angezeigt werden (und anzeigen, dass es sich um eine benutzerdefinierte Funktion handelt, und angeben, wie viele Datensätze betroffen sind), wenn eine benutzerdefinierte Funktion ausgeführt wird, können Sie die Anzeige dieser Meldungen mithilfe der **Warnmeldungen** -Aktion unterdrücken.

Wenn Sie die **ÖffnenFunktion** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) ausführen möchten, verwenden Sie die **OpenFunction** -Methode des **DoCmd** -Objekts.

