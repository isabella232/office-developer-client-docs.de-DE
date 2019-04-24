---
title: Steuern von Transaktionen
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ced1ae7b32d25fbae53c670959a4a6c77bcea0be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295548"
---
# <a name="controlling-transactions"></a><span data-ttu-id="c5609-102">Steuern von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="c5609-102">Controlling Transactions</span></span>


<span data-ttu-id="c5609-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5609-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5609-p101">Eine *Transaktion* begrenzt den Anfang und das Ende einer Reihe von Datenzugriffsvorgängen, die über eine Verbindung erfolgen. Mit dem **Connection**-Objekt, das den Transaktionsfunktionen der Datenquelle unterliegt, können Sie auch Transaktionen erstellen und verwalten. Beispielsweise können Sie mit dem Microsoft OLE DB-Anbieter für SQL Server für den Zugriff auf eine Datenbank in Microsoft SQL Server 2000 mehrere geschachtelte Transaktionen für die von Ihnen ausgeführten Befehle erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5609-p101">A *transaction* delimits the beginning and end of a series of data access operations that transpire across a connection. Subject to the transactional capabilities of your data source, the **Connection** object also allows you to create and manage transactions. For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server 2000, you can create multiple nested transactions for the commands you execute.</span></span>

<span data-ttu-id="c5609-107">ADO stellt sicher, dass Änderungen an einer Datenquelle als Folge von Vorgängen einer Transaktion entweder alle erfolgreich oder überhaupt nicht erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c5609-107">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</span></span>

<span data-ttu-id="c5609-p102">Wenn Sie die Transaktion abbrechen oder wenn einer der Vorgänge einen Fehler erzeugt, sieht das Ergebnis letztlich so aus, als ob keiner der Vorgänge in der Transaktion ausgeführt worden wäre. Die Datenquelle bleibt unverändert so wie vor Beginn der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="c5609-p102">If you cancel the transaction, or if one of its operations fails, the ultimate result will be as if none of the operations in the transaction occurred. The data source will remain as it was before the transaction began.</span></span>

<span data-ttu-id="c5609-110">Das ADO-Objektmodell enthält nicht explizit Transaktionen, stellt sie jedoch mit einer Reihe von Methoden des **Connection**-Objekts dar (**BeginTrans**, **CommitTrans** und **RollbackTrans**).</span><span class="sxs-lookup"><span data-stu-id="c5609-110">The ADO object model does not explicitly include transactions, but represents them with a set of **Connection** object methods (**BeginTrans**, **CommitTrans**, and **RollbackTrans**).</span></span>

<span data-ttu-id="c5609-111">Weitere Informationen zu Transaktionen finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="c5609-111">For more information about transactions, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

