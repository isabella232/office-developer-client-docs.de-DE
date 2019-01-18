---
title: 'Internetserverfehler: Zugriff verweigert'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: af823f46653b3ec83950c2e2cfe639b514196b08
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720387"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="33e9d-102">Internetserverfehler: Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="33e9d-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="33e9d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33e9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33e9d-104">Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:</span><span class="sxs-lookup"><span data-stu-id="33e9d-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="33e9d-105">HTTP\_STATUS\_verweigert 401</span><span class="sxs-lookup"><span data-stu-id="33e9d-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="33e9d-106">Stellen Sie sicher, dass die Verzeichnisse, auf die IIS zugreift, auf die richtigen Berechtigungen eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="33e9d-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="33e9d-107">RDS kann mit einem IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren: anonyme, Basic oder NT/Rückmeldung (integrierte Windows-Authentifizierung in Windows 2000 genannt).</span><span class="sxs-lookup"><span data-stu-id="33e9d-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="33e9d-108">Außerdem muss der Webserver Berechtigungen auf dem Quellcomputer Daten verfügen, wenn es sich um eine Windows NT, Windows 2000-Computer handelt.</span><span class="sxs-lookup"><span data-stu-id="33e9d-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

