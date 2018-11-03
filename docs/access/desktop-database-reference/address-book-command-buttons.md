---
title: Befehlsschaltflächen des Adressbuchs
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f586b92f309ffd330230bf732d0e477acf0a8ba9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946929"
---
# <a name="address-book-command-buttons"></a>Befehlsschaltflächen des Adressbuchs


**Betrifft**: Access 2013, Office 2013


Die Adressbuchanwendung bietet die folgenden Befehlsschaltflächen:

- Eine Schaltfläche **Find**, um eine Abfrage an die Datenbank abzusenden.

- Eine Schaltfläche **Clear**, um die Inhalte aus den Textfelder zu löschen, bevor eine neue Suche gestartet wird.

- Eine Schaltfläche **Update Profile**, um die Änderungen an einem Mitarbeiterdatensatz zu ändern.

- Eine Schaltfläche **Cancel Changes**, um Änderungen zu verwerfen.

## <a name="find-button"></a>Find (Schaltfläche)

Durch Klicken auf die Schaltfläche **Suchen** VBScript suchen aktiviert\_OnClick Sub-Prozedur, die die SQL-Abfrage erstellt und gesendet. Auf diese Schaltfläche klicken, wird das Datenraster aufgefüllt.

## <a name="building-the-sql-query"></a>Erstellen der SQL-Abfrage

Der erste Teil der Suche\_OnClick Sub-Prozedur erstellt die SQL-Abfrage einem Begriff zu einem Zeitpunkt durch Anfügen von Zeichenfolgen, die an eine globale SQL SELECT-Anweisung. Zunächst wird die Variable auf einer SQL SELECT-Anweisung, die alle Zeilen der Daten aus der Datenquellentabelle anfordert. Im nächsten Schritt überprüft der Unterprozedur jede der vier input Felder auf der Seite.

Da das Programm das Wort im Erstellen der SQL-Anweisungen verwendet, stellen die Abfragen Suchvorgänge nach Teilzeichenfolgen dar und nicht als nach genauen Übereinstimmungen.

Wenn das Feld **Nachname** den Eintrag "Berge" enthalten, und das Feld **Titel** den Eintrag "Programmmanager" enthalten, würde beispielsweise die SQL-Anweisung (Wert) lauten:

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

War die Abfrage erfolgreich, werden alle Personen, deren Nachnamen den Text Berge (z. B. Berge und Berger) und deren Positionsbezeichnung die Wörter Program Manager (z. B. Program Manager, Advanced Technologies) enthalten, im HTML-Datenraster angezeigt.

## <a name="preparing-and-sending-the-query"></a>Vorbereiten und Senden der Abfrage

Den letzten Teil der Suche\_OnClick Sub-Prozedur besteht aus zwei Anweisungen. Der ersten Anweisung wird die SQL-Eigenschaft des RDS.DataControl-Objekt ist gleich der dynamisch erstellte SQL-Abfrage. Die zweite Anweisung bewirkt, dass die **RDS.DataControl** -Objekts (), um die Datenbank Abfragen, und klicken Sie dann die Ergebnisse der Abfrage im Raster angezeigt.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Update Profile (Schaltfläche)

Durch Klicken auf die Schaltfläche **Update Profile** aktiviert das VBScript Update\_OnClick-Unterprozedur Update_OnClick RDS. DataControl-Objekt () SubmitChanges und Refresh-Methode.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Wenn DC1. SubmitChanges ausgeführt wird, Remote Data Service die Aktualisierungsinformationen verpackt und sendet ihn an den Server via HTTP. Das Update ist nichts. Wenn ein Teil der Aktualisierung nicht erfolgreich ist, wird die Änderungen vorgenommen, und eine Statusnachricht wird zurückgegeben. ausgeführt wird, Remote Data Service die Aktualisierungsinformationen verpackt und sendet ihn an den Server via HTTP. Das Update ist nichts. Wenn ein Teil der Aktualisierung nicht erfolgreich ist, wird die Änderungen vorgenommen, und eine Statusnachricht wird zurückgegeben. DC1. Aktualisieren nach **SubmitChanges** mit Remote Data Service nicht erforderlich, aber es werden aktuelle Daten sichergestellt.

## <a name="cancel-changes-button"></a>Cancel Changes (Schaltfläche)

Durch Klicken auf **Cancel Changes** wird die VBScript-Abbrechen aktiviert\_OnClick-Unterprozedur Update_OnClick RDS. DataControl Objekt (CancelUpdate-Methode.

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Wenn ausgeführt wird, es verwirft alle Änderungen, die ein Benutzer an einem Mitarbeiterdatensatz auf das Datenraster seit der letzten Abfrage oder Aktualisierung vorgenommen hat. Die ursprünglichen Werte werden wiederhergestellt.

