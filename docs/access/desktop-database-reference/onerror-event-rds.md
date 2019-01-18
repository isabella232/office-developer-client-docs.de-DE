---
title: onError-Ereignis (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712176"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="10800-102">onError-Ereignis (RDS)</span><span class="sxs-lookup"><span data-stu-id="10800-102">onError event (RDS)</span></span>

<span data-ttu-id="10800-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10800-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10800-104">Wenn während eines Vorgangs ein Fehler auftritt, wird das **OnError** -Ereignis aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="10800-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="10800-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10800-105">Syntax</span></span>

<span data-ttu-id="10800-106">OnError*SCode*, *Beschreibung*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="10800-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="10800-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="10800-107">Parameters</span></span>

|<span data-ttu-id="10800-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10800-108">Parameter</span></span>|<span data-ttu-id="10800-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10800-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="10800-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="10800-110">*SCode*</span></span> |<span data-ttu-id="10800-111">Eine ganze Zahl, die den Statuscode des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="10800-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="10800-112">*Description*</span><span class="sxs-lookup"><span data-stu-id="10800-112">*Description*</span></span> |<span data-ttu-id="10800-113">Eine **Zeichenfolge** , die eine Beschreibung des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="10800-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="10800-114">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="10800-114">*Source*</span></span> |<span data-ttu-id="10800-115">Eine **Zeichenfolge** , die angibt, die Abfrage oder den Befehl, der den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="10800-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="10800-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="10800-116">*CancelDisplay*</span></span> |<span data-ttu-id="10800-117">Ein **boolescher** Wert, die bei auf **True**festgelegt, die verhindert, dass den Fehler in einem Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="10800-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

