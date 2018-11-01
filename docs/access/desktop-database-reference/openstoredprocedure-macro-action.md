---
title: ÖffnenGespeicherteProzedur-Makroaktion
TOCTitle: OpenStoredProcedure Macro Action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 52d7d6c54913511ab593ee77d374ed55984ed40b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883253"
---
# <a name="openstoredprocedure-macro-action"></a>ÖffnenGespeicherteProzedur-Makroaktion


**Betrifft**: Access 2013, Office 2013

In einem Access-Projekt können Sie die **ÖffnenGespeicherteProzedur**-Aktion zum Öffnen einer gespeicherten Prozedur in der Datenblattansicht, der Entwurfsansicht der gespeicherten Prozedur oder der Seitenansicht verwenden. Diese Aktion führt die gespeicherte benannte Prozedur aus, wenn sie in der Datenblattansicht geöffnet wird. Sie können den Dateneingabemodus für die gespeicherte Prozedur auswählen und die Datensätze einschränken, die von der gespeicherten Prozedur angezeigt werden.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



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
<td><p>Der Name der gespeicherten Prozedur zu öffnen. Das <strong>Prozedurname</strong> Feld im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle gespeicherten Prozeduren in der aktuellen Datenbank. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, das die <strong>ÖffnenGespeicherteProzedur</strong>-Aktion in einer Bibliotheksdatenbank verwendet, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach der gespeicherten Prozedur mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der die gespeicherte Prozedur geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode</strong></p></td>
<td><p>Der Dateneingabemodus für die gespeicherte Prozedur. Dieser gilt nur für gespeicherte Prozeduren, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, jedoch vorhandene Datensätze nicht anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Diese Aktion ist mit dem Doppelklicken auf die gespeicherte Prozedur im Navigationsbereich, dem Klicken auf die gespeicherte Prozedur im Navigationsbereich mit der rechten Maustaste und dem Auswählen des gewünschten Befehls vergleichbar.

Durch das Wechseln zur Entwurfsansicht, während die gespeicherte Prozedur geöffnet ist, wird die Einstellung des Arguments **Datenmodus** für die gespeicherte Prozedur entfernt. Diese Einstellung ist nicht aktiv, selbst wenn der Benutzer zur Datenblattansicht zurückkehrt.


> [!TIP]
> <P></P>
> <UL>
> <LI>
> <P>Sie können eine gespeicherte Prozedur im Navigationsbereich an eine Makro-Aktionszeile ziehen. Dadurch wird automatisch eine <STRONG>ÖffnenGespeicherteProzedur</STRONG> -Aktion, die die gespeicherte Prozedur in der Datenblattansicht geöffnet wird erstellt.</P>
> <LI>
> <P>
> 						Wenn Sie die Systemmeldungen nicht anzeigen möchten, die normalerweise angezeigt werden, wenn eine gespeicherten Prozedur ausgeführt wird (sie melden, dass es sich um eine gespeicherte Prozedur handelt und auf wie viele Datensätze sie sich auswirkt), können Sie die <STRONG>Warnmeldungen</STRONG>-Aktion verwenden, um die Anzeige dieser Meldungen zu unterdrücken.
</P></LI></UL>
<P></P>



Verwenden Sie die **OpenStoredProcedure**-Methode des **DoCmd**-Objekts, um die **ÖffnenGespeicherteProzedur**-Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

