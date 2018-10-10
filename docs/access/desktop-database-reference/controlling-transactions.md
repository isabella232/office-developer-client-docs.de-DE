---
title: Steuern von Transaktionen
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b70e6586e17286f4f7a13417d0901f1250635631
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475850"
---
# <a name="controlling-transactions"></a>Steuern von Transaktionen


**Betrifft**: Access 2013 | Office 2013

Eine *Transaktion* begrenzt Anfang und Ende einer Reihe von Datenzugriffsvorgänge, die ablaufen über eine Verbindung müssen. Mit dem **Connection** -Objekt, das den Transaktionsfunktionen der Datenquelle unterliegt, können Sie auch Transaktionen erstellen und verwalten. Beispielsweise können Sie mit dem Microsoft OLE DB-Anbieter für SQL Server für den Zugriff auf eine Datenbank in Microsoft SQL Server 2000 mehrere geschachtelte Transaktionen für die von Ihnen ausgeführten Befehle erstellen.

ADO stellt sicher, dass Änderungen an einer Datenquelle als Folge von Vorgängen einer Transaktion entweder alle erfolgreich oder überhaupt nicht erfolgen.

Wenn Sie die Transaktion abbrechen oder wenn einer der Vorgänge einen Fehler erzeugt, sieht das Ergebnis letztlich so aus, als ob keiner der Vorgänge in der Transaktion ausgeführt worden wäre. Die Datenquelle bleibt unverändert so wie vor Beginn der Transaktion.

Das ADO-Objektmodell enthält nicht explizit Transaktionen, stellt sie jedoch mit einer Reihe von Methoden des **Connection**-Objekts dar (**BeginTrans**, **CommitTrans** und **RollbackTrans**).

Weitere Informationen zu Transaktionen finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).

