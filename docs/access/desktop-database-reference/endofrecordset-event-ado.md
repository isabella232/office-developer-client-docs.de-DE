---
title: EndOfRecordset-Ereignis (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293560"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="bc032-102">EndOfRecordset-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="bc032-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="bc032-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc032-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc032-104">Das **EndOfRecordset**-Ereignis wird aufgerufen, wenn in eine Zeile nach dem Ende des [Recordsets](recordset-object-ado.md) gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="bc032-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc032-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc032-105">Syntax</span></span>

<span data-ttu-id="bc032-106">EndOfRecordset*fMoreData*, *Status*, precordset \*\*</span><span class="sxs-lookup"><span data-stu-id="bc032-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="bc032-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc032-107">Parameters</span></span>

|<span data-ttu-id="bc032-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc032-108">Parameter</span></span>|<span data-ttu-id="bc032-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc032-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bc032-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="bc032-110">*fMoreData*</span></span> |<span data-ttu-id="bc032-111">Ein **Variant\_** -Wert vom Typ bool, der bei\_Festlegung auf Variant true angibt, dass dem **Recordset**-Objekt weitere Zeilen hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="bc032-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="bc032-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="bc032-112">*adStatus*</span></span> |<span data-ttu-id="bc032-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="bc032-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="bc032-114">Wenn **EndOfRecordset** aufgerufen wird, wird dieser Parameter auf **adStatusOK** festgelegt, falls die Operation, die zu diesem Ereignis führte, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="bc032-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="bc032-115">Er wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch der Operation, die zu diesem Ereignis führte, nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="bc032-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="bc032-116">Bevor **EndOfRecordset** zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="bc032-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="bc032-117">*precordset*</span><span class="sxs-lookup"><span data-stu-id="bc032-117">*pRecordset*</span></span> | <span data-ttu-id="bc032-p102">Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bc032-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bc032-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc032-120">Remarks</span></span>

<span data-ttu-id="bc032-121">Ein **EndOfRecordset** -Ereignis kann auftreten, wenn die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Operation fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="bc032-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="bc032-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="bc032-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="bc032-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bc032-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="bc032-124">Legen Sie in diesem Fall *fMoreData* auf Variant\_true fest, und geben Sie von **EndOfRecordset**zurück.</span><span class="sxs-lookup"><span data-stu-id="bc032-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="bc032-125">Then call **MoveNext** again to access the newly retrieved records.</span><span class="sxs-lookup"><span data-stu-id="bc032-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

