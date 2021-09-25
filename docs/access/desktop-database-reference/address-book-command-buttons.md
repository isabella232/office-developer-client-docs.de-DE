---
title: Befehlsschaltflächen des Adressbuchs
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f981ef687f916a6d82cddf974ed1b6dac26c4252
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603081"
---
# <a name="address-book-command-buttons"></a>Befehlsschaltflächen des Adressbuchs


**Gilt für**: Access 2013, Office 2013


Die Adressbuchanwendung bietet die folgenden Befehlsschaltflächen:

- Eine Schaltfläche **Find**, um eine Abfrage an die Datenbank abzusenden.

- Eine Schaltfläche **Clear**, um die Inhalte aus den Textfelder zu löschen, bevor eine neue Suche gestartet wird.

- Eine Schaltfläche **Update Profile**, um die Änderungen an einem Mitarbeiterdatensatz zu ändern.

- Eine Schaltfläche **Cancel Changes**, um Änderungen zu verwerfen.

## <a name="find-button"></a>Find (Schaltfläche)

Durch Klicken auf die Schaltfläche **"Suchen"** wird die VBScript Find \_ OnClick Sub-Prozedur aktiviert, die die SQL Abfrage erstellt und sendet. Clicking this button populates the data grid.

## <a name="building-the-sql-query"></a>Erstellen der SQL-Abfrage

Der erste Teil der \_ OnClick Sub-Prozedur suchen erstellt die SQL Abfrage, indem Textzeichenfolgen an eine globale SQL SELECT-Anweisung angefügt werden. Zunächst wird die Variable auf einer SQL SELECT-Anweisung, die alle Zeilen der Daten aus der Datenquellentabelle anfordert. Im nächsten Schritt überprüft der Unterprozedur jede der vier input Felder auf der Seite.

Da das Programm das Wort im Erstellen der SQL-Anweisungen verwendet, stellen die Abfragen Suchvorgänge nach Teilzeichenfolgen dar und nicht als nach genauen Übereinstimmungen.

Wenn das Feld **Nachname** den Eintrag "Berge" enthalten, und das Feld **Titel** den Eintrag "Programmmanager" enthalten, würde beispielsweise die SQL-Anweisung (Wert) lauten:

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.

## <a name="preparing-and-sending-the-query"></a>Vorbereiten und Senden der Abfrage

Der letzte Teil der Find \_ OnClick Sub-Prozedur besteht aus zwei Anweisungen. Der ersten Anweisung wird die SQL-Eigenschaft des RDS.DataControl-Objekt ist gleich der dynamisch erstellte SQL-Abfrage. Die zweite Anweisung bewirkt, dass die **RDS.DataControl** -Objekts (), um die Datenbank Abfragen, und klicken Sie dann die Ergebnisse der Abfrage im Raster angezeigt.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Update Profile (Schaltfläche)

Durch Klicken auf die Schaltfläche **"Profil aktualisieren"** wird die VBScript Update \_ OnClick Sub-Prozedur aktiviert, die rds ausführt. Die Methoden "SubmitChanges" und "Refresh" des DataControl-Objekts.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Wenn DC1. SubmitChanges wird ausgeführt, der Remotedatendienst packt alle Updateinformationen und sendet sie über HTTP an den Server. Das Update ist alles oder nichts; wenn ein Teil der Aktualisierung nicht erfolgreich ist, wird keine der Änderungen vorgenommen, und es wird eine Statusmeldung zurückgegeben. wird ausgeführt, packt der Remotedatendienst alle Updateinformationen und sendet sie über HTTP an den Server. Das Update ist alles oder nichts; wenn ein Teil der Aktualisierung nicht erfolgreich ist, wird keine der Änderungen vorgenommen, und es wird eine Statusmeldung zurückgegeben. DC1. Eine Aktualisierung ist nach **SubmitChanges** mit Remote Data Service nicht erforderlich, stellt jedoch neue Daten sicher.

## <a name="cancel-changes-button"></a>Cancel Changes (Schaltfläche)

Durch Klicken auf **"Änderungen abbrechen"** wird die VBScript Cancel \_ OnClick Sub-Prozedur aktiviert, die rds ausführt. Die Methode des DataControl-Objekts ( CancelUpdate.

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Wenn ausgeführt wird, es verwirft alle Änderungen, die ein Benutzer an einem Mitarbeiterdatensatz auf das Datenraster seit der letzten Abfrage oder Aktualisierung vorgenommen hat. Die ursprünglichen Werte werden wiederhergestellt.

