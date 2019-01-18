---
title: ConnectComplete- und Disconnect-Ereignisse (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699387"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="43396-102">ConnectComplete- und Disconnect-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="43396-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="43396-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43396-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43396-p101">Das **ConnectComplete**-Ereignis wird aufgerufen, nachdem eine Verbindung *gestartet* wurde. Das **Disconnect**-Ereignis wird aufgerufen, nachdem eine Verbindung *beendet* wurde.</span><span class="sxs-lookup"><span data-stu-id="43396-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="43396-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="43396-106">Syntax</span></span>

<span data-ttu-id="43396-107">ConnectComplete-*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="43396-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="43396-108">Trennen Sie*AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="43396-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="43396-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="43396-109">Parameters</span></span>

|<span data-ttu-id="43396-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="43396-110">Parameter</span></span>|<span data-ttu-id="43396-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43396-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="43396-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="43396-112">*pError*</span></span> |<span data-ttu-id="43396-p102">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43396-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="43396-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="43396-115">*adStatus*</span></span> |<span data-ttu-id="43396-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="43396-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="43396-117">Wenn **ConnectComplete** aufgerufen wird, wird dieser Parameter auf **adStatusCancel** festgelegt, falls ein **WillConnect** -Ereignis den Abbruch der ausstehenden Verbindung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="43396-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="43396-p104">Bevor eines dieser Ereignisse zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Das Schließen und erneute Öffnen der [Verbindung](connection-object-ado.md) führt jedoch dazu, dass diese Ereignisse erneut auftreten.</span><span class="sxs-lookup"><span data-stu-id="43396-p104">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="43396-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="43396-120">*pConnection*</span></span> |<span data-ttu-id="43396-121">Das **Connection** -Objekt, für das dieses Ereignis gilt.</span><span class="sxs-lookup"><span data-stu-id="43396-121">The **Connection** object for which this event applies.</span></span>|

