---
title: Konfigurieren von RDS unter Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c69cdbaf30a2c592790942a04c777b11512631f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565772"
---
# <a name="configuring-rds-on-windows-2000"></a>Konfigurieren von RDS unter Windows 2000


**Gilt für**: Access 2013, Office 2013

Wenn es sich für Sie schwierig erweist, die Funktionsfähigkeit von RDS (Remote Data Service) nach eine Update auf Windows 2000 herzustellen, befolgen Sie die unten aufgeführten Schritte, um das Problem zu behandeln.

1.  Stellen Sie sicher, dass der Www-Veröffentlichungsdienst zuerst ausgeführt wird, indem Sie mit Internet Explorer zu https://*Server* navigieren. If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".

2.  From the Start menu, select Run. Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad. Überprüfen Sie den \[ Abschnitt CONNECT \] DEFAULT, und wenn der ACCESS-Parameter auf NOACCESS festgelegt ist, ändern Sie ihn in READONLY.

3.  Navigieren Sie mithilfe des Hilfsprogramms RegEdit zu "HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ DataFactory \\ HandlerInfo", und stellen Sie sicher, dass **HandlerRequired** auf 0 und **DefaultHandler** auf "" (Null-Zeichenfolge) festgelegt ist.
    
    > [!NOTE]
    > Wenn Sie diesen Abschnitt der Registrierung ändern, müssen Sie den WWW-Publishingdienst beenden und neu starten, indem Sie die folgenden Befehle an der Eingabeaufforderung eingeben: NET STOP W3SVC und NET START W3SVC.

4.  Navigieren Sie mithilfe des Hilfsprogramms RegEdit in der Registrierung zu "HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ Services \\ W3SVC \\ Parameters \\ ADCLaunch", und stellen Sie sicher, dass ein Schlüssel namens **RDSServer.Datafactory** vorhanden ist. If not, create it.

5.  Wechseln Sie mithilfe von Internet Services Manager zur Standardwebsite, und zeigen Sie die Eigenschaften des virtuellen Stamms MSADC an. Überprüfen Sie die Einschränkungen für Verzeichnissicherheit, IP-Adressen und Domänennamen. Wenn Zugriff verweigert aktiviert ist, aktivieren Gewährt.

Sie sollten den Server neu starten, wenn es zunächst den Anschein hat, dass das Problem durch die Änderungen nicht gelöst wurde.

