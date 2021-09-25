---
title: 'Internetserverfehler: Zugriff verweigert'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c0b10a07370d2c963328114543b598aa9af9ac26
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594069"
---
# <a name="internet-server-error-access-denied"></a>Internetserverfehler: Zugriff verweigert


**Gilt für**: Access 2013, Office 2013

Wenn diese Fehlermeldung angezeigt wird, bedeutet dies normalerweise, dass Microsoft Internetinformationsdienste (Internet Information Services, IIS) den folgenden Status zurückgegeben hat:

\_HTTP-STATUS \_ VERWEIGERT 401

Stellen Sie sicher, dass die Verzeichnisse, auf die IIS zugreift, auf die richtigen Berechtigungen eingestellt sind. RDS kann mit einem IIS-Webserver kommunizieren, der in einem der drei Modi für die Kennwortauthentifizierung ausgeführt wird: Anonym, Standard oder NT Challenge/Response (integrierte Windows-Authentifizierung in Windows 2000). Außerdem muss der Webserver über Berechtigungen für den Datenquellencomputer verfügen, wenn es sich um einen Windows NT/Windows 2000-Computer handelt.

