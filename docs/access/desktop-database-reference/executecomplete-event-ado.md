---
title: ExecuteComplete-Ereignis (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293224"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="aea6e-102">ExecuteComplete-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="aea6e-102">ExecuteComplete event (ADO)</span></span>

<span data-ttu-id="aea6e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aea6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aea6e-104">Das **ExecuteComplete**-Ereignis wird aufgerufen, nachdem ein Befehl ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="aea6e-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aea6e-105">Syntax</span></span>

<span data-ttu-id="aea6e-106">ExecuteComplete*RecordsAffected*, *pError*, \*\* *pCommand*, precordset \*\*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="aea6e-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="aea6e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aea6e-107">Parameters</span></span>

|<span data-ttu-id="aea6e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aea6e-108">Parameter</span></span>|<span data-ttu-id="aea6e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aea6e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="aea6e-110">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="aea6e-110">*RecordsAffected*</span></span> |<span data-ttu-id="aea6e-111">Ein **Long** -Wert, der die Anzahl von Datensätzen angibt, auf die sich der Befehl auswirkt.</span><span class="sxs-lookup"><span data-stu-id="aea6e-111">A **Long** value indicating the number of records affected by the command.</span></span>|
|<span data-ttu-id="aea6e-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="aea6e-112">*pError*</span></span> |<span data-ttu-id="aea6e-p101">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aea6e-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="aea6e-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="aea6e-115">*adStatus*</span></span> |<span data-ttu-id="aea6e-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="aea6e-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="aea6e-117">Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="aea6e-117">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="aea6e-118">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="aea6e-118">*pCommand*</span></span> |<span data-ttu-id="aea6e-p103">The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span><span class="sxs-lookup"><span data-stu-id="aea6e-p103">The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>|
|<span data-ttu-id="aea6e-121">*precordset*</span><span class="sxs-lookup"><span data-stu-id="aea6e-121">*pRecordset*</span></span> |<span data-ttu-id="aea6e-p104">Ein [Recordset](recordset-object-ado.md)-Objekt, das das Ergebnis des ausgeführten Befehls darstellt. Dieses Recordset kann leer sein. Sie sollten dieses **Recordset** -Objekt niemals innerhalb dieses Ereignishandlers zerstören. Andernfalls führt dies zu einer Access-Verletzung, wenn ADO versucht, auf ein Objekt zuzugreifen, das nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aea6e-p104">A [Recordset](recordset-object-ado.md) object that is the result of the executed command. This **Recordset** may be empty. You should never destroy this Recordset object from within this event handler. Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>|
|<span data-ttu-id="aea6e-126">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="aea6e-126">*pConnection*</span></span> |<span data-ttu-id="aea6e-p105">Ein [Connection](connection-object-ado.md)-Objekt. Die Verbindung, über die die Operation ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="aea6e-p105">A [Connection](connection-object-ado.md) object. The connection over which the operation was executed.</span></span>|

## <a name="remarks"></a><span data-ttu-id="aea6e-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aea6e-129">Remarks</span></span>

<span data-ttu-id="aea6e-130">Ein **ExecuteComplete**-Ereignis kann aufgrund der Methoden **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) oder **Recordset.**[NextRecordset](nextrecordset-method-ado.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="aea6e-130">An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>

