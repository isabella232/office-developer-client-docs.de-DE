---
title: ConnectComplete-und disConnect-Ereignisse (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295989"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="9f7f2-102">ConnectComplete-und disConnect-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="9f7f2-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="9f7f2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f7f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f7f2-104">Das **ConnectComplete**-Ereignis wird aufgerufen, nachdem eine Verbindung *gestartet* wurde.</span><span class="sxs-lookup"><span data-stu-id="9f7f2-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="9f7f2-105">Das **Disconnect**-Ereignis wird aufgerufen, nachdem eine Verbindung *beendet* wurde.</span><span class="sxs-lookup"><span data-stu-id="9f7f2-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f7f2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f7f2-106">Syntax</span></span>

<span data-ttu-id="9f7f2-107">ConnectComplete*pError*, \*\* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="9f7f2-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="9f7f2-108">DisConnect-*Status*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="9f7f2-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="9f7f2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f7f2-109">Parameters</span></span>

|<span data-ttu-id="9f7f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f7f2-110">Parameter</span></span>|<span data-ttu-id="9f7f2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f7f2-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9f7f2-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="9f7f2-112">*pError*</span></span> |<span data-ttu-id="9f7f2-p102">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f7f2-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="9f7f2-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="9f7f2-115">*adStatus*</span></span> |<span data-ttu-id="9f7f2-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="9f7f2-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="9f7f2-117">Wenn **ConnectComplete** aufgerufen wird, wird dieser Parameter auf **adStatusCancel** festgelegt, falls ein **WillConnect** -Ereignis den Abbruch der ausstehenden Verbindung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="9f7f2-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="9f7f2-p104">Bevor eines dieser Ereignisse zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Das Schließen und erneute Öffnen der [Verbindung](connection-object-ado.md) führt jedoch dazu, dass diese Ereignisse erneut auftreten.</span><span class="sxs-lookup"><span data-stu-id="9f7f2-p104">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="9f7f2-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="9f7f2-120">*pConnection*</span></span> |<span data-ttu-id="9f7f2-121">Das **Connection** -Objekt, für das dieses Ereignis gilt.</span><span class="sxs-lookup"><span data-stu-id="9f7f2-121">The **Connection** object for which this event applies.</span></span>|

