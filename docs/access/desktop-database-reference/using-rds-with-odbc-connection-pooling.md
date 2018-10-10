---
title: Verwenden von RDS mit ODBC-Verbindungspooling
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7baaf81d7a5d6a91416ea5baf8ba57745612740e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472997"
---
# <a name="using-rds-with-odbc-connection-pooling"></a>Verwenden von RDS mit ODBC-Verbindungspooling


**Betrifft**: Access 2013 | Office 2013

Wenn Sie eine ODBC-Datenquelle verwenden, können Sie die Verbindungs-Pool-Option in Internetinformationsdienste (IIS) dazu verwenden, eine sehr effiziente Verarbeitung von Clientlast zu erreichen. Verbindungs-Pool (Verbindungspooling) ist ein Ressourcen-Manager für Verbindungen, der häufig verwendete Verbindungen im geöffneten Status hält.

Informationen zum Aktivieren des Verbindungspoolings finden Sie in der Dokumentation zu Internetinformationsdienste.

Beachten Sie, dass der Webserver nach dem Aktivieren von Verbindungspooling möglicherweise anderen Einschränkungen unterliegt (siehe Dokumentation zu Microsoft Internetinformationsdienste).

Konfigurieren Sie Microsoft SQL Server für die Verwendung der TCP/IP-Sockets-Netzwerkbibliothek, um ein stabiles Verbindungspooling sicherzustellen, das eine höhere Effizienz bereitstellt.

Führen Sie dazu die folgenden Aktionen aus:

  - Konfigurieren Sie den Computer, auf dem SQL Server installiert ist, für die Verwendung von TCP/IP-Sockets.

  - Konfigurieren Sie den Webserver für die Verwendung von TCP/IP-Sockets.

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a>Konfigurieren des Computers mit SQL Server für die Verwendung von TCP/IP-Sockets

Führen Sie auf dem Computer mit SQL Server das Setup-Programm von SQL Server aus, sodass bei Interaktionen mit der Datenquelle die TCP/IP-Sockets-Netzwerkbibliothek verwendet wird.

**So geben Sie die TCP/IP-Sockets-Netzwerkbibliothek auf dem Computer mit SQL Server an**

**In Microsoft SQL Server 6.5:**

1.  Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 6.5**, und klicken Sie dann auf **SQL Setup**.

2.  Klicken Sie zweimal auf **Weiter**.

3.  Wählen Sie im Dialogfeld **Microsoft SQL Server 6.5 - Optionen** die Option **Netzwerkunterstützung ändern** aus, und klicken Sie dann auf **Weiter**.

4.  Stellen Sie sicher, dass das Kontrollkästchen **TCP/IP-Sockets** aktiviert ist, und klicken Sie auf **OK**.

5.  Klicken Sie auf **Weiter**, um den Vorgang abzuschließen, und beenden Sie Setup.

**In Microsoft SQL Server 7.0:**

1.  Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 7.0**, und klicken Sie dann auf **SQL Server-Netzwerkkonfiguration**.

2.  Klicken Sie auf der Registerkarte **Allgemein** des Dialogfelds auf **Hinzufügen**.

3.  Klicken Sie im Dialogfeld **Netzwerkbibliotheks-Konfiguration hinzufügen** auf **TCP/IP**.

4.  Geben Sie in die Felder **Anschlussnummer** und **Proxyadresse** die Anschlussnummer und Proxyadresse ein, die Sie von Ihrem Netzwerkadministrator erhalten haben.

5.  Klicken Sie auf **OK**, um den Vorgang abzuschließen, und beenden Sie Setup.

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>Konfigurieren des Webservers für die Verwendung von TCP/IP-Sockets

Sie haben zwei Möglichkeiten, den Webserver für die Verwendung von TCP/IP-Sockets zu konfigurieren. Welche Möglichkeit Sie wählen, hängt davon ab, ob über den Webserver auf alle Server mit SQL Server oder nur auf einen bestimmten Server zugegriffen wird.

Wenn auf alle Server, auf denen SQL Server installiert ist, über den Webserver zugegriffen wird, müssen Sie das SQL Server-Clientkonfigurationsprogramm auf dem Webservercomputer ausführen. Mit den folgenden Schritten wird die Standardnetzwerkbibliothek für alle über diesen IIS-Webserver vorgenommenen SQL Server-Verbindungen für die Verwendung der TCP/IP-Sockets-Netzwerkbibliothek geändert.

**So konfigurieren Sie den Webserver (alle Server mit SQL Server)**

**Für Microsoft SQL Server 6.5:**

1.  Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 6.5**, und klicken Sie dann auf **SQL Clientkonfigurationsprogramm**.

2.  Klicken Sie auf die Registerkarte **Netzwerkbibliothek**.

3.  Wählen Sie im Feld **Standardnetzwerk** die Option **TCP/IP-Sockets** aus.

4.  Klicken Sie auf **Fertig**, um die Änderungen zu speichern und das Hilfsprogramm zu beenden.

**Für Microsoft SQL Server 7.0:**

1.  Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 7.0**, und klicken Sie dann auf **Server-Clientkonfiguration**.

2.  Klicken Sie auf die Registerkarte **Allgemein**.

3.  Klicken Sie im Feld **Standard-Netzwerkbibliothek** auf **TCP/IP**.

4.  Klicken Sie auf **OK**, um die Änderungen zu speichern und das Hilfsprogramm zu beenden.

Wenn auf einen bestimmten Server mit SQL Server über einen Webserver zugegriffen wird, müssen Sie die SQL Server-Clientkonfiguration auf dem Webservercomputer ausführen. Konfigurieren Sie die SQL Server-Clientsoftware auf dem Webservercomputer wie im Folgenden beschrieben, um die Netzwerkbibliothek für eine bestimmte SQL Server-Verbindung zu ändern.

**So konfigurieren Sie den Webserver (ein bestimmter Server mit SQL Server)**

**Für Microsoft SQL Server 6.5:**

1.  Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 6.5**, und klicken Sie dann auf **SQL Clientkonfigurationsprogramm**.

2.  Klicken Sie auf die Registerkarte **Erweitert**.

3.  Geben Sie in das Feld **Server** den Namen des Servers ein, mit dem die Verbindung bei Verwendung von **TCP/IP-Sockets** hergestellt werden soll.

4.  Wählen Sie im Feld **DLL-Name** die Option **TCP/IP-Sockets** aus.

5.  Klicken Sie auf **Hinzufügen/Ändern**. Alle Datenquellen, die auf diesen Server verweisen, verwenden nun TCP/IP-Sockets.

6.  Klicken Sie auf **Fertig**.

**Für Microsoft SQL Server 7.0:**

1.  Zeigen Sie über **das Startmenü** auf **Programme**, zeigen Sie auf **Microsoft SQL Server 7.0**, und klicken Sie dann auf **Clientkonfigurationsprogramm**.

2.  Klicken Sie auf die Registerkarte **Allgemein**.

3.  Klicken Sie auf **Hinzufügen**.

4.  Geben Sie den Alias des Servers in das Feld **SQL Server-Alias** ein. Klicken Sie im Feld **Netzwerkbibliotheken** auf **TCP/IP**. Geben Sie in das Feld **Computername** den Namen des Computer ein, der TCP/IP-Sockets-Clients überwacht. Geben Sie in das Feld **Portnummer** den Port ein, auf dem der SQL Server lauscht.

5.  Klicken Sie auf **OK** und dann noch einmal auf **OK**, um das Hilfsprogramm zu schließen.

