---
title: onError-Ereignis (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fe6f6b78297008e25e15dc17e243ae982a5ccf3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475768"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="3a4d1-102">onError-Ereignis (RDS)</span><span class="sxs-lookup"><span data-stu-id="3a4d1-102">onError Event (RDS)</span></span>


<span data-ttu-id="3a4d1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a4d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3a4d1-104">Wenn während eines Vorgangs ein Fehler auftritt, wird das **OnError** -Ereignis aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a4d1-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a4d1-105">Syntax</span></span>

<span data-ttu-id="3a4d1-106">OnError*SCode*, *Beschreibung*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="3a4d1-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="3a4d1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a4d1-107">Parameters</span></span>

  - <span data-ttu-id="3a4d1-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="3a4d1-108">*SCode*</span></span>

  - <span data-ttu-id="3a4d1-109">Eine ganze Zahl, die den Statuscode des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="3a4d1-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="3a4d1-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="3a4d1-110">*Description*</span></span>

  - <span data-ttu-id="3a4d1-111">Eine **Zeichenfolge** , die eine Beschreibung des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="3a4d1-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="3a4d1-112">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="3a4d1-112">*Source*</span></span>

  - <span data-ttu-id="3a4d1-113">Eine **Zeichenfolge** , die angibt, die Abfrage oder den Befehl, der den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="3a4d1-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="3a4d1-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="3a4d1-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="3a4d1-115">Ein **boolescher** Wert, die bei auf **True**festgelegt, die verhindert, dass den Fehler in einem Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3a4d1-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

