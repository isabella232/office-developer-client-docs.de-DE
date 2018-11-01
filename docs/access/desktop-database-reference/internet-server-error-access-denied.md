---
title: 'Internet Server Error: Access Denied'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 132ecc75c01cdc54eb2d7664227b7abb1578cc2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876540"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="9f0af-102">Internet Server Error: Access Denied</span><span class="sxs-lookup"><span data-stu-id="9f0af-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="9f0af-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f0af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f0af-104">Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:</span><span class="sxs-lookup"><span data-stu-id="9f0af-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="9f0af-105">HTTP\_STATUS\_verweigert 401</span><span class="sxs-lookup"><span data-stu-id="9f0af-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="9f0af-106">Stellen Sie sicher, dass die Verzeichnisse, auf die IIS zugreift, auf die richtigen Berechtigungen eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="9f0af-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="9f0af-107">RDS kann mit einem IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren: anonyme, Basic oder NT/Rückmeldung (integrierte Windows-Authentifizierung in Windows 2000 genannt).</span><span class="sxs-lookup"><span data-stu-id="9f0af-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="9f0af-108">Außerdem muss der Webserver Berechtigungen auf dem Quellcomputer Daten verfügen, wenn es sich um eine Windows NT, Windows 2000-Computer handelt.</span><span class="sxs-lookup"><span data-stu-id="9f0af-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

