---
title: Sichern von RDS-Anwendungen
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a531c01750117ae7abbf87e5ba4cb23daf37851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308778"
---
# <a name="securing-rds-applications"></a>Sichern von RDS-Anwendungen

**Gilt für**: Access 2013, Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Sicherheitsaspekte zu Microsoft Internet Explorer

Mit neuen Sicherheitsverbesserungen, die Microsoft Internet Explorer hinzugefügt werden, sind einige ADO-und RDS-Objekte nur in einer "sicheren" Modus-Umgebung eingeschränkt. Dies erfordert, dass Sie diese Probleme, einschließlich unterschiedlicher Zonen, Sicherheitsstufen, restriktive Verhalten, unsichere Vorgänge und angepasste Sicherheitseinstellungen wissen.

Weitere Informationen zu diesen Aspekten finden Sie unter den entsprechenden ADO- und RDS-Sicherheitsthemen zu Microsoft Internet Explorer in den technischen Artikeln zu ActiveX Data Objects (ADO).

## <a name="security-and-your-web-server"></a>Sicherheit und Ihr Webserver

Wenn Sie das [RDSServer. DataFactory](datafactory-object-rdsserver.md) -Objekt auf Ihrem Internet-Webserver verwenden, ist dies ein potenzielles Sicherheitsrisiko. External users who obtain valid data source name (DSN), user ID, and password information could write pages to send any query to that data source. If you want more restricted access to a data source, one option is to unregister and delete the **RDSServer.DataFactory** object (msadcf.dll), and instead use custom business objects with hard-coded queries.

Weitere Informationen zu den Sicherheitsimplikationen der Verwendung des RDSServer. dataFactory-Objekts finden Sie im Microsoft-Sicherheits Bulletin MS99-025 auf der [Microsoft-Sicherheitswebsite](https://www.microsoft.com/en-us/security/default.aspx).

## <a name="client-impersonation-and-security"></a>Sicherheit beim Clientidentitätswechsel

Wenn die **Kenn Wort Authentifizierungs** Eigenschaft für Ihren IIS-Webserver auf Windows NT Challenge/Response Authentication (für windows NT 4,0) oder auf integrierte Windows-Authentifizierung (für Windows 2000) festgelegt ist, werden Geschäftsobjekte unter dem Client Sicherheitskontext. Das ist ein neues Feature in RDS 1.5, das den Clientidentitätswechsel über HTTP zulässt. Wenn Sie in diesem Modus arbeiten, ist die Anmeldung am Webserver (IIS) nicht anonym, sondern verwendet die Benutzer-ID und das Kennwort, unter dem der Clientcomputer ausgeführt wird. Wenn die ODBC-Datenquellennamen für die Verwendung der vertrauenswürdigen Verbindung eingerichtet sind, erfolgt der Zugriff auf Datenbanken (z. B. SQL Server) ebenfalls unter dem Sicherheitskontext des Clients. Das funktioniert jedoch nur, wenn sich die Datenbank auf demselben Computer wie IIS befindet, denn die Anmeldeinformationen des Clients können nicht auf einen weiteren Computer übertragen werden.

Beispielsweise ist ein Client, John Doe, mit UserID = "JohnD" und Password = "Secret" an einem Clientcomputer angemeldet. Er führt eine browserbasierte Anwendung aus, die auf das **RDSServer. DataFactory-** Objekt zugreifen muss, um eine Daten [Satzgruppe](recordset-object-ado.md) zu erstellen, indem eine SQL-Abfrage auf dem "MyServer"-Computer mit IIS ausgeführt wird. MyServer, ein System mit Windows NT Server 4,0, ist für die Verwendung der Windows NT-Challenge/Response-Authentifizierung eingerichtet, der ODBC-DSN hat "vertrauenswürdige Verbindung verwenden" ausgewählt, und der Server enthält auch die SQL Server-Datenquelle. Wenn eine Anforderung auf dem Webserver empfangen wird, fordert Sie den Client auf, die Benutzer-ID und das Kennwort einzugeben. Daher wird die Anforderung bei MyServer protokolliert, da Sie von "JohnD"/"Secret" anstelle von\_iuser MyServer stammt (Dies ist die Standardeinstellung für die anonyme Kennwortauthentifizierung). Entsprechend wird bei der Anmeldung bei SQL Server "Johnsd"/"Secret" verwendet.

Folglich lässt der IIS-Abfrage/Rückmeldung-Authentifizierungsmodus von Windows NT das Erstellen von HTML-Seiten zu, ohne dass Benutzer ausdrücklich nach der für die Anmeldung an der Datenbank erforderlichen Benutzer-ID und dem Kennwort gefragt werden. Bei Verwendung der IIS-Standardauthentifizierung wäre dies ebenfalls erforderlich.

## <a name="password-authentication"></a>Kennwortauthentifizierung

RDS kann mit einem IIS-Webserver kommunizieren, der in einem der drei Kenn Wort Authentifizierungsmodi ausgeführt wird: Anonymous, Basic oder NT Challenge/Response Authentication (called Integrated Windows Authentication in Windows 2000). Diese Einstellungen definieren, wie ein Webserver den Zugriff darauf steuert, wie beispielsweise, dass ein Clientcomputer explizite Zugriffsrechte auf dem NT-Webserver hat.

