---
title: InternetTimeout-Eigenschaft (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291241"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="db7cf-102">InternetTimeout-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="db7cf-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="db7cf-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db7cf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db7cf-104">Gibt an, wie viele Millisekunden bis zum Erreichen des Timeouts einer Anforderung gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="db7cf-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="db7cf-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="db7cf-105">Settings and return values</span></span>

<span data-ttu-id="db7cf-106">Legt einen **Long**-Wert fest, der die Anzahl von Millisekunden vor dem Timeout der Anforderung darstellt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="db7cf-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7cf-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db7cf-107">Remarks</span></span>

<span data-ttu-id="db7cf-108">Diese Eigenschaft gilt nur für Anforderungen, die mit den Protokollen HTTP oder HTTPS gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="db7cf-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="db7cf-p101">In einer dreistufigen Umgebung kann es mehrere Minuten dauern, bis eine Anforderung ausgeführt wird. Geben Sie mit dieser Eigenschaft zusätzliche Zeit für länger dauernde Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="db7cf-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

