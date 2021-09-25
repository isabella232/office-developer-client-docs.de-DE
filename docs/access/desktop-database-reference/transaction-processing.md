---
title: Transaktionsverarbeitung
TOCTitle: Transaction Processing
ms:assetid: 7cacf3bb-e523-8739-f9ff-c8663c9ddfeb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249523(v=office.15)
ms:contentKeyID: 48545842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1b8c41443a5fc17101edd262b7bac04cb076666b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562160"
---
# <a name="transaction-processing"></a>Verarbeitung von Transaktionen

**Gilt für**: Access 2013, Office 2013

ADO stellt die folgenden Methoden zur Steuerung von Transaktionen bereit: **BeginTrans**, **CommitTrans** und **RollbackTrans**. Verwenden Sie diese Methoden mit einem **Connection** -Objekt, wenn Sie Änderungen an den Quelldaten als eine Einheit speichern oder abbrechen möchten. Um z. B. Geld zwischen Konten zu überweisen, subtrahieren Sie einen Betrag von einem Konto und addieren ihn zu einem anderen Konto. Wenn bei einer der Aktualisierungen ein Fehler gemeldet wird, stimmen die Konten nicht mehr. Wenn Sie diese Änderungen in einer geöffneten Transaktion vornehmen, ist sichergestellt, dass entweder alle oder keine Änderungen ausgeführt werden.

> [!NOTE]
> Nicht alle Anbieter unterstützen Transaktionen. Überprüfen Sie, ob die anbieterdefinierte **Transaction DDL**-Eigenschaft in der [Properties](properties-collection-ado.md)-Auflistung des **Connection**-Objekts angezeigt wird. In diesem Fall werden vom Anbieter Transaktionen unterstützt. Falls der Anbieter keine Transaktionen unterstützt, wird beim Aufrufen einer dieser Methoden ein Fehler zurückgegeben.

Nachdem Sie die **BeginTrans**-Methode aufgerufen haben, führt der Anbieter erst wieder einen sofortigen Commit für Ihre Änderungen aus, wenn Sie **CommitTrans** oder **RollbackTrans** zum Beenden der Transaktion aufrufen.

Durch Aufrufen der **CommitTrans** -Methode werden Änderungen gespeichert, die in einer geöffneten Transaktion für die Verbindung vorgenommen wurden, und die Transaktion wird beendet. Durch Aufrufen der **RollbackTrans** -Methode werden alle Änderungen, die in einer geöffneten Transaktion vorgenommen wurden, rückgängig gemacht, und die Transaktion wird beendet. Ein Fehler wird generiert, wenn eine der Methoden ohne geöffnete Transaktion aufgerufen wird.

In Abhängigkeit von der **Attributes**-Eigenschaft des [Connection](attributes-property-ado.md) -Objekts kann durch Aufrufen der **CommitTrans** - oder **RollbackTrans** -Methode automatisch eine neue Transaktion gestartet werden. Wenn die **Attributes** -Eigenschaft auf **adXactCommitRetaining** festgelegt ist, startet der Anbieter nach einem Aufruf von **CommitTrans** automatisch eine neue Transaktion. Wenn die **Attributes** -Eigenschaft auf **adXactAbortRetaining** festgelegt ist, startet der Anbieter nach einem Aufruf von **RollbackTrans** automatisch eine neue Transaktion.

## <a name="transaction-isolation-level"></a>Transaktionsisolationsstufe

Mithilfe der **IsolationLevel** -Eigenschaft legen Sie die Isolationsstufe einer Transaktion in einem **Connection** -Objekt fest. Diese Einstellung wird erst nach dem nächsten Aufruf der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wirksam. Falls die angeforderte Isolationsstufe nicht verfügbar ist, gibt der Anbieter möglicherweise die nächsthöhere Isolationsstufe zurück. Weitere Informationen zu gültigen Werten finden Sie in der **IsolationLevel-Eigenschaft** in der ADO-Programmierreferenz.

## <a name="nested-transactions"></a>Geschachtelte Transaktionen

Für Anbieter, die geschachtelte Transaktionen unterstützen, wird durch Aufrufen der **BeginTrans** -Methode in einer geöffneten Transaktion eine neue, geschachtelte Transaktion gestartet. Der Rückgabewert gibt die Schachtelungsebene an: Der Rückgabewert "1" gibt an, dass Sie eine Transaktion der obersten Ebene geöffnet haben (die Transaktion wird also nicht innerhalb einer anderen Transaktion geschachtelt); "2" gibt an, dass Sie eine Transaktion der zweiten Ebene geöffnet haben (eine Transaktion, die innerhalb einer Transaktion der obersten Ebene geschachtelt ist) usw. Das Aufrufen von **CommitTrans** oder **RollbackTrans** wirkt sich nur auf die zuletzt geöffnete Transaktion aus. Sie müssen die aktuelle Transaktion schließen oder ein Rollback dafür ausführen, damit Sie Transaktionen auf höherer Ebene auflösen können.

