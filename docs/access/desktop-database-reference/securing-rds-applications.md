---
title: Sichern von RDS-Anwendungen
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d7bc9ff4741ca9a6eccfb6ede3f569c18d0d20e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606468"
---
# <a name="securing-rds-applications"></a>Sichern von RDS-Anwendungen

**Betrifft**: Access 2013 | Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Sicherheitsaspekte zu Microsoft Internet Explorer

Da die Sicherheit von Microsoft® Internet Explorer verbessert wurde, können einige ADO- und RDS-Objekte nur noch in der Umgebung eines "abgesicherten" Modus ausgeführt werden. Machen Sie sich deshalb mit diesen Aspekten vertraut. Dazu gehören auch verschiedene Zonen, Sicherheitsebenen, eingeschränktes Verhalten, unsichere Operationen und angepasste Sicherheitseinstellungen.

Weitere Informationen zu diesen Aspekten finden Sie unter den entsprechenden ADO- und RDS-Sicherheitsthemen zu Microsoft Internet Explorer in den technischen Artikeln zu ActiveX Data Objects (ADO).

<<<<<<< Kopf
## <a name="security-and-your-web-server"></a>Sicherheit des Webservers

Beachten Sie bei der Verwendung des RDSServer.DataFactory-Objekts auf Ihrem Internet-Webserver, dass dadurch möglicherweise ein Sicherheitsrisiko entsteht. Externe Benutzer, die einen gültigen Datenquellennamen (DNS), eine Benutzer-ID und Kennwortinformationen besitzen, könnten Seiten schreiben, mit denen Abfragen an diese Datenquelle gesendet werden. Sie können den Zugriff auf diese Datenquelle u. a. einschränken, indem Sie die Registrierung des RDSServer.DataFactory-Objekts (msadcf.dll) aufheben, das Objekt löschen und stattdessen benutzerdefinierte Geschäftsobjekte mit hartcodierten Abfragen verwenden.
=======
## <a name="security-and-your-web-server"></a>Sicherheit und das Web Server

Wenn Sie das [RDSServer.DataFactory](datafactory-object-rdsserver.md) -Objekt auf Ihrem Webserver Internet verwenden, denken Sie daran, dass dies ein potenzielles Sicherheitsrisiko erstellt. Externe Benutzern, die gültige Datenquellennamen (DSN), Benutzer-ID und Kennwortinformationen erhalten könnten Seiten zum Senden von Abfragen zu dieser Datenquelle schreiben. Wenn Sie Zugriff auf eine Datenquelle möchten, ist eine Option zum Aufheben der Registrierung und löschen Sie das **RDSServer.DataFactory** -Objekt (msadcf.dll) und benutzerdefinierte Geschäftsobjekte stattdessen mit hartcodierten Abfragen verwenden.
>>>>>>> master

