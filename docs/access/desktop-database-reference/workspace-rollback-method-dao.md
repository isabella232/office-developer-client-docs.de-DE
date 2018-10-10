---
title: Workspace.Rollback Method (DAO)
TOCTitle: Rollback Method
ms:assetid: 10775fcc-7db2-9e14-5625-048db5c50466
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845335(v=office.15)
ms:contentKeyID: 48543294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ef95f7c891c59239df82913e3235eef2d5f9545
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475433"
---
# <a name="workspacerollback-method-dao"></a>Workspace.Rollback Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Beendet die aktuelle Transaktion und setzt die Datenbanken im **Workspace**-Objekt in den Zustand zurück, in dem sie sich befanden, als die aktuelle Transaktion gestartet wurde.

## <a name="syntax"></a>Syntax

*Ausdruck* . Rollback

*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Mithilfe der Transaktionsmethoden **BeginTrans**, **CommitTrans** und **Rollback** wird die Transaktionsverarbeitung während einer Sitzung verwaltet, die durch ein **Workspace**-Objekt definiert wurde. Sie verwenden diese Methoden mit einem **Workspace**-Objekt, wenn Sie eine Reihe von an den Datenbanken vorgenommenen Änderungen in einer Sitzung als eine Einheit verarbeiten möchten.

In der Regel verwenden Sie Transaktionen zur Wahrung der Integrität Ihrer Daten, wenn Sie Datensätze in mindestens zwei Tabellen aktualisieren und gleichzeitig sicherstellen müssen, dass die Änderungen in allen Tabellen (Commit) oder in keiner der Tabellen (Rollback) ausgeführt wurden. Beispielsweise subtrahieren Sie zum Übertragen von Geldbeträgen zwischen Konten einen Betrag von einem Konto und addieren ihn dann zu einem anderen Konto. Wenn eine der Aktualisierungen fehlschlägt, sind die Konten nicht mehr ausgeglichen. Verwenden Sie vor dem Aktualisieren des ersten Datensatzes die **BeginTrans**-Methode. Falls nachfolgende Aktualisierungen fehlschlagen, können Sie anschließend mithilfe der **Rollback**-Methode sämtliche Aktualisierungen rückgängig machen. Verwenden Sie die **CommitTrans**-Methode, nachdem Sie den letzten Datensatz erfolgreich aktualisiert haben.


> [!NOTE]
> <P>[!HINWEIS] Innerhalb eines <STRONG>Workspace</STRONG>-Objekts sind Transaktionen für <STRONG>Workspace</STRONG> immer global und nicht auf ein <STRONG>Connection</STRONG>- oder <STRONG>Database</STRONG>-Objekt beschränkt. Wenn Sie Operationen für mehrere Verbindungen oder Datenbanken innerhalb einer <STRONG>Workspace</STRONG>-Transaktion durchführen, wirkt sich das Auflösen der Transaktion (d. h. die Verwendung der <STRONG>CommitTrans</STRONG>- oder <STRONG>Rollback</STRONG>-Methode) auf alle Operationen für sämtliche Verbindungen und Datenbanken innerhalb dieses Arbeitsbereichs aus.</P>



Nach Verwendung von **CommitTrans** können Sie an dieser Transaktion vorgenommene Änderungen nur dann rückgängig machen, wenn die Transaktion in einer anderen Transaktion geschachtelt ist, für die ein Rollback ausgeführt wurde. Wenn Sie Transaktionen schachteln, müssen Sie die aktuelle Transaktion auflösen, bevor Sie eine Transaktion auf einer höheren Schachtelungsebene auflösen können.

Wenn Sie gleichzeitige Transaktionen mit überlappenden, nicht geschachtelten Bereichen wünschen, können Sie zusätzliche **Workspace**-Objekte für die gleichzeitigen Transaktionen erstellen.

Wenn Sie ein **Workspace**-Objekt schließen, ohne ausstehende Transaktionen aufzulösen, wird automatisch ein Rollback für die Transaktionen ausgeführt.

Wenn Sie die **CommitTrans**- oder **Rollback**-Methode verwenden, ohne vorher die **BeginTrans**-Methode verwendet zu haben, tritt ein Fehler auf.

Möglicherweise werden Transaktionen nicht von allen in einem Microsoft Access-Arbeitsbereich verwendeten ISAM-Datenbanken unterstützt. In dem Fall hat die **Transactions**-Eigenschaft des **Database**-Objekts oder des **Recordset**-Objekts den Wert **False**. Überprüfen Sie vor dem Verwenden der **BeginTrans**-Methode den Wert der **Transactions**-Eigenschaft des **Database**-Objekts, um sicherzustellen, dass die Datenbank Transaktionen unterstützt. Wenn Sie ein **Recordset**-Objekt verwenden, das auf mehreren Datenbanken basiert, überprüfen Sie die **Transactions**-Eigenschaft des **Recordset**-Objekts. Basiert ein **Recordset**-Objekt vollständig auf Datenbankmodultabellen von Microsoft Access, können Sie in jedem Fall Transaktionen verwenden. Bei **Recordset**-Objekten, die auf in anderen Datenbankprogrammen erstellten Tabellen basieren, ist es möglich, dass Transaktionen nicht unterstützt werden. Sie können beispielsweise keine Transaktionen in einem **Recordset**-Objekt verwenden, das auf einer Paradox-Tabelle basiert. In diesem Fall ist die **Transactions**-Eigenschaft auf **False** festgelegt. Wenn **Database** oder **Recordset** keine Transaktionen unterstützen, werden die Methoden ignoriert, und es tritt kein Fehler auf.

Wenn Sie über das Microsoft Access-Datenbankmodul auf ODBC-Datenquellen zugreifen, können Sie Transaktionen nicht schachteln.

Wenn Sie in ODBC-Arbeitsbereichen **CommitTrans** verwenden, ist der Cursor möglicherweise nicht mehr gültig. Zeigen Sie die Änderungen im **Recordset**-Objekt mithilfe der **Requery**-Methode an, oder schließen Sie das **Recordset**-Objekt, und öffnen Sie es erneut.

  - Die Leistung der Anwendung lässt sich oftmals dadurch verbessern, dass Operationen unterbrochen werden, die Datenträgerzugriff auf Transaktionsblöcke erfordern. So werden die Operationen zwischengespeichert, und die Zugriffe auf den Datenträger können deutlich verringert werden.

  - In einem Microsoft Access-Arbeitsbereich werden Transaktionen in einer Datei protokolliert, die in dem Verzeichnis gespeichert ist, das durch die Umgebungsvariable TEMP auf der Arbeitsstation festgelegt ist. Wenn der Speicherplatz des TEMP-Laufwerks für die Protokolldatei nicht ausreicht, löst das Datenbankmodul einen Laufzeitfehler aus. Wenn Sie nun **CommitTrans** verwenden, wird ein Commit für eine unbestimmte Anzahl von Operationen ausgeführt. Die übrigen Operationen gehen verloren, und die Operation muss neu gestartet werden. Bei Verwendung einer **Rollback**-Methode wird das Transaktionsprotokoll freigegeben, und für sämtliche Operationen in der Transaktion wird ein Rollback ausgeführt.

  - Wenn Sie den Klon eines **Recordset**-Objekts in einer ausstehenden Transaktion schließen, wird eine implizite **Rollback**-Operation verursacht.
