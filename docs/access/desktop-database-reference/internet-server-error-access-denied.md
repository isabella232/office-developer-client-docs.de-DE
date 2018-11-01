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
# <a name="internet-server-error-access-denied"></a>Internet Server Error: Access Denied


**Betrifft**: Access 2013, Office 2013

Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:

HTTP\_STATUS\_verweigert 401

Stellen Sie sicher, dass die Verzeichnisse, auf die IIS zugreift, auf die richtigen Berechtigungen eingestellt sind. RDS kann mit einem IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren: anonyme, Basic oder NT/Rückmeldung (integrierte Windows-Authentifizierung in Windows 2000 genannt). Außerdem muss der Webserver Berechtigungen auf dem Quellcomputer Daten verfügen, wenn es sich um eine Windows NT, Windows 2000-Computer handelt.

