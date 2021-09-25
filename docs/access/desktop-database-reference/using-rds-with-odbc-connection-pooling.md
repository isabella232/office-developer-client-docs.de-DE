---
title: Verwenden von RDS mit ODBC-Verbindungspooling
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 95111c2698fd6a2efd85a889fcc2a3b40691e68f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572662"
---
# <a name="using-rds-with-odbc-connection-pooling"></a>Verwenden von RDS mit ODBC-Verbindungs-Pooling


**Gilt für**: Access 2013, Office 2013

Wenn Sie eine ODBC-Datenquelle verwenden, können Sie die Verbindungs-Pool-Option in Internetinformationsdienste (IIS) dazu verwenden, eine sehr effiziente Verarbeitung von Clientlast zu erreichen. Verbindungs-Pool (Verbindungspooling) ist ein Ressourcen-Manager für Verbindungen, der häufig verwendete Verbindungen im geöffneten Status hält.

Informationen zum Aktivieren des Verbindungspoolings finden Sie in der Dokumentation zu Internetinformationsdienste.

Bitte beachten Sie, dass die Aktivierung des Verbindungspoolings dem Webserver möglicherweise andere Einschränkungen unterliegt, wie in der dokumentation Microsoft-Internetinformationsdienste angegeben.

Konfigurieren Sie Microsoft SQL Server für die Verwendung der TCP/IP-Sockets-Netzwerkbibliothek, um ein stabiles Verbindungspooling sicherzustellen, das eine höhere Effizienz bereitstellt.

Führen Sie dazu die folgenden Aktionen aus:

  - Konfigurieren Sie den Computer, auf dem SQL Server installiert ist, für die Verwendung von TCP/IP-Sockets.

  - Konfigurieren Sie den Webserver für die Verwendung von TCP/IP-Sockets.

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a>Konfigurieren des Computers mit SQL Server für die Verwendung von TCP/IP-Sockets

Führen Sie auf dem Computer mit SQL Server das Setup-Programm von SQL Server aus, sodass bei Interaktionen mit der Datenquelle die TCP/IP-Sockets-Netzwerkbibliothek verwendet wird.

**So geben Sie die TCP/IP-Sockets-Netzwerkbibliothek auf dem Computer mit SQL Server an**

**In Microsoft SQL Server 6.5:**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.

2.  Klicken Sie zweimal auf **Weiter**.

3.  Wählen Sie im Dialogfeld **Microsoft SQL Server 6.5 - Optionen** die Option **Netzwerkunterstützung ändern** aus, und klicken Sie dann auf **Weiter**.

4.  Stellen Sie sicher, dass das Kontrollkästchen **TCP/IP-Sockets** aktiviert ist, und klicken Sie auf **OK**.

5.  Klicken Sie auf **Weiter**, um den Vorgang abzuschließen, und beenden Sie Setup.

**In Microsoft SQL Server 7.0:**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.

2.  Klicken Sie auf der Registerkarte **Allgemein** des Dialogfelds auf **Hinzufügen**.

3.  Klicken Sie im Dialogfeld **Netzwerkbibliotheks-Konfiguration hinzufügen** auf **TCP/IP**.

4.  Geben Sie in die Felder **Anschlussnummer** und **Proxyadresse** die Anschlussnummer und Proxyadresse ein, die Sie von Ihrem Netzwerkadministrator erhalten haben.

5.  Klicken Sie auf **OK**, um den Vorgang abzuschließen, und beenden Sie Setup.

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>Konfigurieren des Webservers für die Verwendung von TCP/IP-Sockets

Es gibt zwei Optionen zum Konfigurieren des Webservers für die Verwendung von TCP/IP-Sockets. Was Sie tun, hängt davon ab, ob auf alle SQL Server über den Webserver zugegriffen wird oder nur auf eine bestimmte SQL Server über den Webserver zugegriffen wird.

Wenn auf alle SQL Server über den Webserver zugegriffen wird, müssen Sie das SQL Server Clientkonfigurationsprogramm auf dem Webservercomputer ausführen. Mit den folgenden Schritten wird die Standardnetzwerkbibliothek für alle SQL Server Verbindungen, die von diesem IIS-Webserver hergestellt werden, so geändert, dass die TCP/IP-Sockets-Netzwerkbibliothek verwendet wird.

**So konfigurieren Sie den Webserver (alle SQL Server)**

**Für Microsoft SQL Server 6.5:**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.

2.  Klicken Sie auf die Registerkarte **Netzwerkbibliothek**.

3.  Wählen Sie im Feld **Standardnetzwerk** die Option **TCP/IP-Sockets** aus.

4.  Klicken Sie auf **Fertig**, um die Änderungen zu speichern und das Hilfsprogramm zu beenden.

**Für Microsoft SQL Server 7.0:**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.

2.  Klicken Sie auf die Registerkarte **Allgemein**.

3.  Klicken Sie im Feld **Standard-Netzwerkbibliothek** auf **TCP/IP**.

4.  Klicken Sie auf **OK**, um die Änderungen zu speichern und das Hilfsprogramm zu beenden.

Wenn von einem Webserver aus auf eine bestimmte SQL Server zugegriffen wird, müssen Sie das SQL Server Clientkonfigurationsprogramm auf dem Webservercomputer ausführen. Um die Netzwerkbibliothek für eine bestimmte SQL Server Verbindung zu ändern, konfigurieren Sie die SQL Server Clientsoftware auf dem Webservercomputer wie folgt.

**So konfigurieren Sie den Webserver (eine bestimmte SQL Server)**

**Für Microsoft SQL Server 6.5:**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.

2.  Klicken Sie auf die Registerkarte **Erweitert**.

3.  Geben Sie in das Feld **Server** den Namen des Servers ein, mit dem die Verbindung bei Verwendung von **TCP/IP-Sockets** hergestellt werden soll.

4.  Wählen Sie im Feld **DLL-Name** die Option **TCP/IP-Sockets** aus.

5.  Klicken Sie auf **Hinzufügen/Ändern**. Alle Datenquellen, die auf diesen Server verweisen, verwenden nun TCP/IP-Sockets.

6.  Klicken Sie auf **Fertig**.

**Für Microsoft SQL Server 7.0:**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.

2.  Klicken Sie auf die Registerkarte **Allgemein**.

3.  Klicken Sie auf **Hinzufügen**.

4.  Geben Sie den Alias des Servers in das Feld **SQL Server-Alias** ein. Klicken Sie im Feld **Netzwerkbibliotheken** auf **TCP/IP**. Geben Sie in das Feld **Computername** den Namen des Computer ein, der TCP/IP-Sockets-Clients überwacht. Geben Sie in das Feld **Portnummer** den Port ein, auf dem der SQL Server lauscht.

5.  Klicken Sie auf **OK** und dann noch einmal auf **OK**, um das Hilfsprogramm zu schließen.

