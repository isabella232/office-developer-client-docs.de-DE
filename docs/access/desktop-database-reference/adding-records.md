---
title: Hinzufügen von Datensätzen (Access Desktop Database Reference)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280287"
---
# <a name="adding-records"></a>Hinzufügen von Datensätzen

**Gilt für**: Access 2013, Office 2013

Verwenden Sie die **AddNew** -Methode, um einen neuen Datensatz in einem vorhandenen **Recordset** -Objekt zu erstellen und zu initialisieren. Verwenden Sie die **Supports** -Methode mit dem Wert **adAddNew** für **CursorOptionEnum**, um zu überprüfen, ob Sie dem aktuellen **Recordset** -Objekt Datensätze hinzufügen können.

Nachdem Sie die **AddNew** -Methode aufgerufen haben, wird der neue Datensatz der aktuelle Datensatz und bleibt der aktuelle Datensatz, nachdem Sie die **Update** -Methode aufgerufen haben. Wenn das **Recordset** -Objekt keine Lesezeichen unterstützt, können Sie möglicherweise nicht auf den neuen Datensatz zugreifen, sobald Sie zu einem anderen Datensatz wechseln. Deshalb müssen Sie in Abhängigkeit vom Cursortyp die **Requery** -Methode aufrufen, damit auf den neuen Datensatz zugegriffen werden kann.

Wenn Sie **AddNew** während des Bearbeitens des aktuellen Datensatzes oder des Hinzufügens eines neuen Datensatzes aufrufen, ruft ADO die **Update** -Methode auf, um alle Änderungen zu speichern, und ADO erstellt dann den neuen Datensatz.

Dieser Abschnitt enthält die folgenden Themen:

- [Hinzufügen mehrerer Felder](adding-multiple-fields.md)
- [Bestimmen des Bearbeitungsmodus](determining-edit-mode.md)
- [Verwenden von AddNew im sofort-und Batch Modus](using-addnew-in-immediate-and-batch-modes.md)

