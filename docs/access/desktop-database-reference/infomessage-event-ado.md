---
title: InfoMessage-Ereignis (ADO)
TOCTitle: InfoMessage Event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6cc3b69eb3310d8e717605edd3d6fae32d635806
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476041"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="7d532-102">InfoMessage-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="7d532-102">InfoMessage Event (ADO)</span></span>


<span data-ttu-id="7d532-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d532-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7d532-104">Das **InfoMessage** -Ereignis wird aufgerufen, wenn eine Warnung während einer **ConnectionEvent** -Operation auftritt.</span><span class="sxs-lookup"><span data-stu-id="7d532-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d532-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d532-105">Syntax</span></span>

<span data-ttu-id="7d532-106">InfoMessage*pError*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="7d532-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="7d532-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d532-107">Parameters</span></span>

  - <span data-ttu-id="7d532-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="7d532-108">*pError*</span></span>

  - <span data-ttu-id="7d532-p101">Ein [Error](error-object-ado.md)-Objekt. Dieser Parameter enthält sämtliche Fehler, die zurückgegeben werden. Wenn mehrere Fehler zurückgegeben werden, zählen Sie die **Fehler** -Auflistung auf, um sie zu finden.</span><span class="sxs-lookup"><span data-stu-id="7d532-p101">An [Error](error-object-ado.md) object. This parameter contains any errors that are returned. If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>

  - <span data-ttu-id="7d532-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="7d532-112">*adStatus*</span></span>

  - [<span data-ttu-id="7d532-113">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="7d532-113">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="7d532-114">Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7d532-114">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="7d532-115">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="7d532-115">*pConnection*</span></span>

  - <span data-ttu-id="7d532-116">Ein [Connection](connection-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d532-116">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="7d532-117">Die Verbindung, für die die Warnung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7d532-117">The connection for which the warning occurred.</span></span> <span data-ttu-id="7d532-118">Warnungen können beispielsweise auftreten, wenn eine **Verbindung** öffnen-Objekt oder das Ausführen eines [Befehls](command-object-ado.md) für eine **Verbindung**.</span><span class="sxs-lookup"><span data-stu-id="7d532-118">For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>

