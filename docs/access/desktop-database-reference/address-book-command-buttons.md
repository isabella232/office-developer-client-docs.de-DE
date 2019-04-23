---
title: Befehlsschaltflächen des Adressbuchs
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282478"
---
# <a name="address-book-command-buttons"></a>Befehlsschaltflächen des Adressbuchs


**Gilt für**: Access 2013, Office 2013


Die Adressbuchanwendung bietet die folgenden Befehlsschaltflächen:

- Eine Schaltfläche **Find**, um eine Abfrage an die Datenbank abzusenden.

- Eine Schaltfläche **Clear**, um die Inhalte aus den Textfelder zu löschen, bevor eine neue Suche gestartet wird.

- Eine Schaltfläche **Update Profile**, um die Änderungen an einem Mitarbeiterdatensatz zu ändern.

- Eine Schaltfläche **Cancel Changes**, um Änderungen zu verwerfen.

## <a name="find-button"></a>Find (Schaltfläche)

Wenn Sie auf die Schaltfläche **Suchen** klicken,\_wird die VBScript-Suche OnClick Sub-Prozedur aktiviert, die die SQL-Abfrage erstellt und sendet. Clicking this button populates the data grid.

## <a name="building-the-sql-query"></a>Erstellen der SQL-Abfrage

Der erste Teil der "Find\_onclick"-Sub-Prozedur erstellt die SQL-Abfrage, jeweils einen Ausdruck, durch Anfügen von Textzeichenfolgen an eine globale SQL SELECT-Anweisung. Zunächst wird die Variable auf einer SQL SELECT-Anweisung, die alle Zeilen der Daten aus der Datenquellentabelle anfordert. Im nächsten Schritt überprüft der Unterprozedur jede der vier input Felder auf der Seite.

Da das Programm das Wort im Erstellen der SQL-Anweisungen verwendet, stellen die Abfragen Suchvorgänge nach Teilzeichenfolgen dar und nicht als nach genauen Übereinstimmungen.

Wenn das Feld **Nachname** den Eintrag "Berge" enthalten, und das Feld **Titel** den Eintrag "Programmmanager" enthalten, würde beispielsweise die SQL-Anweisung (Wert) lauten:

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.

## <a name="preparing-and-sending-the-query"></a>Vorbereiten und Senden der Abfrage

Der letzte Teil der Find\_OnClick-Sub-Prozedur besteht aus zwei Anweisungen. Der ersten Anweisung wird die SQL-Eigenschaft des RDS.DataControl-Objekt ist gleich der dynamisch erstellte SQL-Abfrage. Die zweite Anweisung bewirkt, dass die **RDS.DataControl** -Objekts (), um die Datenbank Abfragen, und klicken Sie dann die Ergebnisse der Abfrage im Raster angezeigt.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Update Profile (Schaltfläche)

Durch Klicken auf die Schaltfläche **Profil aktualisieren** wird die\_VBScript-Update-OnClick-Sub-Prozedur aktiviert, die RDS ausführt. DataControl-Objekt () SubmitChanges und Refresh-Methode.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Wenn DC1. SubmitChanges ausgeführt wird, werden vom Remote Data Service alle Update Informationen verpackt und über HTTP an den Server gesendet. Das Update ist alles-oder-nichts; Wenn ein Teil der Aktualisierung nicht erfolgreich ist, wird keine der Änderungen vorgenommen, und es wird eine Statusmeldung zurückgegeben. ausgeführt wird, werden vom Remote Data Service alle Update Informationen verpackt und über HTTP an den Server gesendet. Das Update ist alles-oder-nichts; Wenn ein Teil der Aktualisierung nicht erfolgreich ist, wird keine der Änderungen vorgenommen, und es wird eine Statusmeldung zurückgegeben. DC1. Refresh ist nach **SubmitChanges** mit Remote Data Service nicht erforderlich, es werden jedoch neue Daten gesichert.

## <a name="cancel-changes-button"></a>Cancel Changes (Schaltfläche)

Wenn Sie auf **Änderungen abbrechen** klicken, wird\_die VBScript-Unterprozedur Cancel onCLICK aktiviert, die RDS ausführt. DataControl-Objekt (CancelUpdate-Methode.

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Wenn ausgeführt wird, es verwirft alle Änderungen, die ein Benutzer an einem Mitarbeiterdatensatz auf das Datenraster seit der letzten Abfrage oder Aktualisierung vorgenommen hat. Die ursprünglichen Werte werden wiederhergestellt.

