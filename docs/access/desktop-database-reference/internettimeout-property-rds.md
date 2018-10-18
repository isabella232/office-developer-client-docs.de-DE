---
title: InternetTimeout-Eigenschaft (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd0fdc8f64207e1233ac56812ef009da865ce01a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603462"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="e5d05-102">InternetTimeout-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="e5d05-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="e5d05-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5d05-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e5d05-104">Gibt an, wie viele Millisekunden bis zum Erreichen des Timeouts einer Anforderung gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="e5d05-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

<span data-ttu-id="e5d05-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e5d05-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="e5d05-106">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e5d05-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="e5d05-107">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e5d05-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="e5d05-108">master</span><span class="sxs-lookup"><span data-stu-id="e5d05-108">master</span></span>

<span data-ttu-id="e5d05-109">Legt einen **Long** -Wert fest, der die Anzahl von Millisekunden vor dem Timeout der Anforderung darstellt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e5d05-109">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5d05-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e5d05-110">Remarks</span></span>

<span data-ttu-id="e5d05-111">Diese Eigenschaft gilt nur für Anforderungen, die mit den Protokollen HTTP oder HTTPS gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5d05-111">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="e5d05-p101">In einer dreistufigen Umgebung kann es mehrere Minuten dauern, bis eine Anforderung ausgeführt wird. Geben Sie mit dieser Eigenschaft zusätzliche Zeit für länger dauernde Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="e5d05-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

