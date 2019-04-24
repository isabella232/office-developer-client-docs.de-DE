---
title: BeginTrans-, CommitTrans-und RollbackTrans-Methoden (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d9dc28bd64966e85d16ee2d8cb62fdebc3ba942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296871"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="17d5f-102">BeginTrans-, CommitTrans-und RollbackTrans-Methoden (ADO)</span><span class="sxs-lookup"><span data-stu-id="17d5f-102">BeginTrans, CommitTrans, and RollbackTrans methods (ADO)</span></span>

<span data-ttu-id="17d5f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17d5f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17d5f-104">Durch diese Transaktionsmethoden wird die Transaktionsverarbeitung in einem [Connection](connection-object-ado.md)-Objekt wie folgt verwaltet:</span><span class="sxs-lookup"><span data-stu-id="17d5f-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

- <span data-ttu-id="17d5f-105">**BeginTrans** - Eine neue Transaktion wird begonnen.</span><span class="sxs-lookup"><span data-stu-id="17d5f-105">**BeginTrans** — Begins a new transaction.</span></span>

- <span data-ttu-id="17d5f-p101">**CommitTrans** - Alle Änderungen werden gespeichert, und die aktuelle Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="17d5f-p101">**CommitTrans** — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span>

- <span data-ttu-id="17d5f-p102">**RollbackTrans** - Alle während der aktuellen Transaktion vorgenommenen Änderungen werden abgebrochen, und die Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="17d5f-p102">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction. It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d5f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="17d5f-110">Syntax</span></span>

<span data-ttu-id="17d5f-111">*Level* = -*Objekt*. BeginTrans ()</span><span class="sxs-lookup"><span data-stu-id="17d5f-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="17d5f-112">- *Objekt*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="17d5f-112">*object*.BeginTrans</span></span>

<span data-ttu-id="17d5f-113">- *Objekt*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="17d5f-113">*object*.CommitTrans</span></span>

<span data-ttu-id="17d5f-114">- *Objekt*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="17d5f-114">*object*.RollbackTrans</span></span>

## <a name="return-value"></a><span data-ttu-id="17d5f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17d5f-115">Return value</span></span>

<span data-ttu-id="17d5f-116">**BeginTrans** kann als Funktion aufgerufen werden, von der eine **Long**-Variable zurückgegeben wird, durch die die Schachtelungsebene der Transaktion angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="17d5f-116">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="17d5f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="17d5f-117">Parameters</span></span>

|<span data-ttu-id="17d5f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="17d5f-118">Parameter</span></span>|<span data-ttu-id="17d5f-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17d5f-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="17d5f-120">*Objekt*</span><span class="sxs-lookup"><span data-stu-id="17d5f-120">*object*</span></span> |<span data-ttu-id="17d5f-121">Ein **Connection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="17d5f-121">A **Connection** object.</span></span>|

### <a name="connection"></a><span data-ttu-id="17d5f-122">Verbindung</span><span class="sxs-lookup"><span data-stu-id="17d5f-122">Connection</span></span>

<span data-ttu-id="17d5f-p103">Verwenden Sie diese Methoden mit einem **Connection**-Objekt, wenn Sie eine Reihe von an den Quelldaten vorgenommenen Änderungen als einzelne Einheit speichern oder abbrechen möchten. Beispielsweise subtrahieren Sie zum Übertragen von Geldbeträgen zwischen Konten einen Betrag von einem Konto und addieren den gleichen Betrag zu einem anderen Konto. Wenn eine der Aktualisierungen fehlschlägt, sind die Konten nicht mehr ausgeglichen. Durch das Vornehmen dieser Änderungen mit einer geöffneten Transaktion wird sichergestellt, dass alle oder keine der Änderungen durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="17d5f-p103">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>

> [!NOTE]
> <span data-ttu-id="17d5f-127">Transaktionen werden nicht von allen Anbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17d5f-127">Not all providers support transactions.</span></span> <span data-ttu-id="17d5f-128">Stellen Sie sicher, dass die Anbieter definierte Eigenschaft **Transaction DDL** in der [Properties](properties-collection-ado.md) -Auflistung des **Connection** -Objekts angezeigt wird, was darauf hinweist, dass der Anbieter Transaktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17d5f-128">Verify that the provider-defined property **Transaction DDL** appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions.</span></span> <span data-ttu-id="17d5f-129">Wenn Transaktionen vom Anbieter nicht unterstützt werden, wird beim Aufrufen einer dieser Methoden ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17d5f-129">If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="17d5f-130">Nach dem Aufrufen der **BeginTrans**-Methode wird vom Anbieter erst wieder sofort ein Commit für vorgenommene Änderungen ausgeführt, wenn Sie **CommitTrans** oder **RollbackTrans** aufrufen, um die Transaktion zu beenden.</span><span class="sxs-lookup"><span data-stu-id="17d5f-130">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="17d5f-p105">Für Anbieter, von denen geschachtelte Transaktionen unterstützt werden, wird durch das Aufrufen der **BeginTrans**-Methode in einer geöffneten Transaktion eine neue geschachtelte Transaktion gestartet. Durch den Rückgabewert wird die Ebene der Schachtelung angegeben: Durch den Rückgabewert "1" wird angegeben, dass Sie eine Transaktion der obersten Ebene geöffnet haben (d. h., die Transaktion ist nicht in einer anderen Transaktion geschachtelt), durch "2" wird angegeben, dass Sie eine Transaktion der zweiten Ebene geöffnet haben (eine Transaktion, die in einer Transaktion der obersten Ebene geschachtelt ist) usw. Das Aufrufen von **CommitTrans** oder **RollbackTrans** wirkt sich nur auf die zuletzt geöffnete Transaktion aus. Sie müssen die aktuelle Transaktion schließen oder ein Rollback ausführen, bevor Sie Transaktionen einer höheren Ebene auflösen können.</span><span class="sxs-lookup"><span data-stu-id="17d5f-p105">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="17d5f-p106">Durch das Aufrufen der **CommitTrans** -Methode werden in einer geöffneten Transaktion vorgenommene Änderungen für die Verbindung gespeichert, und die Transaktion wird beendet. Durch das Aufrufen der **RollbackTrans** -Methode werden alle in einer geöffneten Transaktion vorgenommenen Änderungen rückgängig gemacht, und die Transaktion wird beendet. Durch das Aufrufen einer der Methoden ohne geöffnete Transaktion wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="17d5f-p106">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="17d5f-p107">Abhängig von der **Attributes**-Eigenschaft des [Connection](attributes-property-ado.md) -Objekts wird durch das Aufrufen der Methoden **CommitTrans** oder **RollbackTrans** möglicherweise automatisch eine neue Transaktion gestartet. Wenn die **Attributes** -Eigenschaft auf **adXactCommitRetaining** festgelegt ist, wird nach einem **CommitTrans** -Aufruf automatisch vom Anbieter eine neue Transaktion gestartet. Wenn die **Attributes** -Eigenschaft auf **adXactAbortRetaining** festgelegt ist, wird nach einem **RollbackTrans** -Aufruf automatisch vom Anbieter eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="17d5f-p107">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction. If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call. If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

### <a name="remote-data-service"></a><span data-ttu-id="17d5f-140">Remote Data Service</span><span class="sxs-lookup"><span data-stu-id="17d5f-140">Remote Data Service</span></span>

<span data-ttu-id="17d5f-141">Die Methoden **BeginTrans**, **CommitTrans** und **RollbackTrans** stehen für ein clientseitiges **Connection**-Objekt nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="17d5f-141">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

