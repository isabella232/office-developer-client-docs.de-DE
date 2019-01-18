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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710076"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="a1cb1-102">InternetTimeout-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="a1cb1-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="a1cb1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1cb1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1cb1-104">Gibt an, wie viele Millisekunden bis zum Erreichen des Timeouts einer Anforderung gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="a1cb1-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a1cb1-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a1cb1-105">Settings and return values</span></span>

<span data-ttu-id="a1cb1-106">Legt einen **Long** -Wert fest, der die Anzahl von Millisekunden vor dem Timeout der Anforderung darstellt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a1cb1-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1cb1-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1cb1-107">Remarks</span></span>

<span data-ttu-id="a1cb1-108">Diese Eigenschaft gilt nur für Anforderungen, die mit den Protokollen HTTP oder HTTPS gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1cb1-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="a1cb1-p101">In einer dreistufigen Umgebung kann es mehrere Minuten dauern, bis eine Anforderung ausgeführt wird. Geben Sie mit dieser Eigenschaft zusätzliche Zeit für länger dauernde Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="a1cb1-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

