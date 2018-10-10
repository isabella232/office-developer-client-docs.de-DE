---
title: Sichern von RDS-Anwendungen
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16dd0fd983d6e04f01c7d848a8d45f82b0f1c85a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473116"
---
# <a name="securing-rds-applications"></a>Sichern von RDS-Anwendungen

**Betrifft**: Access 2013 | Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Sicherheitsaspekte zu Microsoft Internet Explorer

Da die Sicherheit von Microsoft® Internet Explorer verbessert wurde, können einige ADO- und RDS-Objekte nur noch in der Umgebung eines "abgesicherten" Modus ausgeführt werden. Machen Sie sich deshalb mit diesen Aspekten vertraut. Dazu gehören auch verschiedene Zonen, Sicherheitsebenen, eingeschränktes Verhalten, unsichere Operationen und angepasste Sicherheitseinstellungen.

Weitere Informationen zu diesen Aspekten finden Sie unter den entsprechenden ADO- und RDS-Sicherheitsthemen zu Microsoft Internet Explorer in den technischen Artikeln zu ActiveX Data Objects (ADO).

## <a name="security-and-your-web-server"></a>Sicherheit des Webservers

Beachten Sie bei der Verwendung des RDSServer.DataFactory-Objekts auf Ihrem Internet-Webserver, dass dadurch möglicherweise ein Sicherheitsrisiko entsteht. Externe Benutzer, die einen gültigen Datenquellennamen (DNS), eine Benutzer-ID und Kennwortinformationen besitzen, könnten Seiten schreiben, mit denen Abfragen an diese Datenquelle gesendet werden. Sie können den Zugriff auf diese Datenquelle u. a. einschränken, indem Sie die Registrierung des RDSServer.DataFactory-Objekts (msadcf.dll) aufheben, das Objekt löschen und stattdessen benutzerdefinierte Geschäftsobjekte mit hartcodierten Abfragen verwenden.

Weitere Informationen über die Sicherheitsaspekte bei der Verwendung des RDSServer.DataFactory-Objekts finden Sie unter Microsoft-Sicherheitsbulletin MS99-025 auf der [Microsoft Security-Website](https://www.microsoft.com/en-us/security/default.aspx).

## <a name="client-impersonation-and-security"></a>Sicherheit beim Clientidentitätswechsel

Wenn die **Password Authentication** -Eigenschaft für Ihren IIS-Webserver auf die Abfrage/Rückmeldung-Authentifizierung von Windows NT (bei Windows NT 4.0) oder auf die integrierte Windows-Authentifizierung (bei Windows 2000) festgelegt ist, werden die Geschäftsobjekte unter dem Sicherheitskontext des Clients aufgerufen. Das ist ein neues Feature in RDS 1.5, das den Clientidentitätswechsel über HTTP zulässt. Bei der Arbeit in diesem Modus erfolgt die Anmeldung am Webserver (IIS) nicht anonym, sondern es werden die Benutzer-ID und das Kennwort verwendet, unter denen der Clientcomputer ausgeführt wird. Wenn die ODBC-Datenquellennamen für die Verwendung der vertrauenswürdigen Verbindung eingerichtet sind, erfolgt der Zugriff auf Datenbanken (z. B. SQL Server) ebenfalls unter dem Sicherheitskontext des Clients. Das funktioniert jedoch nur, wenn sich die Datenbank auf demselben Computer wie IIS befindet, denn die Anmeldeinformationen des Clients können nicht auf einen weiteren Computer übertragen werden.

Angenommen, ein Client John Doe mit Userid = "HerbertD" und das Kennwort = "Secret" an einem Clientcomputer angemeldet ist. Er führt eine browserbasierte Anwendung, die auf das **RDSServer.DataFactory** -Objekt, um ein [Recordset-Objekt](recordset-object-ado.md) erstellen, indem Sie eine SQL-Abfrage ausführen, auf dem Computer "MyServer" mit IIS zugreifen muss. MyServer, einem System mit Windows NT Server 4.0, Windows NT NTLM-Authentifizierung eingerichtet ist, dessen ODBC-DSN "Vertrauenswürdige Verbindung verwenden" ausgewählt wurde und der Server enthält auch die SQL Server-Datenquelle. Wenn eine Anforderung auf dem Webserver empfangen wird, werden Sie den Client für den Benutzer-ID und das Kennwort gefragt. Daher die Anforderung angemeldet ist MyServer entnommen "HerbertD" / "Geheim" anstelle von IUSER\_MyServer (die Standardeinstellung ist, wenn anonyme Kennwortauthentifizierung aktiviert ist). In ähnlicher Weise bei der Anmeldung bei SQL Server "HerbertD" / "Geheim" wird verwendet.

Folglich lässt der IIS-Abfrage/Rückmeldung-Authentifizierungsmodus von Windows NT das Erstellen von HTML-Seiten zu, ohne dass Benutzer ausdrücklich nach der für die Anmeldung an der Datenbank erforderlichen Benutzer-ID und dem Kennwort gefragt werden. Bei Verwendung der IIS-Standardauthentifizierung wäre dies ebenfalls erforderlich.

## <a name="password-authentication"></a>Kennwortauthentifizierung

RDS kann mit einem IIS-Webserver kommunizieren, der in einem der drei Modi der Kennwortauthentifizierung ausgeführt wird: anonym, Standard oder Abfrage/Rückmeldung-Authentifizierung von Windows NT (in Windows 2000 als integrierte Windows-Authentifizierung bezeichnet). Diese Einstellungen definieren, wie der Zugriff über einen Webserver gesteuert wird, wie beispielsweise, ob ein Clientcomputer explizite Zugriffsberechtigungen für den NT-Webserver besitzen muss.

