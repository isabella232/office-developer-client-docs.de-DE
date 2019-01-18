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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720954"
---
# <a name="configuring-rds-on-windows-2000"></a>Konfigurieren von RDS unter Windows 2000


**Betrifft**: Access 2013, Office 2013

Wenn es sich für Sie schwierig erweist, die Funktionsfähigkeit von RDS (Remote Data Service) nach eine Update auf Windows 2000 herzustellen, befolgen Sie die unten aufgeführten Schritte, um das Problem zu behandeln.

1.  Stellen Sie sicher, dass der WWW-Publishingdienst ersten ausgeführt wird, navigieren Sie zur https://*Server* mithilfe von Internet Explorer. Wenn Sie nicht auf den Webserver auf diese Weise zugreifen können, rufen Sie ein Eingabeaufforderungsfenster, und geben Sie den folgenden Befehl, "NET START W3SVC".

2.  Wählen Sie im Startmenü ausführen aus. Geben Sie msdfmap.ini, und klicken Sie auf OK, um die Datei "Msdfmap.ini" im Editor zu öffnen. Überprüfen Sie die \[CONNECT DEFAULT\] Abschnitt, und wenn der Parameter Zugriff auf NOACCESS festgelegt ist, ändern Sie ihn auf READONLY.

3.  Navigieren Sie mithilfe des Dienstprogramms RegEdit zu "HKEY\_lokale\_Computer\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo", und stellen Sie sicher, dass **DefaultHandler** auf 0 festgelegt ist und **HandlerRequired** "" (Null String).
    
    > [!NOTE]
    > Wenn Sie diesen Abschnitt der Registrierung ändern, müssen Sie den WWW-Publishingdienst beenden und neu starten, indem Sie die folgenden Befehle an der Eingabeaufforderung eingeben: NET STOP W3SVC und NET START W3SVC.

4.  Navigieren Sie mithilfe des Dienstprogramms RegEdit in der Registrierung auf "HKEY\_lokale\_Computer\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameter\\ADCLaunch" und stellen Sie sicher, dass eine wichtige gewählte **vorhanden ist RDSServer.Datafactory**. Wenn dies nicht der Fall ist, erstellen Sie ihn.

5.  Internetdienste-Manager verwenden, wechseln Sie zu der Standardwebsite, und zeigen Sie die Eigenschaften des virtuellen Stammverzeichnisses MSADC. Untersuchen Sie die Directory Security-IP-Adresse und der Domäne Name Einschränkungen. Wenn die "Zugriff verweigert" überprüft wird wählen Sie dann "Gewährt" aus.

Sie sollten den Server neu starten, wenn es zunächst den Anschein hat, dass das Problem durch die Änderungen nicht gelöst wurde.

