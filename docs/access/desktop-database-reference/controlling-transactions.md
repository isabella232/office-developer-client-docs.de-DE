---
title: Steuern von Transaktionen
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 78380cda81e7260eee609e01bed0f88ce04f96c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581609"
---
# <a name="controlling-transactions"></a>Steuern von Transaktionen


**Gilt für**: Access 2013, Office 2013

Eine *Transaktion* begrenzt den Anfang und das Ende einer Reihe von Datenzugriffsvorgängen, die über eine Verbindung erfolgen. Mit dem **Connection**-Objekt, das den Transaktionsfunktionen der Datenquelle unterliegt, können Sie auch Transaktionen erstellen und verwalten. Beispielsweise können Sie mit dem Microsoft OLE DB-Anbieter für SQL Server für den Zugriff auf eine Datenbank in Microsoft SQL Server 2000 mehrere geschachtelte Transaktionen für die von Ihnen ausgeführten Befehle erstellen.

ADO stellt sicher, dass Änderungen an einer Datenquelle als Folge von Vorgängen einer Transaktion entweder alle erfolgreich oder überhaupt nicht erfolgen.

Wenn Sie die Transaktion abbrechen oder wenn einer der Vorgänge einen Fehler erzeugt, sieht das Ergebnis letztlich so aus, als ob keiner der Vorgänge in der Transaktion ausgeführt worden wäre. Die Datenquelle bleibt unverändert so wie vor Beginn der Transaktion.

Das ADO-Objektmodell enthält nicht explizit Transaktionen, stellt sie jedoch mit einer Reihe von Methoden des **Connection**-Objekts dar (**BeginTrans**, **CommitTrans** und **RollbackTrans**).

Weitere Informationen zu Transaktionen finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).

