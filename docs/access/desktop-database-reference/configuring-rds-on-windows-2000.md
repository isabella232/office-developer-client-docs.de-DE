---
title: Konfigurieren von RDS unter Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8482df5ca2fab110e5b1a77fe227c5f0c583d893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296017"
---
# <a name="configuring-rds-on-windows-2000"></a>Konfigurieren von RDS unter Windows 2000


**Gilt für**: Access 2013, Office 2013

Wenn es sich für Sie schwierig erweist, die Funktionsfähigkeit von RDS (Remote Data Service) nach eine Update auf Windows 2000 herzustellen, befolgen Sie die unten aufgeführten Schritte, um das Problem zu behandeln.

1.  Stellen Sie sicher, dass der www-VeröffentlichungsDienst zuerst durch Navigieren zum https://-*Server* mit Internet Explorer gestartet wird. If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".

2.  From the Start menu, select Run. Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad. Überprüfen \[Sie den\] Abschnitt Connect Default, und wenn der Parameter Access auf NoAccess festgelegt ist, ändern Sie ihn in ReadOnly.

3.  Navigieren Sie mit dem Dienstprogramm RegEdit zu "\_HKEY\_-\\lokale\\Computer\\Software Microsoft\\DataFactory HandlerInfo", und stellen Sie sicher, dass **HandlerRequired** auf 0 und **DefaultHandler** ist "" (null Zeichenfolge).
    
    > [!NOTE]
    > Wenn Sie diesen Abschnitt der Registrierung ändern, müssen Sie den WWW-Publishingdienst beenden und neu starten, indem Sie die folgenden Befehle an der Eingabeaufforderung eingeben: NET STOP W3SVC und NET START W3SVC.

4.  Navigieren Sie mit dem Dienstprogramm RegEdit in der Registrierung zu "\_HKEY\_local\\Machine\\System\\CurrentControlSet\\Services\\W3SVC\\Parameters ADCLaunch", und überprüfen Sie, ob ein Schlüssel namens ** RDSServer. DataFactory**. If not, create it.

5.  Wechseln Sie mit dem Internet Dienste-Manager zur Standardwebsite, und zeigen Sie die Eigenschaften des virtuellen MSADC-Stammverzeichnisses an. Überprüfen Sie die Einschränkungen für Verzeichnissicherheit, IP-Adressen und Domänennamen. Wenn Zugriff verweigert aktiviert ist, aktivieren Gewährt.

Sie sollten den Server neu starten, wenn es zunächst den Anschein hat, dass das Problem durch die Änderungen nicht gelöst wurde.

