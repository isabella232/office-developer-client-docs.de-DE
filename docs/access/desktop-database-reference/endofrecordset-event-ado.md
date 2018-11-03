---
title: EndOfRecordset-Ereignis (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89ca397c4e95dd6f18de41862e9383f77fe14aa8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928838"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="e93d6-102">EndOfRecordset-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="e93d6-102">EndOfRecordset event (ADO)</span></span>


<span data-ttu-id="e93d6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e93d6-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="e93d6-104">Das **EndOfRecordset** -Ereignis wird aufgerufen, wenn in eine Zeile nach dem Ende des [Recordsets](recordset-object-ado.md) gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="e93d6-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e93d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e93d6-105">Syntax</span></span>

<span data-ttu-id="e93d6-106">EndOfRecordset*fMoreData*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="e93d6-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="e93d6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e93d6-107">Parameters</span></span>

  - <span data-ttu-id="e93d6-108">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="e93d6-108">*fMoreData*</span></span>

  - <span data-ttu-id="e93d6-109">Eine **VARIANT\_BOOL** Wert festlegen Variante\_true ist, gibt das **Recordset**mehr Zeilen hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="e93d6-109">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>

  - <span data-ttu-id="e93d6-110">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="e93d6-110">*adStatus*</span></span>

  - [<span data-ttu-id="e93d6-111">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="e93d6-111">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="e93d6-p101">Wenn **EndOfRecordset** aufgerufen wird, wird dieser Parameter auf **adStatusOK** festgelegt, falls die Operation, die zu diesem Ereignis führte, erfolgreich war. Er wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch der Operation, die zu diesem Ereignis führte, nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="e93d6-p101">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span>
    
    <span data-ttu-id="e93d6-114">Bevor **EndOfRecordset** zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="e93d6-114">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="e93d6-115">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="e93d6-115">*pRecordset*</span></span>

  - <span data-ttu-id="e93d6-p102">Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e93d6-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e93d6-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e93d6-118">Remarks</span></span>

<span data-ttu-id="e93d6-119">Ein **EndOfRecordset** -Ereignis kann auftreten, wenn die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Operation fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="e93d6-119">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="e93d6-120">Dieser Ereignishandler wird aufgerufen, wenn versucht wird, vielleicht verschieben nach dem Ende des **Recordset** -Objekt als Ergebnis einer **MoveNext**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e93d6-120">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="e93d6-121">Klicken Sie in diesem Fall konnte Sie jedoch mehr Datensätze aus einer Datenbank abzurufen und sie bis zum Ende des **Recordset-Objekts**anfügen.</span><span class="sxs-lookup"><span data-stu-id="e93d6-121">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="e93d6-122">In diesem Fall Variante festlegen *fMoreData* \_TRUE und aus **EndOfRecordset**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e93d6-122">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="e93d6-123">Rufen Sie dann die **MoveNext** erneut aus, um die neu abgerufenen Datensätze zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e93d6-123">Then call **MoveNext** again to access the newly retrieved records.</span></span>

