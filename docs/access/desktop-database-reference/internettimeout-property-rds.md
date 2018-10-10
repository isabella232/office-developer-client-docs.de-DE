---
title: InternetTimeout-Eigenschaft (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929b166a308276836fbe4a48a2461ef7eb0caba2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472664"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="64650-102">InternetTimeout-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="64650-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="64650-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="64650-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="64650-104">Gibt an, wie viele Millisekunden bis zum Erreichen des Timeouts einer Anforderung gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="64650-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="64650-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="64650-105">Settings and Return Values</span></span>

<span data-ttu-id="64650-106">Legt einen **Long** -Wert fest, der die Anzahl von Millisekunden vor dem Timeout der Anforderung darstellt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="64650-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="64650-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64650-107">Remarks</span></span>

<span data-ttu-id="64650-108">Diese Eigenschaft gilt nur für Anforderungen, die mit den Protokollen HTTP oder HTTPS gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="64650-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="64650-p101">In einer dreistufigen Umgebung kann es mehrere Minuten dauern, bis eine Anforderung ausgeführt wird. Geben Sie mit dieser Eigenschaft zusätzliche Zeit für länger dauernde Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="64650-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

