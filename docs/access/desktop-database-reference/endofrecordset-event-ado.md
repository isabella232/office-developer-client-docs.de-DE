---
title: EndOfRecordset-Ereignis (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36babff0c6de48e0539375caaad367698906e3fd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950188"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="7046c-102">EndOfRecordset-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="7046c-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="7046c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7046c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7046c-104">Das **EndOfRecordset** -Ereignis wird aufgerufen, wenn in eine Zeile nach dem Ende des [Recordsets](recordset-object-ado.md) gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="7046c-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7046c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7046c-105">Syntax</span></span>

<span data-ttu-id="7046c-106">EndOfRecordset*fMoreData*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="7046c-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="7046c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7046c-107">Parameters</span></span>

|<span data-ttu-id="7046c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7046c-108">Parameter</span></span>|<span data-ttu-id="7046c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7046c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7046c-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="7046c-110">*fMoreData*</span></span> |<span data-ttu-id="7046c-111">Eine **VARIANT\_BOOL** Wert festlegen Variante\_true ist, gibt das **Recordset**mehr Zeilen hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="7046c-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="7046c-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="7046c-112">*adStatus*</span></span> |<span data-ttu-id="7046c-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="7046c-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="7046c-114">Wenn **EndOfRecordset** aufgerufen wird, wird dieser Parameter auf **adStatusOK** festgelegt, falls die Operation, die zu diesem Ereignis führte, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7046c-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="7046c-115">Er wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch der Operation, die zu diesem Ereignis führte, nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="7046c-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="7046c-116">Bevor **EndOfRecordset** zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7046c-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="7046c-117">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="7046c-117">*pRecordset*</span></span> | <span data-ttu-id="7046c-p102">Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7046c-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7046c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7046c-120">Remarks</span></span>

<span data-ttu-id="7046c-121">Ein **EndOfRecordset** -Ereignis kann auftreten, wenn die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Operation fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="7046c-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="7046c-122">Dieser Ereignishandler wird aufgerufen, wenn versucht wird, vielleicht verschieben nach dem Ende des **Recordset** -Objekt als Ergebnis einer **MoveNext**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7046c-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="7046c-123">Klicken Sie in diesem Fall konnte Sie jedoch mehr Datensätze aus einer Datenbank abzurufen und sie bis zum Ende des **Recordset-Objekts**anfügen.</span><span class="sxs-lookup"><span data-stu-id="7046c-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="7046c-124">In diesem Fall Variante festlegen *fMoreData* \_TRUE und aus **EndOfRecordset**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7046c-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="7046c-125">Rufen Sie dann die **MoveNext** erneut aus, um die neu abgerufenen Datensätze zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7046c-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

