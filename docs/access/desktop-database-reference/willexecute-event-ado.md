---
title: WillExecute-Ereignis (ADO)
TOCTitle: WillExecute Event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3cdf4764cca2b40cee62f9d66ea748a4e627a5f
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606843"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="73602-102">WillExecute-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="73602-102">WillExecute Event (ADO)</span></span>


<span data-ttu-id="73602-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="73602-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="73602-104">Das **WillExecute** -Ereignis wird unmittelbar vor dem Ausführen eines ausstehenden Befehls für eine Verbindung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73602-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="73602-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73602-105">Syntax</span></span>

<span data-ttu-id="73602-106">WillExecute*Source*, *CursorType*, *LockType*, *Optionen*, *AdStatus*, *pCommand*, *pCommand*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="73602-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="73602-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="73602-107">Parameters</span></span>

  - <span data-ttu-id="73602-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="73602-108">*Source*</span></span>

  - <span data-ttu-id="73602-109">Ein **String** -Wert, der einen SQL-Befehl oder den Namen einer gespeicherten Prozedur enthält.</span><span class="sxs-lookup"><span data-stu-id="73602-109">A **String** that contains an SQL command or a stored procedure name.</span></span>

  - <span data-ttu-id="73602-110">*CursorType*</span><span class="sxs-lookup"><span data-stu-id="73602-110">*CursorType*</span></span>

  - <span data-ttu-id="73602-111">Ein [CursorTypeEnum](cursortypeenum.md)-Wert, der den Cursortyp für das **Recordset** -Objekt angibt, dass geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="73602-111">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="73602-112">Mit diesem Parameter können Sie den Cursor während ein Vorgang zum [Öffnen](open-method-ado-recordset.md) des **Recordset-Objekt** für jede Art ändern.</span><span class="sxs-lookup"><span data-stu-id="73602-112">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="73602-113">*CursorType* wird für alle anderen Vorgänge ignoriert.</span><span class="sxs-lookup"><span data-stu-id="73602-113">*CursorType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="73602-114">*LockType*</span><span class="sxs-lookup"><span data-stu-id="73602-114">*LockType*</span></span>

  - <span data-ttu-id="73602-115">Ein [LockTypeEnum](locktypeenum.md)-Wert, der den Sperrtyp für das **Recordset** -Objekt enthält, das geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="73602-115">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="73602-116">Mit diesem Parameter können Sie beim **Open** -Vorgang des **Recordset** -Objekts die Sperre in einen beliebigen Typ ändern.</span><span class="sxs-lookup"><span data-stu-id="73602-116">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="73602-117">*LockType* wird für alle anderen Vorgänge ignoriert.</span><span class="sxs-lookup"><span data-stu-id="73602-117">*LockType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="73602-118">*Options*</span><span class="sxs-lookup"><span data-stu-id="73602-118">*Options*</span></span>

  - <span data-ttu-id="73602-119">Ein **Long** -Wert, der die Optionen angibt, die zum Ausführen des Befehls oder zum Öffnen des **Recordset** -Objekts verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="73602-119">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>

  - <span data-ttu-id="73602-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="73602-120">*adStatus*</span></span>

  - [<span data-ttu-id="73602-121">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="73602-121">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="73602-122">Legen Sie diesen Parameter vor Rückgabe des Ereignisses auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Oder legen Sie ihn auf **adStatusCancel** fest, um den Abbruch des das Ereignis verursachenden Vorgangs anzufordern.</span><span class="sxs-lookup"><span data-stu-id="73602-122">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>

  - <span data-ttu-id="73602-123">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="73602-123">*pCommand*</span></span>

  - <span data-ttu-id="73602-124">Das [Command](command-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt.</span><span class="sxs-lookup"><span data-stu-id="73602-124">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="73602-125">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="73602-125">*pRecordset*</span></span>

  - <span data-ttu-id="73602-126">Das [Recordset](recordset-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt.</span><span class="sxs-lookup"><span data-stu-id="73602-126">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="73602-127">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="73602-127">*pConnection*</span></span>

  - <span data-ttu-id="73602-128">Das [Connection](connection-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt.</span><span class="sxs-lookup"><span data-stu-id="73602-128">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>

## <a name="remarks"></a><span data-ttu-id="73602-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="73602-129">Remarks</span></span>

<span data-ttu-id="73602-130"><<<<<<< HEAD **WillExecute** -Ereignis kann aufgrund von Auftreten einer **Verbindung.** [Führen Sie](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) **Befehl.** Wird [ausgeführt](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), oder **Recordset.** [Open](open-method-ado-recordset.md) -Methode *eintreten* sollte immer einen gültigen Verweis auf ein **Connection** -Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="73602-130"><<<<<<< HEAD A **WillExecute** event may occur due to a **Connection.**[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **Command.**[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="73602-131">Wenn das Ereignis aufgrund der **Methoden Connection.Execute**, werden die Parameter *pCommand* und *pCommand* auf **Nothing**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73602-131">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="73602-132">Ist das Ereignis aufgrund **Recordset.Open**, der *pCommand* -Parameter wird das **Recordset** -Objekt verweisen, und der Parameter *pCommand* auf **Nothing**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73602-132">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="73602-133">Ist das Ereignis aufgrund von **Command.Execute**, Parameters *pCommand* verweist auf das **Command** -Objekt, und der Parameter *pCommand* auf **Nothing**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73602-133">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>
<span data-ttu-id="73602-134">=== Ein **WillExecute** -Ereignis kann aufgrund von Auftreten einer **Verbindung.** [Führen Sie](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) **Befehl.** Wird [ausgeführt](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), oder **Recordset.** [Open](open-method-ado-recordset.md) -Methode *eintreten* sollte immer einen gültigen Verweis auf ein **Connection** -Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="73602-134">======= A **WillExecute** event may occur due to a **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="73602-135">Wenn das Ereignis aufgrund der **Methoden Connection.Execute**, werden die Parameter *pCommand* und *pCommand* auf **Nothing**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73602-135">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="73602-136">Ist das Ereignis aufgrund **Recordset.Open**, der *pCommand* -Parameter wird das **Recordset** -Objekt verweisen, und der Parameter *pCommand* auf **Nothing**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73602-136">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="73602-137">Ist das Ereignis aufgrund von **Command.Execute**, Parameters *pCommand* verweist auf das **Command** -Objekt, und der Parameter *pCommand* auf **Nothing**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73602-137">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>
>>>>>>> <span data-ttu-id="73602-138">master</span><span class="sxs-lookup"><span data-stu-id="73602-138">master</span></span>

<span data-ttu-id="73602-p104">Mit **WillExecute** können Sie die ausstehenden Ausführungsparameter untersuchen und ändern. Dieses Ereignis kann eine Anforderung zurückgeben, dass der ausstehende Befehl abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="73602-p104">**WillExecute** allows you to examine and modify the pending execution parameters. This event may return a request that the pending command be canceled.</span></span>

