---
title: Hinzufügen von Datensätzen (Access PC-Datenbank-Referenz)
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bfa1503e7f7b874136ab5aee70721a3b9cf3463b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475599"
---
# <a name="adding-records"></a>Hinzufügen von Datensätzen


**Betrifft**: Access 2013 | Office 2013

Verwenden Sie die **AddNew** -Methode, um einen neuen Datensatz in einem vorhandenen **Recordset** -Objekt zu erstellen und zu initialisieren. Verwenden Sie die **Supports** -Methode mit dem Wert **adAddNew** für **CursorOptionEnum**, um zu überprüfen, ob Sie dem aktuellen **Recordset** -Objekt Datensätze hinzufügen können.

Nachdem Sie die **AddNew** -Methode aufgerufen haben, wird der neue Datensatz der aktuelle Datensatz und bleibt der aktuelle Datensatz, nachdem Sie die **Update** -Methode aufgerufen haben. Wenn das **Recordset** -Objekt keine Lesezeichen unterstützt, können Sie möglicherweise nicht auf den neuen Datensatz zugreifen, sobald Sie zu einem anderen Datensatz wechseln. Deshalb müssen Sie in Abhängigkeit vom Cursortyp die **Requery** -Methode aufrufen, damit auf den neuen Datensatz zugegriffen werden kann.

Wenn Sie **AddNew** während des Bearbeitens des aktuellen Datensatzes oder des Hinzufügens eines neuen Datensatzes aufrufen, ruft ADO die **Update** -Methode auf, um alle Änderungen zu speichern, und ADO erstellt dann den neuen Datensatz.

