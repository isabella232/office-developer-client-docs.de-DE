---
title: Sichern von RDS-Anwendungen
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49476ab8bf3af8fadf4127fabd2966e888981af6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596876"
---
# <a name="securing-rds-applications"></a>Sichern von RDS-Anwendungen

**Gilt für**: Access 2013, Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Sicherheitsaspekte zu Microsoft Internet Explorer

Da microsoft Internet Explorer neue Sicherheitsverbesserungen hinzugefügt wurden, sind einige ADO- und RDS-Objekte auf die Ausführung in einer Umgebung mit sicherem Modus beschränkt. Dies erfordert, dass Sie sich dieser Probleme bewusst sind, einschließlich verschiedener Zonen, Sicherheitsstufen, restriktivem Verhalten, unsicheren Vorgängen und angepassten Sicherheitseinstellungen.

Weitere Informationen zu diesen Aspekten finden Sie unter den entsprechenden ADO- und RDS-Sicherheitsthemen zu Microsoft Internet Explorer in den technischen Artikeln zu ActiveX Data Objects (ADO).

## <a name="security-and-your-web-server"></a>Sicherheit und Ihr Webserver

Wenn Sie das [RDSServer.DataFactory-Objekt](datafactory-object-rdsserver.md) auf Ihrem Internetwebserver verwenden, denken Sie daran, dass dadurch ein potenzielles Sicherheitsrisiko entsteht. External users who obtain valid data source name (DSN), user ID, and password information could write pages to send any query to that data source. If you want more restricted access to a data source, one option is to unregister and delete the **RDSServer.DataFactory** object (msadcf.dll), and instead use custom business objects with hard-coded queries.

Weitere Informationen zu den Sicherheitsauswirkungen der Verwendung des RDSServer.DataFactory-Objekts finden Sie im Microsoft-Sicherheitsbulletin MS99-025 auf der [Microsoft Security-Website.](https://www.microsoft.com/en-us/security/default.aspx)

## <a name="client-impersonation-and-security"></a>Sicherheit beim Clientidentitätswechsel

Wenn die **Kennwortauthentifizierungseigenschaft** für Ihren IIS-Webserver auf Windows NT-Abfrage-/Antwortauthentifizierung (für Windows NT 4.0) oder auf integrierte Windows-Authentifizierung (für Windows 2000) festgelegt ist, werden Geschäftsobjekte im Sicherheitskontext des Clients aufgerufen. Das ist ein neues Feature in RDS 1.5, das den Clientidentitätswechsel über HTTP zulässt. Wenn Sie in diesem Modus arbeiten, ist die Anmeldung beim Webserver (IIS) nicht anonym, sondern verwendet die Benutzer-ID und das Kennwort, unter denen der Clientcomputer ausgeführt wird. Wenn die ODBC-Datenquellennamen für die Verwendung der vertrauenswürdigen Verbindung eingerichtet sind, erfolgt der Zugriff auf Datenbanken (z. B. SQL Server) ebenfalls unter dem Sicherheitskontext des Clients. Das funktioniert jedoch nur, wenn sich die Datenbank auf demselben Computer wie IIS befindet, denn die Anmeldeinformationen des Clients können nicht auf einen weiteren Computer übertragen werden.

Beispielsweise wird ein Client, John Doe, mit userid="JohnD" und password="secret" bei einem Clientcomputer angemeldet. Er führt eine browserbasierte Anwendung aus, die auf das **RDSServer.DataFactory-Objekt** zugreifen muss, um ein [Recordset](recordset-object-ado.md) zu erstellen, indem eine SQL Abfrage auf dem Computer "MyServer" ausgeführt wird, auf dem IIS ausgeführt wird. MyServer, ein System mit Windows NT Server 4.0, ist für die Verwendung Windows NT-Abfrage-/Antwortauthentifizierung eingerichtet, der ODBC-DSN hat "Vertrauenswürdige Verbindung verwenden" ausgewählt, und der Server enthält auch die SQL Server Datenquelle. Wenn eine Anforderung auf dem Webserver empfangen wird, wird der Client nach der Benutzer-ID und dem Kennwort gefragt. Daher wird die Anforderung bei MyServer als von "JohnD"/"Secret" anstelle von IUSER \_ MyServer (die Standardeinstellung bei aktivierter anonymer Kennwortauthentifizierung) protokolliert. Ebenso wird bei der Anmeldung bei SQL Server "JohnD"/"Secret" verwendet.

Folglich lässt der IIS-Abfrage/Rückmeldung-Authentifizierungsmodus von Windows NT das Erstellen von HTML-Seiten zu, ohne dass Benutzer ausdrücklich nach der für die Anmeldung an der Datenbank erforderlichen Benutzer-ID und dem Kennwort gefragt werden. Bei Verwendung der IIS-Standardauthentifizierung wäre dies ebenfalls erforderlich.

## <a name="password-authentication"></a>Kennwortauthentifizierung

RDS kann mit einem IIS-Webserver kommunizieren, der in einem der drei Kennwortauthentifizierungsmodi ausgeführt wird: Anonym, Standard- oder NT-Abfrage-/Antwortauthentifizierung (integrierte Windows-Authentifizierung in Windows 2000). Diese Einstellungen definieren, wie ein Webserver den Zugriff über ihn steuert, z. B. dass ein Clientcomputer über explizite Zugriffsberechtigungen auf dem NT-Webserver verfügt.

