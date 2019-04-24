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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291255"
---
# <a name="internet-server-error-access-denied"></a>Internetserverfehler: Zugriff verweigert


**Gilt für**: Access 2013, Office 2013

Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:

HTTP\_-\_Status verweigert 401

Stellen Sie sicher, dass die Verzeichnisse, auf die IIS zugreift, auf die richtigen Berechtigungen eingestellt sind. RDS kann mit einem IIS-Webserver kommunizieren, der in einem der drei Kenn Wort Authentifizierungsmodi ausgeführt wird: Anonymous, Basic oder NT Challenge/Response (als integrierte Windows-Authentifizierung in Windows 2000 bezeichnet). Außerdem muss der Webserver über Berechtigungen für den Datenquellencomputer verfügen, wenn es sich um einen Windows NT/Windows 2000-Computer handelt.

