---
title: Close-Methode – ActiveX Data Objects (ADO)
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 23cdfa8fc549e8e868a634142d93779e1dd4ccea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573166"
---
# <a name="close-method-ado"></a>Close-Methode (ADO)


**Gilt für**: Access 2013, Office 2013

Ein geöffnetes Objekt und alle abhängigen Objekte werden geschlossen.

## <a name="syntax"></a>Syntax

*Objekt*.Close

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **Close** -Methode, um ein [Connection](connection-object-ado.md)-, ein [Record](record-object-ado.md)-, ein [Recordset](recordset-object-ado.md)- oder ein [Stream](stream-object-ado.md) -Objekt zu schließen, um alle zugeordneten Systemressourcen freizugeben. Durch das Schließen eines Objekts wird es nicht aus dem Arbeitsspeicher entfernt. Sie können die Eigenschafteneinstellungen ändern und später erneut öffnen. Um ein Objekt vollständig aus dem Arbeitsspeicher zu entfernen, legen Sie die Objektvariable nach dem Schließen des Objekts auf *Nothing* (in Visual Basic) fest.

**Connection**

Beim Verwenden der **Close** -Methode zum Schließen eines **Connection** -Objekts werden auch alle der Verbindung zugeordneten **Recordset** -Objekte geschlossen. Ein [Command](command-object-ado.md)-Objekt, das dem zu schließenden **Connection** -Objekt zugeordnet ist, bleibt permanent, ist jedoch nicht mehr einem **Connection** -Objekt zugeordnet, d. h., seine [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft wird auf **Nothing** festgelegt. Außerdem werden alle vom Anbieter definierten Parameter aus der **Parameters**-Auflistung des [Command](parameters-collection-ado.md) -Objekts gelöscht.

Später können Sie die [Open](open-method-ado-connection.md)-Methode aufrufen, um die Verbindung mit der gleichen oder einer anderen Datenquelle erneut herzustellen. Während das **Connection** -Objekt geschlossen ist, wird durch das Aufrufen von Methoden, die eine offene Verbindung mit der Datenquelle erfordern, ein Fehler generiert.

Durch das Schließen eines **Connection** -Objekts während geöffnete **Recordset** -Objekte für die Verbindung vorhanden sind, wird ein Rollback für ausstehende Änderungen in allen **Recordset** -Objekten ausgeführt. Durch das explizite Schließen eines **Connection** -Objekts (Aufrufen der **Close** -Methode) während einer ausgeführten Transaktion wird ein Fehler generiert. Wenn ein **Connection** -Objekt während einer ausgeführten Transaktion außerhalb des Bereichs liegt, wird von ADO automatisch ein Rollback für die Transaktion ausgeführt.

**Recordset, Record, Stream**

Beim Verwenden der **Close** -Methode zum Schließen der Objekte **Recordset**, **Record** oder **Stream** werden die zugeordneten Daten und jeder möglicherweise für Sie geltende exklusive Zugriff auf die Daten über das jeweilige Objekt freigegeben. Später können Sie die [Open](open-method-ado-recordset.md)-Methode aufrufen, um das Objekt mit den gleichen oder geänderten Attributen erneut zu öffnen.

Während ein **Recordset** -Objekt geschlossen ist, wird durch das Aufrufen von Methoden, die einen Livecursor erfordern, ein Fehler generiert.

Wenn im Modus für sofortige Aktualisierungen eine Bearbeitung ausgeführt wird, wird durch Aufrufen der **Close** -Methode ein Fehler generiert; rufen Sie stattdessen erst die Methode [Update](update-method-ado.md) oder [CancelUpdate](cancelupdate-method-ado.md) auf. Wenn Sie das **Recordset** -Objekt im Batchaktualisierungsmodus schließen, gehen alle Änderungen seit dem letzten [UpdateBatch](updatebatch-method-ado.md)-Aufruf verloren.

Wenn Sie die [Clone](clone-method-ado.md)-Methode zum Erstellen von Kopien eines geöffneten **Recordset** -Objekts verwenden, wirkt sich das Schließen des Originals oder eines Klons nicht auf andere Kopien aus.

