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
# <a name="internet-server-error-access-denied"></a>Internet Server Error: Access Denied


**Betrifft**: Access 2013 | Office 2013

Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:

HTTP\_STATUS\_verweigert 401

<<<<<<< HEAD stellen sicher, dass die Verzeichnisse von IIS zugegriffen erforderlichen Berechtigungen. RDS (Remote Data Service) kann mit einem IIS-Webserver kommunizieren, der in einem der drei Kennwortauthentifizierungsmodi ausgeführt wird: Anonym, Standard oder NT-Anfrage/Antwort (integrierte Windows-Authentifizierung in Windows 2000). Außerdem muss der Webserver Berechtigungen für den Datenquellencomputer haben, wenn es sich dabei um einen Computer mit Windows NT/Windows 2000 handelt.
=== Stellen Sie sicher, dass die Verzeichnisse von IIS zugegriffen erforderlichen Berechtigungen haben. RDS kann mit einem IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren: anonyme, Basic oder NT/Rückmeldung (integrierte Windows-Authentifizierung in Windows 2000 genannt). Außerdem muss der Webserver Berechtigungen auf dem Quellcomputer Daten verfügen, wenn es sich um eine Windows NT, Windows 2000-Computer handelt.
>>>>>>> master

