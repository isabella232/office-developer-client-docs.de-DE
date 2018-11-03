---
title: Sichern von RDS-Anwendungen
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4240ca118adfcc122ebe346cb60f8b9a0b6efd9e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937491"
---
# <a name="securing-rds-applications"></a>Sichern von RDS-Anwendungen

**Betrifft**: Access 2013, Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Sicherheitsaspekte zu Microsoft Internet Explorer

Mit neuen Security optimierten Features von Microsoft Internet Explorer sind einige ADO- und RDS-Objekte nur in einer Umgebung "sicher" Modus ausgeführt. Dies erfordert, dass Sie diesen Problemen, einschließlich der verschiedenen Zonen, Sicherheitsstufen, strengen Verhalten, unsichere Vorgänge kennen und Sicherheitseinstellungen angepasst.

Weitere Informationen zu diesen Aspekten finden Sie unter den entsprechenden ADO- und RDS-Sicherheitsthemen zu Microsoft Internet Explorer in den technischen Artikeln zu ActiveX Data Objects (ADO).

## <a name="security-and-your-web-server"></a>Sicherheit und das Web Server

Wenn Sie das [RDSServer.DataFactory](datafactory-object-rdsserver.md) -Objekt auf Ihrem Webserver Internet verwenden, denken Sie daran, dass dies ein potenzielles Sicherheitsrisiko erstellt. Externe Benutzern, die gültige Datenquellennamen (DSN), Benutzer-ID und Kennwortinformationen erhalten könnten Seiten zum Senden von Abfragen zu dieser Datenquelle schreiben. Wenn Sie Zugriff auf eine Datenquelle möchten, ist eine Option zum Aufheben der Registrierung und löschen Sie das **RDSServer.DataFactory** -Objekt (msadcf.dll) und benutzerdefinierte Geschäftsobjekte stattdessen mit hartcodierten Abfragen verwenden.

Weitere Informationen über die Sicherheitsaspekte bei der Verwendung des RDSServer.DataFactory-Objekts finden Sie unter Microsoft-Sicherheitsbulletin MS99-025 auf der [Microsoft Security-Website](https://www.microsoft.com/en-us/security/default.aspx).

## <a name="client-impersonation-and-security"></a>Sicherheit beim Clientidentitätswechsel

Wenn die **Kennwortauthentifizierung** -Eigenschaft für den IIS-Webserver auf Windows NT NTLM-Authentifizierung (für Windows NT 4.0) oder auf integrierte Windows-Authentifizierung (für Windows 2000) festgelegt ist, werden klicken Sie dann von Geschäftsobjekten unter des Clients aufgerufen Sicherheitskontext. Dies ist ein neues Feature in RDS 1.5, das den Clientidentitätswechsel über HTTP zulässt. Bei der Arbeit in diesem Modus werden die Anmeldung an den Webserver (IIS) ist nicht anonyme, verwendet die Benutzer-ID und das Kennwort, das unter der Clientcomputer ausgeführt wird. Wenn die ODBC-Datenquellennamen für die Verwendung der vertrauenswürdigen Verbindung eingerichtet sind, erfolgt der Zugriff auf Datenbanken, wie SQL Server, auch Sicherheitskontext des Clients. Aber dies funktioniert nur, wenn die Datenbank auf demselben Computer wie der IIS. die Anmeldeinformationen des Clients können nicht auf noch einen anderen Computer übertragen werden.

Angenommen, ein Client John Doe mit Userid = "HerbertD" und das Kennwort = "Secret" an einem Clientcomputer angemeldet ist. Er führt eine browserbasierte Anwendung, die auf das **RDSServer.DataFactory** -Objekt, um ein [Recordset-Objekt](recordset-object-ado.md) erstellen, indem Sie eine SQL-Abfrage ausführen, auf dem Computer "MyServer" mit IIS zugreifen muss. MyServer, einem System mit Windows NT Server 4.0, Windows NT NTLM-Authentifizierung eingerichtet ist, dessen ODBC-DSN "Vertrauenswürdige Verbindung verwenden" ausgewählt wurde und der Server enthält auch die SQL Server-Datenquelle. Wenn eine Anforderung auf dem Webserver empfangen wird, werden Sie den Client für den Benutzer-ID und das Kennwort gefragt. Daher die Anforderung angemeldet ist MyServer entnommen "HerbertD" / "Geheim" anstelle von IUSER\_MyServer (die Standardeinstellung ist, wenn anonyme Kennwortauthentifizierung aktiviert ist). In ähnlicher Weise bei der Anmeldung bei SQL Server "HerbertD" / "Geheim" wird verwendet.

Folglich lässt der IIS-Abfrage/Rückmeldung-Authentifizierungsmodus von Windows NT das Erstellen von HTML-Seiten zu, ohne dass Benutzer ausdrücklich nach der für die Anmeldung an der Datenbank erforderlichen Benutzer-ID und dem Kennwort gefragt werden. Bei Verwendung der IIS-Standardauthentifizierung wäre dies ebenfalls erforderlich.

## <a name="password-authentication"></a>Kennwortauthentifizierung

RDS kann mit einem IIS-Webserver ausgeführt wird, in einem der drei Modi Kennwortauthentifizierung kommunizieren: anonyme, die Standard-, oder NT NTLM-Authentifizierung (integrierte Windows-Authentifizierung in Windows 2000 genannt). Diese Einstellungen definieren, wie Steuerelemente ein Webserver Zugriff über, wie etwa festzulegen, dass es sich bei ein Clientcomputer auf dem Webserver NT expliziten Zugriffsrechte haben.

