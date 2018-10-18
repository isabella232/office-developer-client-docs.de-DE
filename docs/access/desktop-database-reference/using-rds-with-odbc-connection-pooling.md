---
title: Verwenden von RDS mit ODBC-Verbindungspooling
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee66e68cb8eeaaca57c007dc64a9e2b3a8476ec7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606017"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="26e5d-102">Verwenden von RDS mit ODBC-Verbindungspooling</span><span class="sxs-lookup"><span data-stu-id="26e5d-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="26e5d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="26e5d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="26e5d-p101">Wenn Sie eine ODBC-Datenquelle verwenden, können Sie die Verbindungs-Pool-Option in Internetinformationsdienste (IIS) dazu verwenden, eine sehr effiziente Verarbeitung von Clientlast zu erreichen. Verbindungs-Pool (Verbindungspooling) ist ein Ressourcen-Manager für Verbindungen, der häufig verwendete Verbindungen im geöffneten Status hält.</span><span class="sxs-lookup"><span data-stu-id="26e5d-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="26e5d-106">Informationen zum Aktivieren des Verbindungspoolings finden Sie in der Dokumentation zu Internetinformationsdienste.</span><span class="sxs-lookup"><span data-stu-id="26e5d-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="26e5d-107"><<<<<<< HEAD Bitte beachten Sie, dass Aktivieren von Verbindungspooling den Webserver anderen Einschränkungen Subject-möglicherweise wie bereits erwähnt in der Dokumentation zu Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="26e5d-107"><<<<<<< HEAD Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
<span data-ttu-id="26e5d-108">=== Bitte beachten Sie, dass Aktivieren von Verbindungspooling den Webserver anderen Einschränkungen Subject-möglicherweise wie bereits erwähnt in der Dokumentation zu Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="26e5d-108">======= Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
>>>>>>> <span data-ttu-id="26e5d-109">master</span><span class="sxs-lookup"><span data-stu-id="26e5d-109">master</span></span>

<span data-ttu-id="26e5d-110">Konfigurieren Sie Microsoft SQL Server für die Verwendung der TCP/IP-Sockets-Netzwerkbibliothek, um ein stabiles Verbindungspooling sicherzustellen, das eine höhere Effizienz bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="26e5d-110">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="26e5d-111">Führen Sie dazu die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="26e5d-111">To do this, you need to:</span></span>

  - <span data-ttu-id="26e5d-112">Konfigurieren Sie den Computer, auf dem SQL Server installiert ist, für die Verwendung von TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="26e5d-112">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

<span data-ttu-id="26e5d-113"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="26e5d-113"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="26e5d-114">Konfigurieren Sie den Webserver für die Verwendung von TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="26e5d-114">Configure the Web server to use TCP/IP Sockets.</span></span>
=======
  - <span data-ttu-id="26e5d-115">Konfigurieren des Webservers zur Verwendung von TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="26e5d-115">Configure the web server to use TCP/IP Sockets.</span></span>
>>>>>>> <span data-ttu-id="26e5d-116">master</span><span class="sxs-lookup"><span data-stu-id="26e5d-116">master</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="26e5d-117">Konfigurieren des Computers mit SQL Server für die Verwendung von TCP/IP-Sockets</span><span class="sxs-lookup"><span data-stu-id="26e5d-117">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="26e5d-118">Führen Sie auf dem Computer mit SQL Server das Setup-Programm von SQL Server aus, sodass bei Interaktionen mit der Datenquelle die TCP/IP-Sockets-Netzwerkbibliothek verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26e5d-118">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="26e5d-119">**So geben Sie die TCP/IP-Sockets-Netzwerkbibliothek auf dem Computer mit SQL Server an**</span><span class="sxs-lookup"><span data-stu-id="26e5d-119">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="26e5d-120">**In Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="26e5d-120">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="26e5d-121">Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 6.5**, und klicken Sie dann auf **SQL Setup**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-121">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="26e5d-122">Klicken Sie zweimal auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-122">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="26e5d-123">Wählen Sie im Dialogfeld **Microsoft SQL Server 6.5 - Optionen** die Option **Netzwerkunterstützung ändern** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-123">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="26e5d-124">Stellen Sie sicher, dass das Kontrollkästchen **TCP/IP-Sockets** aktiviert ist, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-124">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="26e5d-125">Klicken Sie auf **Weiter**, um den Vorgang abzuschließen, und beenden Sie Setup.</span><span class="sxs-lookup"><span data-stu-id="26e5d-125">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="26e5d-126">**In Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="26e5d-126">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="26e5d-127">Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 7.0**, und klicken Sie dann auf **SQL Server-Netzwerkkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-127">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="26e5d-128">Klicken Sie auf der Registerkarte **Allgemein** des Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-128">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="26e5d-129">Klicken Sie im Dialogfeld **Netzwerkbibliotheks-Konfiguration hinzufügen** auf **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-129">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="26e5d-130">Geben Sie in die Felder **Anschlussnummer** und **Proxyadresse** die Anschlussnummer und Proxyadresse ein, die Sie von Ihrem Netzwerkadministrator erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="26e5d-130">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="26e5d-131">Klicken Sie auf **OK**, um den Vorgang abzuschließen, und beenden Sie Setup.</span><span class="sxs-lookup"><span data-stu-id="26e5d-131">Click **OK** to finish, and exit setup.</span></span>

