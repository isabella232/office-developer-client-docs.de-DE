---
title: 'Kapitel 5: Aktualisieren und Speichern von Daten'
TOCTitle: 'Chapter 5: Updating and persisting data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d829a0a6984979008d33c3c68d805e82b69799aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562853"
---
# <a name="chapter-5-updating-and-persisting-data"></a>Kapitel 5: Aktualisieren und Speichern von Daten

**Gilt für**: Access 2013, Office 2013

In den vorangegangenen Kapiteln wurde erläutert, wie Sie mit ADO auf Daten in einer Datenquelle zugreifen, wie Sie in den Daten navigieren und sogar wie Sie die Daten bearbeiten. Wenn natürlich die Benutzer mit der Anwendung Änderungen an den Daten vornehmen sollen, müssen Sie wissen, wie diese Änderungen gespeichert werden. Sie können entweder die Änderungen am **Recordset** -Objekt mithilfe der **Save** -Methode in einer Datei speichern, oder aber Sie senden die Änderungen mithilfe der Methode **Update** oder **UpdateBatch** zur Speicherung an die Datenquelle zurück.

In den vorangegangenen Kapiteln änderten Sie die Daten in mehreren Zeilen des **Recordset** -Objekts. ADO unterstützt zwei grundlegende Konzepte im Hinblick auf das Hinzufügen, Löschen und Ändern von Datenzeilen.

Das erste Konzept besagt, dass Änderungen nicht sofort am **Recordset**-Objekt vorgenommen werden, sondern stattdessen an einem internen *Kopierpuffer*. Wenn Sie die Änderungen nicht übernehmen möchten, werden die Änderungen im Kopierpuffer verworfen. Wenn Sie die Änderungen übernehmen möchten, werden die Änderungen im Kopierpuffer auf das **Recordset**-Objekt angewandt.

Das zweite Konzept besagt, dass Änderungen entweder an die Datenquelle weitergegeben werden, sobald Sie eine Zeile als abgeschlossen deklarieren (also der *sofortige* Aktualisierungsmodus), oder alle Änderungen an Zeilen werden gesammelt, bis Sie die Zeilen als abgeschlossen deklarieren (also der *Batch* modus). Die **LockType**-Eigenschaft bestimmt, wann die Änderungen an der zugrunde liegenden Datenquelle vorgenommen werden. **adLockOptimistic** oder **adLockPessimistic** gibt den sofortigen Aktualisierungsmodus an, während **adLockBatchOptimistic** den Batchmodus angibt. Von der **CursorLocation**-Eigenschaft kann es abhängen, welche **LockType**-Einstellungen verfügbar sind. Beispielsweise wird die **adLockPessimistic**-Einstellung nicht unterstützt, wenn die **CursorLocation**-Eigenschaft auf **adUseClient** festgelegt ist.

Im sofortigen Aktualisierungsmodus werden durch jeden Aufruf der **Update** -Methode die Änderungen an die Datenquelle weitergegeben. Im Batchmodus werden durch jeden Aufruf der **Update** -Methode oder die Verschiebung der aktuellen Zeilenposition die Änderungen im Kopierpuffer gespeichert, aber nur mit der **UpdateBatch** -Methode werden die Änderungen an die Datenquelle weitergegeben.

In diesem Kapitel werden die folgenden Themen behandelt:

- [Aktualisieren von Daten (ADO)](updating-data.md)
- [Speichern von Daten (ADO)](persisting-data.md)
