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
# <a name="internet-server-error-access-denied"></a>Internetserverfehler: Zugriff verweigert


**Betrifft**: Access 2013, Office 2013

Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:

HTTP\_STATUS\_verweigert 401

Stellen Sie sicher, dass die Verzeichnisse, auf die IIS zugreift, auf die richtigen Berechtigungen eingestellt sind. RDS kann mit einem IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren: anonyme, Basic oder NT/Rückmeldung (integrierte Windows-Authentifizierung in Windows 2000 genannt). Außerdem muss der Webserver Berechtigungen auf dem Quellcomputer Daten verfügen, wenn es sich um eine Windows NT, Windows 2000-Computer handelt.

