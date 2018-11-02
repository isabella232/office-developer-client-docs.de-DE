---
title: ConnectComplete- und Disconnect-Ereignisse (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ab98e270fd52d656bf722c7f666afbe22d5ea44
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926304"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="8d82d-102">ConnectComplete- und Disconnect-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d82d-102">ConnectComplete and Disconnect events (ADO)</span></span>


<span data-ttu-id="8d82d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d82d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d82d-p101">Das **ConnectComplete**-Ereignis wird aufgerufen, nachdem eine Verbindung *gestartet* wurde. Das **Disconnect**-Ereignis wird aufgerufen, nachdem eine Verbindung *beendet* wurde.</span><span class="sxs-lookup"><span data-stu-id="8d82d-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d82d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d82d-106">Syntax</span></span>

<span data-ttu-id="8d82d-107">ConnectComplete-*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="8d82d-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="8d82d-108">Trennen Sie*AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="8d82d-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="8d82d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d82d-109">Parameters</span></span>

  - <span data-ttu-id="8d82d-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="8d82d-110">*pError*</span></span>

  - <span data-ttu-id="8d82d-p102">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d82d-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="8d82d-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="8d82d-113">*adStatus*</span></span>

  - [<span data-ttu-id="8d82d-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="8d82d-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="8d82d-115">Wenn **ConnectComplete** aufgerufen wird, wird dieser Parameter auf **adStatusCancel** festgelegt, falls ein **WillConnect** -Ereignis den Abbruch der ausstehenden Verbindung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="8d82d-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="8d82d-p103">Bevor eines dieser Ereignisse zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Das Schließen und erneute Öffnen der [Verbindung](connection-object-ado.md) führt jedoch dazu, dass diese Ereignisse erneut auftreten.</span><span class="sxs-lookup"><span data-stu-id="8d82d-p103">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="8d82d-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="8d82d-118">*pConnection*</span></span>

  - <span data-ttu-id="8d82d-119">Das **Connection** -Objekt, für das dieses Ereignis gilt.</span><span class="sxs-lookup"><span data-stu-id="8d82d-119">The **Connection** object for which this event applies.</span></span>

