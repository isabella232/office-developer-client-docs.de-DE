---
title: 'Kapitel 6: Fehlerbehandlung'
TOCTitle: 'Chapter 6: Error handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 14d3dc4b291d96a47e0fb67c0e7d837463cd4bf2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296409"
---
# <a name="chapter-6-error-handling"></a>Kapitel 6: Fehlerbehandlung

**Gilt für**: Access 2013, Office 2013

ADO verwendet mehrere unterschiedliche Methoden, um eine Anwendung über aufgetretene Fehler zu informieren. In diesem Kapitel werden die Fehlertypen behandelt, die beim Verwenden von ADO auftreten können, sowie die Art und Weise, wie die Anwendung informiert wird. Schließlich werden Vorschläge zum Behandeln dieser Fehler gemacht.

## <a name="how-does-ado-report-errors"></a>Wie meldet ADO Fehler?

ADO verwendet mehrere Methoden, um Sie über Fehler zu informieren:

- ADO-Fehler generieren einen Laufzeitfehler. Behandeln Sie einen ADO-Fehler genau so wie jeden anderen Laufzeitfehler, wie z. B. mithilfe einer **On Error** -Anweisung in Visual Basic.

- Das Programm kann Fehler von OLE DB empfangen. Ein OLE DB-Fehler generiert auch einen Laufzeitfehler.

- Bei einem datenproviderspezifischen Fehler wird mindestens ein **Error** -Objekt in der **Errors** -Auflistung des **Connection** -Objekts platziert, mit dem beim Auftreten des Fehlers auf den Datenspeicher zugegriffen wurde.

- Wenn der Prozess, der ein Ereignis auslöste, außerdem einen Fehler erzeugt, werden Fehlerinformationen einem **Error** -Objekt hinzugefügt und als Parameter an das Ereignis übergeben. Weitere Informationen zu Ereignissen finden Sie in [Kapitel 7: Behandeln von ADO-Ereignissen](chapter-7-handling-ado-events.md).

- Probleme, die beim Verarbeiten von Batchaktualisierungen oder sonstigen Massenvorgängen, bei denen ein **Recordset** -Objekt beteiligt ist, auftreten, können durch die **Status** -Eigenschaft des **Recordset** -Objekts angezeigt werden. Beispielsweise können Schemaeinschränkungsverletzungen oder unzureichende Berechtigungen durch **RecordStatusEnum** -Werte angegeben werden.

- Probleme, die bei einem bestimmten **Field** -Objekt im aktuellen Datensatz auftreten, werden ebenfalls durch die **Status** -Eigenschaft jedes **Field** -Objekts in der **Fields** -Auflistung des **Record** - oder **Recordset** -Objekts angezeigt. Beispielsweise können Aktualisierungen, die nicht abgeschlossen werden konnten, oder inkompatible Datentypen durch **FieldStatusEnum** -Werte angegeben werden.

In den folgenden Abschnitten werden die verschiedenen Benachrichtigungsmethoden ausführlich beschrieben.

- [ADO-Fehler](ado-errors.md)
- [ADO-Fehlerreferenz](ado-error-reference.md)
- [Anbieterfehler](provider-errors.md)
- [Feldbezogene Fehlerinformationen](field-related-error-information.md)
- [Recordset-bezogene Fehlerinformationen](recordset-related-error-information.md)
- [Vorhersehen von Fehlern](anticipating-errors.md)
- [Behandeln von Fehlern in anderen Sprachen (ADO)](handling-errors-in-other-languages.md)
