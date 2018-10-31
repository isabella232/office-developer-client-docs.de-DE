---
title: Methoden 'BeginTrans', 'CommitTrans' und 'RollbackTrans' (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 719c495e18fb769a2d3f994542ab8d9e93a469f1
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860378"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="7b553-102">Methoden "BeginTrans", "CommitTrans" und "RollbackTrans" (ADO)</span><span class="sxs-lookup"><span data-stu-id="7b553-102">BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)</span></span>


<span data-ttu-id="7b553-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b553-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="7b553-104">Durch diese Transaktionsmethoden wird die Transaktionsverarbeitung in einem [Connection](connection-object-ado.md)-Objekt wie folgt verwaltet:</span><span class="sxs-lookup"><span data-stu-id="7b553-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

  - <span data-ttu-id="7b553-105">**BeginTrans** - Eine neue Transaktion wird begonnen.</span><span class="sxs-lookup"><span data-stu-id="7b553-105">**BeginTrans** — Begins a new transaction.</span></span>

  - <span data-ttu-id="7b553-p101">**CommitTrans** - Alle Änderungen werden gespeichert, und die aktuelle Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="7b553-p101">**CommitTrans** — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span>

  - <span data-ttu-id="7b553-p102">**RollbackTrans** - Alle während der aktuellen Transaktion vorgenommenen Änderungen werden abgebrochen, und die Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="7b553-p102">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction. It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b553-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b553-110">Syntax</span></span>

<span data-ttu-id="7b553-111">*Ebene* = *Objekt*. BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="7b553-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="7b553-112">- *Objekt*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="7b553-112">*object*.BeginTrans</span></span>

<span data-ttu-id="7b553-113">- *Objekt*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="7b553-113">*object*.CommitTrans</span></span>

<span data-ttu-id="7b553-114">- *Objekt*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="7b553-114">*object*.RollbackTrans</span></span>

<span data-ttu-id="7b553-115"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7b553-115"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="7b553-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b553-116">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="7b553-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b553-117">Return value</span></span>
>>>>>>> <span data-ttu-id="7b553-118">master</span><span class="sxs-lookup"><span data-stu-id="7b553-118">master</span></span>

<span data-ttu-id="7b553-119">**BeginTrans** kann als Funktion aufgerufen werden, von der eine **Long** -Variable zurückgegeben wird, durch die die Schachtelungsebene der Transaktion angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7b553-119">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b553-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b553-120">Parameters</span></span>

  - <span data-ttu-id="7b553-121">*Objekt*</span><span class="sxs-lookup"><span data-stu-id="7b553-121">*object*</span></span>

  - <span data-ttu-id="7b553-122">Ein **Connection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7b553-122">A **Connection** object.</span></span>

<span data-ttu-id="7b553-123">**Connection**</span><span class="sxs-lookup"><span data-stu-id="7b553-123">**Connection**</span></span>

<span data-ttu-id="7b553-p103">Verwenden Sie diese Methoden mit einem **Connection** -Objekt, wenn Sie eine Reihe von an den Quelldaten vorgenommenen Änderungen als einzelne Einheit speichern oder abbrechen möchten. Beispielsweise subtrahieren Sie zum Übertragen von Geldbeträgen zwischen Konten einen Betrag von einem Konto und addieren den gleichen Betrag zu einem anderen Konto. Wenn eine der Aktualisierungen fehlschlägt, sind die Konten nicht mehr ausgeglichen. Durch das Vornehmen dieser Änderungen mit einer geöffneten Transaktion wird sichergestellt, dass alle oder keine der Änderungen durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="7b553-p103">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>


> [!NOTE]
> <span data-ttu-id="7b553-p104">Transaktionen werden nicht von allen Anbietern unterstützt. Überprüfen Sie, ob die vom Anbieter definierte "**Transaction DDL**"-Eigenschaft in der [Properties](properties-collection-ado.md)-Auflistung des **Connection**-Objekts angezeigt wird und damit angibt, dass Transaktionen vom Anbieter unterstützt werden. Wenn Transaktionen vom Anbieter nicht unterstützt werden, wird beim Aufrufen einer dieser Methoden ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b553-p104">Not all providers support transactions. Verify that the provider-defined property "**Transaction DDL**" appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions. If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="7b553-131">Nach dem Aufrufen der **BeginTrans** -Methode wird vom Anbieter erst wieder sofort ein Commit für vorgenommene Änderungen ausgeführt, wenn Sie **CommitTrans** oder **RollbackTrans** aufrufen, um die Transaktion zu beenden.</span><span class="sxs-lookup"><span data-stu-id="7b553-131">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="7b553-p105">Für Anbieter, von denen geschachtelte Transaktionen unterstützt werden, wird durch das Aufrufen der **BeginTrans** -Methode in einer geöffneten Transaktion eine neue geschachtelte Transaktion gestartet. Durch den Rückgabewert wird die Ebene der Schachtelung angegeben: Durch den Rückgabewert "1" wird angegeben, dass Sie eine Transaktion der obersten Ebene geöffnet haben (d. h., die Transaktion ist nicht in einer anderen Transaktion geschachtelt), durch "2" wird angegeben, dass Sie eine Transaktion der zweiten Ebene geöffnet haben (eine Transaktion, die in einer Transaktion der obersten Ebene geschachtelt ist) usw. Das Aufrufen von **CommitTrans** oder **RollbackTrans** wirkt sich nur auf die zuletzt geöffnete Transaktion aus. Sie müssen die aktuelle Transaktion schließen oder ein Rollback ausführen, bevor Sie Transaktionen einer höheren Ebene auflösen können.</span><span class="sxs-lookup"><span data-stu-id="7b553-p105">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="7b553-p106">Durch das Aufrufen der **CommitTrans** -Methode werden in einer geöffneten Transaktion vorgenommene Änderungen für die Verbindung gespeichert, und die Transaktion wird beendet. Durch das Aufrufen der **RollbackTrans** -Methode werden alle in einer geöffneten Transaktion vorgenommenen Änderungen rückgängig gemacht, und die Transaktion wird beendet. Durch das Aufrufen einer der Methoden ohne geöffnete Transaktion wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="7b553-p106">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="7b553-p107">Abhängig von der **Attributes**-Eigenschaft des [Connection](attributes-property-ado.md) -Objekts wird durch das Aufrufen der Methoden **CommitTrans** oder **RollbackTrans** möglicherweise automatisch eine neue Transaktion gestartet. Wenn die **Attributes** -Eigenschaft auf **adXactCommitRetaining** festgelegt ist, wird nach einem **CommitTrans** -Aufruf automatisch vom Anbieter eine neue Transaktion gestartet. Wenn die **Attributes** -Eigenschaft auf **adXactAbortRetaining** festgelegt ist, wird nach einem **RollbackTrans** -Aufruf automatisch vom Anbieter eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="7b553-p107">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction. If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call. If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

<span data-ttu-id="7b553-141">**Remote Data Service**</span><span class="sxs-lookup"><span data-stu-id="7b553-141">**Remote Data Service**</span></span>

<span data-ttu-id="7b553-142">Die Methoden **BeginTrans**, **CommitTrans** und **RollbackTrans** stehen für ein clientseitiges **Connection** -Objekt nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7b553-142">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

