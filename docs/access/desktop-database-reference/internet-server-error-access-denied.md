---
title: 'Internet Server Error: Access Denied'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db78b6f2c51e2e5df918622043e33abc6bc9e674
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473890"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="455f1-102">Internet Server Error: Access Denied</span><span class="sxs-lookup"><span data-stu-id="455f1-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="455f1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="455f1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="455f1-104">Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:</span><span class="sxs-lookup"><span data-stu-id="455f1-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="455f1-105">HTTP\_STATUS\_verweigert 401</span><span class="sxs-lookup"><span data-stu-id="455f1-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="455f1-p101">Stellen Sie sicher, dass die Verzeichnisse, auf die IIS zugreift, auf die richtigen Berechtigungen eingestellt sind. RDS (Remote Data Service) kann mit einem IIS-Webserver kommunizieren, der in einem der drei Kennwortauthentifizierungsmodi ausgeführt wird: Anonym, Standard oder NT-Anfrage/Antwort (integrierte Windows-Authentifizierung in Windows 2000). Außerdem muss der Webserver Berechtigungen für den Datenquellencomputer haben, wenn es sich dabei um einen Computer mit Windows NT/Windows 2000 handelt.</span><span class="sxs-lookup"><span data-stu-id="455f1-p101">Make sure the directories accessed by IIS have proper permissions. RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000). Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

