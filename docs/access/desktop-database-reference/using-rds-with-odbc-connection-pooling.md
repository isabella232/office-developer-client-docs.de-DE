---
title: Verwenden von RDS mit ODBC-Verbindungspooling
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87d380fdc52cdee2aa834fd6e78ff1b761a0e93a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312117"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="8c4e2-102">Verwenden von RDS mit ODBC-Verbindungs-Pooling</span><span class="sxs-lookup"><span data-stu-id="8c4e2-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="8c4e2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c4e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c4e2-p101">Wenn Sie eine ODBC-Datenquelle verwenden, können Sie die Verbindungs-Pool-Option in Internetinformationsdienste (IIS) dazu verwenden, eine sehr effiziente Verarbeitung von Clientlast zu erreichen. Verbindungs-Pool (Verbindungspooling) ist ein Ressourcen-Manager für Verbindungen, der häufig verwendete Verbindungen im geöffneten Status hält.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="8c4e2-106">Informationen zum Aktivieren des Verbindungspoolings finden Sie in der Dokumentation zu Internetinformationsdienste.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="8c4e2-107">Beachten Sie, dass das Aktivieren des Verbindungspools den Webserver anderen Einschränkungen unterwerfen kann, wie in der Microsoft Internet Information Services-Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="8c4e2-108">Konfigurieren Sie Microsoft SQL Server für die Verwendung der TCP/IP-Sockets-Netzwerkbibliothek, um ein stabiles Verbindungspooling sicherzustellen, das eine höhere Effizienz bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="8c4e2-109">Führen Sie dazu die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="8c4e2-109">To do this, you need to:</span></span>

  - <span data-ttu-id="8c4e2-110">Konfigurieren Sie den Computer, auf dem SQL Server installiert ist, für die Verwendung von TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="8c4e2-111">Konfigurieren Sie den Webserver für die Verwendung von TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="8c4e2-112">Konfigurieren des Computers mit SQL Server für die Verwendung von TCP/IP-Sockets</span><span class="sxs-lookup"><span data-stu-id="8c4e2-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="8c4e2-113">Führen Sie auf dem Computer mit SQL Server das Setup-Programm von SQL Server aus, sodass bei Interaktionen mit der Datenquelle die TCP/IP-Sockets-Netzwerkbibliothek verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="8c4e2-114">**So geben Sie die TCP/IP-Sockets-Netzwerkbibliothek auf dem Computer mit SQL Server an**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="8c4e2-115">**In Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="8c4e2-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="8c4e2-117">Klicken Sie zweimal auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="8c4e2-118">Wählen Sie im Dialogfeld **Microsoft SQL Server 6.5 - Optionen** die Option **Netzwerkunterstützung ändern** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="8c4e2-119">Stellen Sie sicher, dass das Kontrollkästchen **TCP/IP-Sockets** aktiviert ist, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="8c4e2-120">Klicken Sie auf **Weiter**, um den Vorgang abzuschließen, und beenden Sie Setup.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="8c4e2-121">**In Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="8c4e2-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="8c4e2-123">Klicken Sie auf der Registerkarte **Allgemein** des Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="8c4e2-124">Klicken Sie im Dialogfeld **Netzwerkbibliotheks-Konfiguration hinzufügen** auf **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="8c4e2-125">Geben Sie in die Felder **Anschlussnummer** und **Proxyadresse** die Anschlussnummer und Proxyadresse ein, die Sie von Ihrem Netzwerkadministrator erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="8c4e2-126">Klicken Sie auf **OK**, um den Vorgang abzuschließen, und beenden Sie Setup.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="8c4e2-127">Konfigurieren des webServers für die Verwendung von TCP/IP-Sockets</span><span class="sxs-lookup"><span data-stu-id="8c4e2-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="8c4e2-128">Es gibt zwei Optionen zum Konfigurieren des Webservers für die Verwendung von TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="8c4e2-129">Was Sie tun, hängt davon ab, ob auf alle SQL-Server vom Webserver zugegriffen wird, oder auf einen bestimmten SQL Server wird vom Webserver zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="8c4e2-130">Wenn auf alle SQL-Server über den Webserver zugegriffen wird, müssen Sie das SQL Server-Client Konfigurationsprogramm auf dem Webservercomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="8c4e2-131">Die folgenden Schritte ändern die standardmäßige Netzwerkbibliothek für alle SQL Server-Verbindungen, die von diesem IIS-Webserver ausgeführt werden, um die TCP/IP-Sockets-Netzwerkbibliothek zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="8c4e2-132">**So konfigurieren Sie den Webserver (alle SQL-Server)**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="8c4e2-133">**Für Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="8c4e2-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="8c4e2-135">Klicken Sie auf die Registerkarte **Netzwerkbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="8c4e2-136">Wählen Sie im Feld **Standardnetzwerk** die Option **TCP/IP-Sockets** aus.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="8c4e2-137">Klicken Sie auf **Fertig**, um die Änderungen zu speichern und das Hilfsprogramm zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="8c4e2-138">**Für Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="8c4e2-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="8c4e2-140">Klicken Sie auf die Registerkarte **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="8c4e2-141">Klicken Sie im Feld **Standard-Netzwerkbibliothek** auf **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="8c4e2-142">Klicken Sie auf **OK**, um die Änderungen zu speichern und das Hilfsprogramm zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="8c4e2-143">Wenn auf einen bestimmten SQL Server von einem Webserver zugegriffen wird, müssen Sie das SQL Server-Client Konfigurationsprogramm auf dem Webservercomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="8c4e2-144">Konfigurieren Sie die SQL Server-Client Software auf dem Webservercomputer wie folgt, um die Netzwerkbibliothek für eine bestimmte SQL Server-Verbindung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="8c4e2-145">**So konfigurieren Sie den Webserver (ein bestimmter SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="8c4e2-146">**Für Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="8c4e2-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="8c4e2-148">Klicken Sie auf die Registerkarte **Erweitert**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="8c4e2-149">Geben Sie in das Feld **Server** den Namen des Servers ein, mit dem die Verbindung bei Verwendung von **TCP/IP-Sockets** hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="8c4e2-150">Wählen Sie im Feld **DLL-Name** die Option **TCP/IP-Sockets** aus.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="8c4e2-p105">Klicken Sie auf **Hinzufügen/Ändern**. Alle Datenquellen, die auf diesen Server verweisen, verwenden nun TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="8c4e2-153">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-153">Click **Done**.</span></span>

<span data-ttu-id="8c4e2-154">**Für Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="8c4e2-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="8c4e2-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="8c4e2-156">Klicken Sie auf die Registerkarte **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="8c4e2-157">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-157">Click **Add**.</span></span>

4.  <span data-ttu-id="8c4e2-p106">Geben Sie den Alias des Servers in das Feld **SQL Server-Alias** ein. Klicken Sie im Feld **Netzwerkbibliotheken** auf **TCP/IP**. Geben Sie in das Feld **Computername** den Namen des Computer ein, der TCP/IP-Sockets-Clients überwacht. Geben Sie in das Feld **Portnummer** den Port ein, auf dem der SQL Server lauscht.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="8c4e2-162">Klicken Sie auf **OK** und dann noch einmal auf **OK**, um das Hilfsprogramm zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8c4e2-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

