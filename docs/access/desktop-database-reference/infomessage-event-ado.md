---
title: InfoMessage-Ereignis (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699898"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="c7eac-102">InfoMessage-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="c7eac-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="c7eac-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7eac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7eac-104">Das **InfoMessage** -Ereignis wird aufgerufen, wenn eine Warnung während einer **ConnectionEvent** -Operation auftritt.</span><span class="sxs-lookup"><span data-stu-id="c7eac-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7eac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7eac-105">Syntax</span></span>

<span data-ttu-id="c7eac-106">InfoMessage*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="c7eac-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="c7eac-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7eac-107">Parameters</span></span>

|<span data-ttu-id="c7eac-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7eac-108">Parameter</span></span>|<span data-ttu-id="c7eac-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7eac-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c7eac-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="c7eac-110">*pError*</span></span> |<span data-ttu-id="c7eac-p101">Ein [Error](error-object-ado.md)-Objekt. Dieser Parameter enthält sämtliche Fehler, die zurückgegeben werden. Wenn mehrere Fehler zurückgegeben werden, zählen Sie die **Fehler** -Auflistung auf, um sie zu finden.</span><span class="sxs-lookup"><span data-stu-id="c7eac-p101">An [Error](error-object-ado.md) object. This parameter contains any errors that are returned. If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="c7eac-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="c7eac-114">*adStatus*</span></span> |<span data-ttu-id="c7eac-115">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="c7eac-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="c7eac-116">Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="c7eac-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="c7eac-117">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="c7eac-117">*pConnection*</span></span> |<span data-ttu-id="c7eac-118">Ein [Connection](connection-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c7eac-118">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="c7eac-119">Die Verbindung, für die die Warnung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c7eac-119">The connection for which the warning occurred.</span></span> <span data-ttu-id="c7eac-120">Warnungen können beispielsweise auftreten, wenn eine **Verbindung** öffnen-Objekt oder das Ausführen eines [Befehls](command-object-ado.md) für eine **Verbindung**.</span><span class="sxs-lookup"><span data-stu-id="c7eac-120">For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

