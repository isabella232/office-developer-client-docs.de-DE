---
title: ConnectComplete- und Disconnect-Ereignisse (ADO)
TOCTitle: ConnectComplete and Disconnect Events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 731879abf181f64c24b1012e45ea23435f965574
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475297"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="d45c5-102">ConnectComplete- und Disconnect-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="d45c5-102">ConnectComplete and Disconnect Events (ADO)</span></span>


<span data-ttu-id="d45c5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d45c5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d45c5-p101">Das **ConnectComplete**-Ereignis wird aufgerufen, nachdem eine Verbindung *gestartet* wurde. Das **Disconnect**-Ereignis wird aufgerufen, nachdem eine Verbindung *beendet* wurde.</span><span class="sxs-lookup"><span data-stu-id="d45c5-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45c5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d45c5-106">Syntax</span></span>

<span data-ttu-id="d45c5-107">ConnectComplete-*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="d45c5-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="d45c5-108">Trennen Sie*AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="d45c5-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="d45c5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d45c5-109">Parameters</span></span>

  - <span data-ttu-id="d45c5-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="d45c5-110">*pError*</span></span>

  - <span data-ttu-id="d45c5-p102">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d45c5-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="d45c5-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="d45c5-113">*adStatus*</span></span>

  - [<span data-ttu-id="d45c5-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="d45c5-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="d45c5-115">Wenn **ConnectComplete** aufgerufen wird, wird dieser Parameter auf **adStatusCancel** festgelegt, falls ein **WillConnect** -Ereignis den Abbruch der ausstehenden Verbindung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="d45c5-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="d45c5-p103">Bevor eines dieser Ereignisse zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Das Schließen und erneute Öffnen der [Verbindung](connection-object-ado.md) führt jedoch dazu, dass diese Ereignisse erneut auftreten.</span><span class="sxs-lookup"><span data-stu-id="d45c5-p103">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="d45c5-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="d45c5-118">*pConnection*</span></span>

  - <span data-ttu-id="d45c5-119">Das **Connection** -Objekt, für das dieses Ereignis gilt.</span><span class="sxs-lookup"><span data-stu-id="d45c5-119">The **Connection** object for which this event applies.</span></span>

