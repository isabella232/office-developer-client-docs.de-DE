---
title: 'Internet Server Error: Access Denied'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c874b7a2c4facb9f5969bf9a2150c86773a2687a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603343"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="0645a-102">Internet Server Error: Access Denied</span><span class="sxs-lookup"><span data-stu-id="0645a-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="0645a-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0645a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0645a-104">Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:</span><span class="sxs-lookup"><span data-stu-id="0645a-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="0645a-105">HTTP\_STATUS\_verweigert 401</span><span class="sxs-lookup"><span data-stu-id="0645a-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="0645a-106"><<<<<<< HEAD stellen sicher, dass die Verzeichnisse von IIS zugegriffen erforderlichen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="0645a-106"><<<<<<< HEAD Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="0645a-107">RDS (Remote Data Service) kann mit einem IIS-Webserver kommunizieren, der in einem der drei Kennwortauthentifizierungsmodi ausgeführt wird: Anonym, Standard oder NT-Anfrage/Antwort (integrierte Windows-Authentifizierung in Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="0645a-107">RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="0645a-108">Außerdem muss der Webserver Berechtigungen für den Datenquellencomputer haben, wenn es sich dabei um einen Computer mit Windows NT/Windows 2000 handelt.</span><span class="sxs-lookup"><span data-stu-id="0645a-108">Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>
<span data-ttu-id="0645a-109">=== Stellen Sie sicher, dass die Verzeichnisse von IIS zugegriffen erforderlichen Berechtigungen haben.</span><span class="sxs-lookup"><span data-stu-id="0645a-109">======= Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="0645a-110">RDS kann mit einem IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren: anonyme, Basic oder NT/Rückmeldung (integrierte Windows-Authentifizierung in Windows 2000 genannt).</span><span class="sxs-lookup"><span data-stu-id="0645a-110">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="0645a-111">Außerdem muss der Webserver Berechtigungen auf dem Quellcomputer Daten verfügen, wenn es sich um eine Windows NT, Windows 2000-Computer handelt.</span><span class="sxs-lookup"><span data-stu-id="0645a-111">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>
>>>>>>> <span data-ttu-id="0645a-112">master</span><span class="sxs-lookup"><span data-stu-id="0645a-112">master</span></span>

