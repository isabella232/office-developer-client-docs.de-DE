---
title: Transaktionsverarbeitung
TOCTitle: Transaction Processing
ms:assetid: 7cacf3bb-e523-8739-f9ff-c8663c9ddfeb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249523(v=office.15)
ms:contentKeyID: 48545842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 24e7940c86b079d5eb51fa894426a19e7700bf39
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937484"
---
# <a name="transaction-processing"></a>Transaktionsverarbeitung


**Betrifft**: Access 2013, Office 2013

ADO stellt die folgenden Methoden zur Steuerung von Transaktionen bereit: **BeginTrans**, **CommitTrans** und **RollbackTrans**. Verwenden Sie diese Methoden mit einem **Connection** -Objekt, wenn Sie Änderungen an den Quelldaten als eine Einheit speichern oder abbrechen möchten. Um z. B. Geld zwischen Konten zu überweisen, subtrahieren Sie einen Betrag von einem Konto und addieren ihn zu einem anderen Konto. Wenn bei einer der Aktualisierungen ein Fehler gemeldet wird, stimmen die Konten nicht mehr. Wenn Sie diese Änderungen in einer geöffneten Transaktion vornehmen, ist sichergestellt, dass entweder alle oder keine Änderungen ausgeführt werden.


> [!NOTE]
> <P>Transaktionen werden nicht von allen Anbietern unterstützt. Überprüfen Sie, ob die vom Anbieter definierte "<STRONG>Transaction DDL</STRONG>"-Eigenschaft in der <A href="properties-collection-ado.md">Properties</A>-Auflistung des <STRONG>Connection</STRONG>-Objekts angezeigt wird und damit angibt, dass Transaktionen vom Anbieter unterstützt werden. Wenn Transaktionen vom Anbieter nicht unterstützt werden, wird beim Aufrufen einer dieser Methoden ein Fehler zurückgegeben.</P>



Nachdem Sie die **BeginTrans** -Methode aufgerufen haben, führt der Anbieter erst wieder einen sofortigen Commit für Ihre Änderungen aus, wenn Sie **CommitTrans** oder **RollbackTrans** zum Beenden der Transaktion aufrufen.

Durch Aufrufen der **CommitTrans** -Methode werden Änderungen gespeichert, die in einer geöffneten Transaktion für die Verbindung vorgenommen wurden, und die Transaktion wird beendet. Durch Aufrufen der **RollbackTrans** -Methode werden alle Änderungen, die in einer geöffneten Transaktion vorgenommen wurden, rückgängig gemacht, und die Transaktion wird beendet. Ein Fehler wird generiert, wenn eine der Methoden ohne geöffnete Transaktion aufgerufen wird.

In Abhängigkeit von der **Attributes**-Eigenschaft des [Connection](attributes-property-ado.md) -Objekts kann durch Aufrufen der **CommitTrans** - oder **RollbackTrans** -Methode automatisch eine neue Transaktion gestartet werden. Wenn die **Attributes** -Eigenschaft auf **adXactCommitRetaining** festgelegt ist, startet der Anbieter nach einem Aufruf von **CommitTrans** automatisch eine neue Transaktion. Wenn die **Attributes** -Eigenschaft auf **adXactAbortRetaining** festgelegt ist, startet der Anbieter nach einem Aufruf von **RollbackTrans** automatisch eine neue Transaktion.

## <a name="transaction-isolation-level"></a>Transaktionsisolationsstufe

Mithilfe der **IsolationLevel** -Eigenschaft legen Sie die Isolationsstufe einer Transaktion in einem **Connection** -Objekt fest. Diese Einstellung wird erst nach dem nächsten Aufruf der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wirksam. Falls die angeforderte Isolationsstufe nicht verfügbar ist, gibt der Anbieter möglicherweise die nächsthöhere Isolationsstufe zurück. Verweisen Sie auf die **IsolationLevel** -Eigenschaft in der ADO-Programmierreferenz für Weitere Informationen zu gültigen Werten.

## <a name="nested-transactions"></a>Geschachtelte Transaktionen

Für Anbieter, die geschachtelte Transaktionen unterstützen, wird durch Aufrufen der **BeginTrans** -Methode in einer geöffneten Transaktion eine neue, geschachtelte Transaktion gestartet. Der Rückgabewert gibt die Schachtelungsebene an: Der Rückgabewert "1" gibt an, dass Sie eine Transaktion der obersten Ebene geöffnet haben (die Transaktion wird also nicht innerhalb einer anderen Transaktion geschachtelt); "2" gibt an, dass Sie eine Transaktion der zweiten Ebene geöffnet haben (eine Transaktion, die innerhalb einer Transaktion der obersten Ebene geschachtelt ist) usw. Das Aufrufen von **CommitTrans** oder **RollbackTrans** wirkt sich nur auf die zuletzt geöffnete Transaktion aus. Sie müssen die aktuelle Transaktion schließen oder ein Rollback dafür ausführen, damit Sie Transaktionen auf höherer Ebene auflösen können.

