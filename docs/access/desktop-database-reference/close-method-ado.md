---
title: Close-Methode - ActiveX Data Objects (ADO)
TOCTitle: Close Method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2df2f04f54242186093122bf70ef3365ad8617bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875819"
---
# <a name="close-method-ado"></a><span data-ttu-id="70875-102">Close-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="70875-102">Close Method (ADO)</span></span>


<span data-ttu-id="70875-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70875-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70875-104">Ein geöffnetes Objekt und alle abhängigen Objekte werden geschlossen.</span><span class="sxs-lookup"><span data-stu-id="70875-104">Closes an open object and any dependent objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="70875-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70875-105">Syntax</span></span>

<span data-ttu-id="70875-106">*Objekt*.Close</span><span class="sxs-lookup"><span data-stu-id="70875-106">*object*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="70875-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70875-107">Remarks</span></span>

<span data-ttu-id="70875-108">Verwenden Sie die **Close** -Methode, um eine [Verbindung](connection-object-ado.md), einen [Datensatz](record-object-ado.md), ein [Recordset-Objekt](recordset-object-ado.md)oder ein [Stream](stream-object-ado.md) -Objekt, um alle zugeordneten Systemressourcen frei zu schließen.</span><span class="sxs-lookup"><span data-stu-id="70875-108">Use the **Close** method to close a [Connection](connection-object-ado.md), a [Record](record-object-ado.md), a [Recordset](recordset-object-ado.md), or a [Stream](stream-object-ado.md) object to free any associated system resources.</span></span> <span data-ttu-id="70875-109">Ein Objekt schließen, wird es nicht aus dem Speicher entfernt; Sie können ändern, dessen Eigenschaft und einem späteren Zeitpunkt erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="70875-109">Closing an object does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="70875-110">Um ein Objekt aus dem Speicher vollständig zu entfernen, legen Sie die Objektvariable auf *Nothing* (in Visual Basic) nach dem Schließen des Objekts.</span><span class="sxs-lookup"><span data-stu-id="70875-110">To completely eliminate an object from memory, set the object variable to *Nothing* (in Visual Basic) after closing the object.</span></span>

<span data-ttu-id="70875-111">**Connection**</span><span class="sxs-lookup"><span data-stu-id="70875-111">**Connection**</span></span>

<span data-ttu-id="70875-p102">Beim Verwenden der **Close** -Methode zum Schließen eines **Connection** -Objekts werden auch alle der Verbindung zugeordneten **Recordset** -Objekte geschlossen. Ein [Command](command-object-ado.md)-Objekt, das dem zu schließenden **Connection** -Objekt zugeordnet ist, bleibt permanent, ist jedoch nicht mehr einem **Connection** -Objekt zugeordnet, d. h., seine [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft wird auf **Nothing** festgelegt. Außerdem werden alle vom Anbieter definierten Parameter aus der **Parameters**-Auflistung des [Command](parameters-collection-ado.md) -Objekts gelöscht.</span><span class="sxs-lookup"><span data-stu-id="70875-p102">Using the **Close** method to close a **Connection** object also closes any active **Recordset** objects associated with the connection. A [Command](command-object-ado.md) object associated with the **Connection** object you are closing will persist, but it will no longer be associated with a **Connection** object; that is, its [ActiveConnection](activeconnection-property-ado.md) property will be set to **Nothing**. Also, the **Command** object's [Parameters](parameters-collection-ado.md) collection will be cleared of any provider-defined parameters.</span></span>

<span data-ttu-id="70875-p103">Später können Sie die [Open](open-method-ado-connection.md)-Methode aufrufen, um die Verbindung mit der gleichen oder einer anderen Datenquelle erneut herzustellen. Während das **Connection** -Objekt geschlossen ist, wird durch das Aufrufen von Methoden, die eine offene Verbindung mit der Datenquelle erfordern, ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="70875-p103">You can later call the [Open](open-method-ado-connection.md) method to re-establish the connection to the same, or another, data source. While the **Connection** object is closed, calling any methods that require an open connection to the data source generates an error.</span></span>

<span data-ttu-id="70875-p104">Durch das Schließen eines **Connection** -Objekts während geöffnete **Recordset** -Objekte für die Verbindung vorhanden sind, wird ein Rollback für ausstehende Änderungen in allen **Recordset** -Objekten ausgeführt. Durch das explizite Schließen eines **Connection** -Objekts (Aufrufen der **Close** -Methode) während einer ausgeführten Transaktion wird ein Fehler generiert. Wenn ein **Connection** -Objekt während einer ausgeführten Transaktion außerhalb des Bereichs liegt, wird von ADO automatisch ein Rollback für die Transaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70875-p104">Closing a **Connection** object while there are open **Recordset** objects on the connection rolls back any pending changes in all of the **Recordset** objects. Explicitly closing a **Connection** object (calling the **Close** method) while a transaction is in progress generates an error. If a **Connection** object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</span></span>

<span data-ttu-id="70875-120">**Recordset, Record, Stream**</span><span class="sxs-lookup"><span data-stu-id="70875-120">**Recordset, Record, Stream**</span></span>

<span data-ttu-id="70875-p105">Beim Verwenden der **Close** -Methode zum Schließen der Objekte **Recordset**, **Record** oder **Stream** werden die zugeordneten Daten und jeder möglicherweise für Sie geltende exklusive Zugriff auf die Daten über das jeweilige Objekt freigegeben. Später können Sie die [Open](open-method-ado-recordset.md)-Methode aufrufen, um das Objekt mit den gleichen oder geänderten Attributen erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="70875-p105">Using the **Close** method to close a **Recordset**, **Record**, or **Stream** object releases the associated data and any exclusive access you may have had to the data through this particular object. You can later call the [Open](open-method-ado-recordset.md) method to reopen the object with the same, or modified, attributes.</span></span>

<span data-ttu-id="70875-123">Während ein **Recordset** -Objekt geschlossen ist, wird durch das Aufrufen von Methoden, die einen Livecursor erfordern, ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="70875-123">While a **Recordset** object is closed, calling any methods that require a live cursor generates an error.</span></span>

<span data-ttu-id="70875-p106">Wenn im Modus für sofortige Aktualisierungen eine Bearbeitung ausgeführt wird, wird durch Aufrufen der **Close** -Methode ein Fehler generiert; rufen Sie stattdessen erst die Methode [Update](update-method-ado.md) oder [CancelUpdate](cancelupdate-method-ado.md) auf. Wenn Sie das **Recordset** -Objekt im Batchaktualisierungsmodus schließen, gehen alle Änderungen seit dem letzten [UpdateBatch](updatebatch-method-ado.md)-Aufruf verloren.</span><span class="sxs-lookup"><span data-stu-id="70875-p106">If an edit is in progress while in immediate update mode, calling the **Close** method generates an error; instead, call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first. If you close the **Recordset** object while in batch update mode, all changes since the last [UpdateBatch](updatebatch-method-ado.md) call are lost.</span></span>

<span data-ttu-id="70875-126">Wenn Sie die [Clone](clone-method-ado.md)-Methode zum Erstellen von Kopien eines geöffneten **Recordset** -Objekts verwenden, wirkt sich das Schließen des Originals oder eines Klons nicht auf andere Kopien aus.</span><span class="sxs-lookup"><span data-stu-id="70875-126">If you use the [Clone](clone-method-ado.md) method to create copies of an open **Recordset** object, closing the original or a clone does not affect any of the other copies.</span></span>

