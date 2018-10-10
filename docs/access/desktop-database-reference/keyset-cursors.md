---
title: Keysetcursor (Access PC-Datenbank-Referenz)
TOCTitle: Keyset Cursors
ms:assetid: 4b6e5f90-4413-4fb3-0a08-2cb89d3c61f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249236(v=office.15)
ms:contentKeyID: 48544690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bdb03b4a205e1b4954e86368c3af4aa62f773b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472619"
---
# <a name="keyset-cursors"></a>Keysetcursor


**Betrifft**: Access 2013 | Office 2013

Der Keysetcursor stellt Funktionalität zwischen einem statischen und einem dynamischen Cursor bereit, um Änderungen zu erkennen. Wie ein statischer Cursor erkennt er nicht immer Änderungen an der Mitgliedschaft und der Reihenfolge des Resultsets. Wie ein dynamischer Cursor erkennt er keine Änderungen an den Werten von Zeilen im Resultset.

Keysetgesteuerte Cursor werden durch eine Reihe eindeutiger Bezeichner (Schlüssel) gesteuert, die als Keyset bezeichnet werden. Die Schlüssel werden anhand von Spalten erstellt, die die Zeilen im Resultset eindeutig identifizieren. Das Keyset bezeichnet die Schlüsselwerte aller Zeilen, die von der Abfrageanweisung zurückgegeben werden.

Mit keysetgesteuerten Cursorn wird für jede Zeile im Cursor ein Schlüssel erstellt und gespeichert und entweder auf der Clientarbeitsstation oder auf dem Server gespeichert. Wenn Sie auf eine Zeile zugreifen, werden mithilfe des gespeicherten Schlüssels die aktuellen Datenwerte aus der Datenquelle abgerufen. Bei einem keysetgesteuerten Cursor wird die Resultsetmitgliedschaft fixiert, wenn das Keyset vollständig aufgefüllt ist. Deshalb sind Hinzufügungen oder Aktualisierungen, die die Mitgliedschaft betreffen, erst nach dem erneuten Öffnen des Cursors im Resultset vorhanden.

Änderungen an Datenwerten (entweder durch den Keysetbesitzer oder durch andere Prozesse) werden angezeigt, wenn der Benutzer einen Bildlauf im Resultset ausführt. Einfügungen, die außerhalb des Cursors (durch andere Prozesse) ausgeführt werden, werden nur angezeigt, wenn der Cursor geschlossen und erneut geöffnet wird. Einfügungen, die innerhalb des Cursors ausgeführt werden, werden am Ende des Resultsets angezeigt.

Wenn ein keysetgesteuerter Cursor versucht, eine gelöschte Zeile abzurufen, wird die Zeile als "Lücke" im Resultset angezeigt. Der Schlüssel für die Zeile ist im Keyset vorhanden, aber die Zeile ist nicht mehr im Resultset vorhanden. Falls die Schlüsselwerte in einer Zeile aktualisiert werden, wird die Zeile als gelöscht und dann eingefügt betrachtet, weshalb solche Zeilen ebenfalls als Lücke im Resultset dargestellt werden. Ein keysetgesteuerter Cursor kann immer Zeilen erkennen, die von anderen Prozessen gelöscht wurden, aber er kann optional die Schlüssel für Zeilen entfernen, die er selbst löscht. Keysetgesteuerte Cursor, die diesen Vorgang ausführen, können ihre eigenen Löschvorgänge erkennen, weil der Nachweis entfernt wurde.

Die Aktualisierung einer Schlüsselspalte verhält sich wie der Löschvorgang des alten Schlüssels, gefolgt vom Einfügen des neuen Schlüssels. Der neue Schlüsselwert wird nicht angezeigt, wenn die Aktualisierung nicht über den Cursor erfolgte. Falls die Aktualisierung über den Cursor erfolgte, wird der neue Schlüsselwert am Ende des Resultsets angezeigt.

Bei keysetgesteuerten Cursorn gibt es eine Variante, die so genannten keysetgesteuerten Standardcursor. Bei einem keysetgesteuerten Standardcursor werden die Mitgliedschaft der Zeilen im Resultset und die Reihenfolge der Zeilen beim Öffnen des Cursors fixiert, aber Änderungen an Werten, die vom Cursorbesitzer ausgeführt werden, und Änderungen, für die ein Commit ausgeführt wurde und die von anderen Prozessen vorgenommen wurden, werden angezeigt. Falls eine Änderung eine Zeile von der Mitgliedschaft ausschließt oder die Reihenfolge einer Zeile ändert, wird die Zeile nur ausgeblendet oder verschoben, wenn der Cursor geschlossen und erneut geöffnet wird. Eingefügte Daten werden nicht angezeigt, aber Änderungen an vorhandenen Daten werden angezeigt, wenn die Zeilen abgerufen werden.

Die richtige Verwendung des keysetgesteuerten Cursors ist schwierig, weil die Empfindlichkeit gegenüber Datenänderungen wie oben beschrieben von vielen verschiedenen Umständen abhängt. Wenn jedoch gleichzeitige Aktualisierungen für Ihre Anwendung keine Rolle spielen, wenn die Anwendung fehlerhafte Schlüssel programmgesteuert verarbeiten kann, und wenn die Anwendung auf bestimmte auf Schlüsseln basierende Zeilen direkt zugreifen muss, kann der keysetgesteuerte Cursor für Sie geeignet sein. Verwenden Sie **adOpenKeyset** für **CursorTypeEnum**, um anzugeben, dass Sie einen Keysetcursor in ADO verwenden möchten.