Weitere Informationen über die Sicherheitsaspekte bei der Verwendung des RDSServer.DataFactory-Objekts finden Sie unter Microsoft-Sicherheitsbulletin MS99-025 auf der [Microsoft Security-Website](https://www.microsoft.com/en-us/security/default.aspx).

## <a name="client-impersonation-and-security"></a>Sicherheit beim Clientidentitätswechsel

<<<<<<< HEAD Wenn die **Kennwortauthentifizierung** -Eigenschaft für den IIS-Webserver wird festgelegt auf Windows NT NTLM-Authentifizierung (für Windows NT 4.0) oder auf integrierte Windows-Authentifizierung (für Windows 2000), klicken Sie dann Business Objekte werden unter den Client Sicherheitskontext aufgerufen. Dies ist ein neues Feature in RDS 1.5, das den Clientidentitätswechsel über HTTP zulässt. Bei der Arbeit in diesem Modus werden die Anmeldung an den Webserver (IIS) ist nicht anonyme, verwendet die Benutzer-ID und das Kennwort, das unter der Clientcomputer ausgeführt wird. Wenn die ODBC-Datenquellennamen für die Verwendung der vertrauenswürdigen Verbindung eingerichtet sind, erfolgt der Zugriff auf Datenbanken, wie SQL Server, auch Sicherheitskontext des Clients. Aber dies funktioniert nur, wenn die Datenbank auf demselben Computer wie der IIS. die Anmeldeinformationen des Clients können nicht auf noch einen anderen Computer übertragen werden.

<a name="for-example-a-client-john-doe-with-useridjohnd-and-passwordsecret-is-logged-on-to-a-client-computer-he-runs-a-browser-based-application-that-needs-to-access-the-rdsserverdatafactory-object-to-create-a-recordsetrecordset-object-adomd-by-executing-an-sql-query-on-the-myserver-computer-running-iis-myserver-a-system-running-windows-nt-server-40-is-set-up-to-use-windows-nt-challengeresponse-authentication-its-odbc-dsn-has-use-trusted-connection-selected-and-the-server-also-contains-the-sql-server-data-source-when-a-request-is-received-on-the-web-server-it-asks-the-client-for-the-user-id-and-password-thus-the-request-is-logged-on-myserver-as-coming-from-johndsecret-instead-of-iusermyserver-which-is-the-default-when-anonymous-password-authentication-is-on-similarly-when-logging-on-to-sql-server-johndsecret-is-used"></a>Angenommen, ein Client John Doe mit Userid = "HerbertD" und das Kennwort = "Secret" an einem Clientcomputer angemeldet ist. Er führt eine browserbasierte Anwendung, die auf das **RDSServer.DataFactory** -Objekt, um ein [Recordset-Objekt](recordset-object-ado.md) erstellen, indem Sie eine SQL-Abfrage ausführen, auf dem Computer "MyServer" mit IIS zugreifen muss. MyServer, einem System mit Windows NT Server 4.0, Windows NT NTLM-Authentifizierung eingerichtet ist, dessen ODBC-DSN "Vertrauenswürdige Verbindung verwenden" ausgewählt wurde und der Server enthält auch die SQL Server-Datenquelle. Wenn eine Anforderung auf dem Webserver empfangen wird, werden Sie den Client für den Benutzer-ID und das Kennwort gefragt. Daher die Anforderung angemeldet ist MyServer entnommen "HerbertD" / "Geheim" anstelle von IUSER\_MyServer (die Standardeinstellung ist, wenn anonyme Kennwortauthentifizierung aktiviert ist). In ähnlicher Weise bei der Anmeldung bei SQL Server "HerbertD" / "Geheim" wird verwendet.
=======
Wenn die **Kennwortauthentifizierung** -Eigenschaft für den IIS-Webserver auf Windows NT NTLM-Authentifizierung (für Windows NT 4.0) oder auf integrierte Windows-Authentifizierung (für Windows 2000) festgelegt ist, werden klicken Sie dann von Geschäftsobjekten unter des Clients aufgerufen Sicherheitskontext. Dies ist ein neues Feature in RDS 1.5, das den Clientidentitätswechsel über HTTP zulässt. Bei der Arbeit in diesem Modus werden die Anmeldung an den Webserver (IIS) ist nicht anonyme, verwendet die Benutzer-ID und das Kennwort, das unter der Clientcomputer ausgeführt wird. Wenn die ODBC-Datenquellennamen für die Verwendung der vertrauenswürdigen Verbindung eingerichtet sind, erfolgt der Zugriff auf Datenbanken, wie SQL Server, auch Sicherheitskontext des Clients. Aber dies funktioniert nur, wenn die Datenbank auf demselben Computer wie der IIS. die Anmeldeinformationen des Clients können nicht auf noch einen anderen Computer übertragen werden.

Angenommen, ein Client John Doe mit Userid = "HerbertD" und das Kennwort = "Secret" an einem Clientcomputer angemeldet ist. Er führt eine browserbasierte Anwendung, die auf das **RDSServer.DataFactory** -Objekt, um ein [Recordset-Objekt](recordset-object-ado.md) erstellen, indem Sie eine SQL-Abfrage ausführen, auf dem Computer "MyServer" mit IIS zugreifen muss. MyServer, einem System mit Windows NT Server 4.0, Windows NT NTLM-Authentifizierung eingerichtet ist, dessen ODBC-DSN "Vertrauenswürdige Verbindung verwenden" ausgewählt wurde und der Server enthält auch die SQL Server-Datenquelle. Wenn eine Anforderung auf dem Webserver empfangen wird, werden Sie den Client für den Benutzer-ID und das Kennwort gefragt. Daher die Anforderung angemeldet ist MyServer entnommen "HerbertD" / "Geheim" anstelle von IUSER\_MyServer (die Standardeinstellung ist, wenn anonyme Kennwortauthentifizierung aktiviert ist). In ähnlicher Weise bei der Anmeldung bei SQL Server "HerbertD" / "Geheim" wird verwendet.
>>>>>>> master

Folglich lässt der IIS-Abfrage/Rückmeldung-Authentifizierungsmodus von Windows NT das Erstellen von HTML-Seiten zu, ohne dass Benutzer ausdrücklich nach der für die Anmeldung an der Datenbank erforderlichen Benutzer-ID und dem Kennwort gefragt werden. Bei Verwendung der IIS-Standardauthentifizierung wäre dies ebenfalls erforderlich.

## <a name="password-authentication"></a>Kennwortauthentifizierung

<<<<<<< HEAD RDS mit IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren kann: anonyme, die Standard-, oder NT NTLM-Authentifizierung (integrierte Windows-Authentifizierung in Windows 2000 genannt). Diese Einstellungen definieren, wie der Zugriff über einen Webserver gesteuert wird, wie beispielsweise, ob ein Clientcomputer explizite Zugriffsberechtigungen für den NT-Webserver besitzen muss.
=== RDS kann mit einem IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren: anonyme, die Standard-, oder NT NTLM-Authentifizierung (integrierte Windows-Authentifizierung in Windows 2000 genannt). Diese Einstellungen definieren, wie Steuerelemente ein Webserver Zugriff über, wie etwa festzulegen, dass es sich bei ein Clientcomputer auf dem Webserver NT expliziten Zugriffsrechte haben.
>>>>>>> master