<span data-ttu-id="26e5d-132"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="26e5d-132"><<<<<<< HEAD</span></span>
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="26e5d-133">Konfigurieren des Webservers für die Verwendung von TCP/IP-Sockets</span><span class="sxs-lookup"><span data-stu-id="26e5d-133">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="26e5d-p103">Sie haben zwei Möglichkeiten, den Webserver für die Verwendung von TCP/IP-Sockets zu konfigurieren. Welche Möglichkeit Sie wählen, hängt davon ab, ob über den Webserver auf alle Server mit SQL Server oder nur auf einen bestimmten Server zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="26e5d-p103">There are two options for configuring the Web server to use TCP/IP Sockets. What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="26e5d-p104">Wenn auf alle Server, auf denen SQL Server installiert ist, über den Webserver zugegriffen wird, müssen Sie das SQL Server-Clientkonfigurationsprogramm auf dem Webservercomputer ausführen. Mit den folgenden Schritten wird die Standardnetzwerkbibliothek für alle über diesen IIS-Webserver vorgenommenen SQL Server-Verbindungen für die Verwendung der TCP/IP-Sockets-Netzwerkbibliothek geändert.</span><span class="sxs-lookup"><span data-stu-id="26e5d-p104">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<a name="to-configure-the-web-server-all-sql-servers"></a><span data-ttu-id="26e5d-138">**So konfigurieren Sie den Webserver (alle Server mit SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="26e5d-138">**To configure the Web server (all SQL Servers)**</span></span>
=======
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="26e5d-139">Konfigurieren das Web Server auf TCP/IP-Sockets verwenden</span><span class="sxs-lookup"><span data-stu-id="26e5d-139">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="26e5d-140">Es gibt zwei Optionen für das Konfigurieren des Webservers zur Verwendung von TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="26e5d-140">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="26e5d-141">Was Sie tun, hängt davon, ob alle SQL Server aus dem Webserver zugegriffen wird oder nur eine bestimmte SQL Server erfolgt über den Webserver.</span><span class="sxs-lookup"><span data-stu-id="26e5d-141">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="26e5d-142">Wenn alle SQL Server aus dem Webserver zugegriffen wird, müssen Sie die SQL Server-Clientkonfigurationsprogramm auf dem Webservercomputer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26e5d-142">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="26e5d-143">Die folgenden Schritte ändern die Standard-Netzwerkbibliothek für alle SQL Server-Verbindungen, die mit der Verwendung der TCP/IP-Sockets-Netzwerkbibliothek IIS-Webservers.</span><span class="sxs-lookup"><span data-stu-id="26e5d-143">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="26e5d-144">**So konfigurieren Sie den Webserver (alle SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="26e5d-144">**To configure the web server (all SQL Servers)**</span></span>
>>>>>>> <span data-ttu-id="26e5d-145">master</span><span class="sxs-lookup"><span data-stu-id="26e5d-145">master</span></span>

<span data-ttu-id="26e5d-146">**Für Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="26e5d-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="26e5d-147">Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 6.5**, und klicken Sie dann auf **SQL Clientkonfigurationsprogramm**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="26e5d-148">Klicken Sie auf die Registerkarte **Netzwerkbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-148">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="26e5d-149">Wählen Sie im Feld **Standardnetzwerk** die Option **TCP/IP-Sockets** aus.</span><span class="sxs-lookup"><span data-stu-id="26e5d-149">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="26e5d-150">Klicken Sie auf **Fertig**, um die Änderungen zu speichern und das Hilfsprogramm zu beenden.</span><span class="sxs-lookup"><span data-stu-id="26e5d-150">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="26e5d-151">**Für Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="26e5d-151">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="26e5d-152">Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 7.0**, und klicken Sie dann auf **Server-Clientkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-152">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="26e5d-153">Klicken Sie auf die Registerkarte **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-153">Click the **General** tab.</span></span>

3.  <span data-ttu-id="26e5d-154">Klicken Sie im Feld **Standard-Netzwerkbibliothek** auf **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-154">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="26e5d-155">Klicken Sie auf **OK**, um die Änderungen zu speichern und das Hilfsprogramm zu beenden.</span><span class="sxs-lookup"><span data-stu-id="26e5d-155">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="26e5d-156"><<<<<<< HEAD, wenn eine bestimmte SQL Server auf einem Webserver zugegriffen wird, müssen Sie die SQL Server-Clientkonfigurationsprogramm auf dem Webservercomputer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26e5d-156"><<<<<<< HEAD If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</span></span> <span data-ttu-id="26e5d-157">Konfigurieren Sie die SQL Server-Clientsoftware auf dem Webservercomputer wie im Folgenden beschrieben, um die Netzwerkbibliothek für eine bestimmte SQL Server-Verbindung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="26e5d-157">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<a name="to-configure-the-web-server-a-specific-sql-server"></a><span data-ttu-id="26e5d-158">**So konfigurieren Sie den Webserver (ein bestimmter Server mit SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="26e5d-158">**To configure the Web server (a specific SQL Server)**</span></span>
=======
<span data-ttu-id="26e5d-159">Wenn eine bestimmte SQL Server auf einem Webserver zugegriffen wird, müssen Sie die SQL Server-Clientkonfigurationsprogramm auf dem Webservercomputer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26e5d-159">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="26e5d-160">Um die Netzwerkbibliothek für eine bestimmte SQL Server-Verbindung zu ändern, konfigurieren Sie die SQL Server-Clientsoftware wie folgt auf dem Webservercomputer aus.</span><span class="sxs-lookup"><span data-stu-id="26e5d-160">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="26e5d-161">**So konfigurieren Sie die Webserver (eine bestimmte SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="26e5d-161">**To configure the web server (a specific SQL Server)**</span></span>
>>>>>>> <span data-ttu-id="26e5d-162">master</span><span class="sxs-lookup"><span data-stu-id="26e5d-162">master</span></span>

<span data-ttu-id="26e5d-163">**Für Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="26e5d-163">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="26e5d-164">Im Menü **Start** zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server 6.5**, und klicken Sie dann auf **SQL Clientkonfigurationsprogramm**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-164">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="26e5d-165">Klicken Sie auf die Registerkarte **Erweitert**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-165">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="26e5d-166">Geben Sie in das Feld **Server** den Namen des Servers ein, mit dem die Verbindung bei Verwendung von **TCP/IP-Sockets** hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="26e5d-166">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="26e5d-167">Wählen Sie im Feld **DLL-Name** die Option **TCP/IP-Sockets** aus.</span><span class="sxs-lookup"><span data-stu-id="26e5d-167">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="26e5d-p109">Klicken Sie auf **Hinzufügen/Ändern**. Alle Datenquellen, die auf diesen Server verweisen, verwenden nun TCP/IP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="26e5d-p109">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="26e5d-170">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-170">Click **Done**.</span></span>

<span data-ttu-id="26e5d-171">**Für Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="26e5d-171">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="26e5d-172">Zeigen Sie über **das Startmenü** auf **Programme**, zeigen Sie auf **Microsoft SQL Server 7.0**, und klicken Sie dann auf **Clientkonfigurationsprogramm**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-172">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="26e5d-173">Klicken Sie auf die Registerkarte **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-173">Click the **General** tab.</span></span>

3.  <span data-ttu-id="26e5d-174">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-174">Click **Add**.</span></span>

4.  <span data-ttu-id="26e5d-p110">Geben Sie den Alias des Servers in das Feld **SQL Server-Alias** ein. Klicken Sie im Feld **Netzwerkbibliotheken** auf **TCP/IP**. Geben Sie in das Feld **Computername** den Namen des Computer ein, der TCP/IP-Sockets-Clients überwacht. Geben Sie in das Feld **Portnummer** den Port ein, auf dem der SQL Server lauscht.</span><span class="sxs-lookup"><span data-stu-id="26e5d-p110">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="26e5d-179">Klicken Sie auf **OK** und dann noch einmal auf **OK**, um das Hilfsprogramm zu schließen.</span><span class="sxs-lookup"><span data-stu-id="26e5d-179">Click **OK**, and then **OK** again to exit the utility.</span></span>

