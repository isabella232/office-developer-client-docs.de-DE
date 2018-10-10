---
title: EndOfRecordset-Ereignis (ADO)
TOCTitle: EndOfRecordset Event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bdef3bdf0a2530fb37c71109d8626808695df8be
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474136"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="0a9ce-102">EndOfRecordset-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a9ce-102">EndOfRecordset Event (ADO)</span></span>


<span data-ttu-id="0a9ce-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a9ce-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="0a9ce-104">Das **EndOfRecordset** -Ereignis wird aufgerufen, wenn in eine Zeile nach dem Ende des [Recordsets](recordset-object-ado.md) gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a9ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a9ce-105">Syntax</span></span>

<span data-ttu-id="0a9ce-106">EndOfRecordset*fMoreData*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="0a9ce-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="0a9ce-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a9ce-107">Parameters</span></span>

  - <span data-ttu-id="0a9ce-108">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="0a9ce-108">*fMoreData*</span></span>

  - <span data-ttu-id="0a9ce-109">Eine **VARIANT\_BOOL** Wert festlegen Variante\_true ist, gibt das **Recordset**mehr Zeilen hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-109">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>

  - <span data-ttu-id="0a9ce-110">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="0a9ce-110">*adStatus*</span></span>

  - [<span data-ttu-id="0a9ce-111">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="0a9ce-111">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="0a9ce-p101">Wenn **EndOfRecordset** aufgerufen wird, wird dieser Parameter auf **adStatusOK** festgelegt, falls die Operation, die zu diesem Ereignis führte, erfolgreich war. Er wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch der Operation, die zu diesem Ereignis führte, nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-p101">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span>
    
    <span data-ttu-id="0a9ce-114">Bevor **EndOfRecordset** zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-114">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="0a9ce-115">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="0a9ce-115">*pRecordset*</span></span>

  - <span data-ttu-id="0a9ce-p102">Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a9ce-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a9ce-118">Remarks</span></span>

<span data-ttu-id="0a9ce-119">Ein **EndOfRecordset** -Ereignis kann auftreten, wenn die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Operation fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-119">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="0a9ce-120">Dieser Ereignishandler wird aufgerufen, wenn versucht wird, vielleicht verschieben nach dem Ende des **Recordset** -Objekt als Ergebnis einer **MoveNext**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-120">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="0a9ce-121">Klicken Sie in diesem Fall konnte Sie jedoch mehr Datensätze aus einer Datenbank abzurufen und sie bis zum Ende des **Recordset-Objekts**anfügen.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-121">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="0a9ce-122">In diesem Fall Variante festlegen *fMoreData* \_TRUE und aus **EndOfRecordset**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-122">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="0a9ce-123">Rufen Sie dann die **MoveNext** erneut aus, um die neu abgerufenen Datensätze zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0a9ce-123">Then call **MoveNext** again to access the newly retrieved records.</span></span>

