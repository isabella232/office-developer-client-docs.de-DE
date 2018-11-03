---
title: 'Kapitel 5: Aktualisieren und Speichern von Daten'
TOCTitle: 'Chapter 5: Updating and persisting data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: decb4eefa7c1215d8889fec85c22296d33eff40c
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937309"
---
# <a name="chapter-5-updating-and-persisting-data"></a>Kapitel 5: Aktualisieren und Speichern von Daten

**Betrifft**: Access 2013, Office 2013

In den vorangegangenen Kapiteln wurde erläutert, wie Sie mit ADO auf Daten in einer Datenquelle zugreifen, wie Sie in den Daten navigieren und sogar wie Sie die Daten bearbeiten. Wenn natürlich die Benutzer mit der Anwendung Änderungen an den Daten vornehmen sollen, müssen Sie wissen, wie diese Änderungen gespeichert werden. Sie können entweder die Änderungen am **Recordset** -Objekt mithilfe der **Save** -Methode in einer Datei speichern, oder aber Sie senden die Änderungen mithilfe der Methode **Update** oder **UpdateBatch** zur Speicherung an die Datenquelle zurück.

In den vorangegangenen Kapiteln änderten Sie die Daten in mehreren Zeilen des **Recordset** -Objekts. ADO unterstützt zwei grundlegende Konzepte im Hinblick auf das Hinzufügen, Löschen und Ändern von Datenzeilen.

Das erste Konzept besagt, dass Änderungen nicht sofort am **Recordset**-Objekt vorgenommen werden, sondern stattdessen an einem internen *Kopierpuffer*. Wenn Sie die Änderungen nicht übernehmen möchten, werden die Änderungen im Kopierpuffer verworfen. Wenn Sie die Änderungen übernehmen möchten, werden die Änderungen im Kopierpuffer auf das **Recordset**-Objekt angewandt.

Das zweite Konzept besteht darin, dass Änderungen handelt es sich entweder auf die Datenquelle weitergegeben, sobald Sie die Arbeit für eine vollständige Zeile (d. h., *unmittelbaren* Modus) deklarieren, oder alle Überarbeitungen in einem Satz von Zeilen gesammelt, bis Sie der Aufwand für die Gruppe deklarieren (das ist abgeschlossen im *Batchmodus* ). Die **LockType** -Eigenschaft bestimmt, wann die Änderungen an der zugrunde liegenden Datenquelle vorgenommen werden. **adLockOptimistic** oder **adLockPessimistic** gibt den sofortigen Aktualisierungsmodus an, während **adLockBatchOptimistic** den Batchmodus angibt. Von der **CursorLocation** -Eigenschaft kann es abhängen, welche **LockType** -Einstellungen verfügbar sind. Beispielsweise wird die **adLockPessimistic** -Einstellung nicht unterstützt, wenn die **CursorLocation** -Eigenschaft auf **adUseClient** festgelegt ist.

Im sofortigen Aktualisierungsmodus werden durch jeden Aufruf der **Update** -Methode die Änderungen an die Datenquelle weitergegeben. Im Batchmodus werden durch jeden Aufruf der **Update** -Methode oder die Verschiebung der aktuellen Zeilenposition die Änderungen im Kopierpuffer gespeichert, aber nur mit der **UpdateBatch** -Methode werden die Änderungen an die Datenquelle weitergegeben.

In diesem Kapitel werden die folgenden Themen behandelt:

- [Aktualisieren von Daten (ADO)](updating-data.md)
- [Speichern von Daten (ADO)](persisting-data.md)