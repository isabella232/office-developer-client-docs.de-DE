---
title: Aktualisieren von Daten (Access-Desktopdatenbankreferenz)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7dca0407e500868eb21607eda996e474b0231438
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611340"
---
# <a name="updating-data"></a>Aktualisieren von Daten


**Gilt für**: Access 2013, Office 2013

Aktualisierungsverhalten und Funktionalität sind größtenteils vom Aktualisierungsmodus (Sperrtyp), Cursortyp und Cursorplatzierung abhängig.

Verwenden Sie die **Update** -Methode, um Änderungen am aktuellen Datensatz eines **Recordset** -Objekts seit dem Aufrufen der **AddNew** -Methode oder seit dem Ändern von Feldwerten in einem vorhandenen Datensatz zu speichern. Das **Recordset** -Objekt muss Aktualisierungen unterstützen.

Wenn das **Recordset** -Objekt die Batchaktualisierung unterstützt, können Sie mehrere Änderungen an mindestens einem Datensatz bis zum Aufrufen der **UpdateBatch** -Methode lokal speichern. Falls Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie die **UpdateBatch** -Methode aufrufen, ruft ADO automatisch die **Update** -Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden.

Der aktuelle Datensatz bleibt aktuell, nachdem Sie die Methode **Update** oder **UpdateBatch** aufgerufen haben.

Dieser Abschnitt enthält die folgenden Themen:

- [Unmittelbarer Modus](immediate-mode.md)
- [Verarbeitung von Transaktionen](transaction-processing.md)
- [Batchmodus (ADO)](batch-mode.md)

