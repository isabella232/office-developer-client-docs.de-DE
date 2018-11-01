---
title: ExecuteComplete-Ereignis (ADO)
TOCTitle: ExecuteComplete Event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e29db2848d7ec7b229831156ee64815a152a4bfc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887901"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="316c8-102">ExecuteComplete-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="316c8-102">ExecuteComplete Event (ADO)</span></span>


<span data-ttu-id="316c8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="316c8-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="316c8-104">Das **ExecuteComplete** -Ereignis wird aufgerufen, nachdem ein Befehl ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="316c8-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="316c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="316c8-105">Syntax</span></span>

<span data-ttu-id="316c8-106">ExecuteComplete*RecordsAffected*, *pError*, *AdStatus*, *pCommand*, *pCommand*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="316c8-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="316c8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="316c8-107">Parameters</span></span>

  - <span data-ttu-id="316c8-108">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="316c8-108">*RecordsAffected*</span></span>

  - <span data-ttu-id="316c8-109">Ein **Long** -Wert, der die Anzahl von Datensätzen angibt, auf die sich der Befehl auswirkt.</span><span class="sxs-lookup"><span data-stu-id="316c8-109">A **Long** value indicating the number of records affected by the command.</span></span>

  - <span data-ttu-id="316c8-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="316c8-110">*pError*</span></span>

  - <span data-ttu-id="316c8-p101">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="316c8-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="316c8-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="316c8-113">*adStatus*</span></span>

  - [<span data-ttu-id="316c8-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="316c8-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="316c8-115">Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="316c8-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="316c8-116">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="316c8-116">*pCommand*</span></span>

  - <span data-ttu-id="316c8-117">Das [Command](command-object-ado.md) -Objekt, das ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="316c8-117">The [Command](command-object-ado.md) object that was executed.</span></span> <span data-ttu-id="316c8-118">Enthält ein **Command** -Objekt, selbst wenn **Connection.Execute** oder **Recordset.Open** ohne explizit Erstellen eines **Befehls**, in denen Anfragen das **Command** -Objekt von ADO intern erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="316c8-118">Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>

  - <span data-ttu-id="316c8-119">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="316c8-119">*pRecordset*</span></span>

  - <span data-ttu-id="316c8-p103">Ein [Recordset](recordset-object-ado.md)-Objekt, das das Ergebnis des ausgeführten Befehls darstellt. Dieses Recordset kann leer sein. Sie sollten dieses **Recordset** -Objekt niemals innerhalb dieses Ereignishandlers zerstören. Andernfalls führt dies zu einer Access-Verletzung, wenn ADO versucht, auf ein Objekt zuzugreifen, das nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="316c8-p103">A [Recordset](recordset-object-ado.md) object that is the result of the executed command. This **Recordset** may be empty. You should never destroy this Recordset object from within this event handler. Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>

  - <span data-ttu-id="316c8-124">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="316c8-124">*pConnection*</span></span>

  - <span data-ttu-id="316c8-p104">Ein [Connection](connection-object-ado.md)-Objekt. Die Verbindung, über die die Operation ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="316c8-p104">A [Connection](connection-object-ado.md) object. The connection over which the operation was executed.</span></span>

## <a name="remarks"></a><span data-ttu-id="316c8-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="316c8-127">Remarks</span></span>

<span data-ttu-id="316c8-128">Ein **ExecuteComplete** -Ereignis kann aufgrund der Methoden **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) oder **Recordset.**[NextRecordset](nextrecordset-method-ado.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="316c8-128">An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>

