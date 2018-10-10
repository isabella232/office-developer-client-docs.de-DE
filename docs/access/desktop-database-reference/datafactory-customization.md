---
title: DataFactory-Anpassung
TOCTitle: DataFactory Customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b805f9d6ff7a1f3b27bb5600d42cabf8fce651cd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475332"
---
# <a name="datafactory-customization"></a>DataFactory-Anpassung


**Betrifft**: Access 2013 | Office 2013

Durch Remote Data Service (RDS) wird eine Möglichkeit bereitgestellt, problemlosen Datenzugriff in einem dreistufigen Client-/Server-System auszuführen. Durch ein Clientdatensteuerelement werden die Parameter für Verbindungs- und Befehlszeichenfolgen zum Ausführen einer Abfrage für eine Remotedatenquelle oder Parameter für Verbindungszeichenfolgen und [Recordset](recordset-object-ado.md)-Objekte zum Ausführen einer Aktualisierung angegeben.

Die Parameter werden einem Serverprogramm übergeben, durch das die Datenzugriffsoperation für die Remotedatenquelle ausgeführt wird. Durch RDS wird ein Standardserverprogramm, das [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt, bereitgestellt. Durch das **RDSServer.DataFactory** -Objekt werden alle von einer Abfrage an den Client erzeugten **Recordset** -Objekte zurückgegeben.

**RDSServer.DataFactory** ist jedoch auf das Ausführen von Abfragen und Aktualisierungen beschränkt. Eine Überprüfung oder Verarbeitung der Verbindungs- oder Befehlszeichenfolgen kann nicht ausgeführt werden.

Sie können mit ADO angeben, dass **DataFactory** in Verbindung mit einem anderen Serverprogrammtyp, einem *Handler*, verwendet werden soll. Durch den Handler können Clientverbindungs- und -befehlszeichenfolgen geändert werden, bevor sie zum Zugreifen auf die Datenquelle verwendet werden. Außerdem können durch den Handler Zugriffsrechte erzwungen werden, durch die die Fähigkeit des Clients zum Lesen und Schreiben von Daten in der Datenquelle gesteuert wird.

Die vom Handler zum Ändern von Clientparametern und Zugriffsrechten verwendeten Parameter werden in Abschnitten einer Anpassungsdatei angegeben.

Weitere Informationen zum Anpassen des **DataFactory** -Objekts finden Sie unter den folgenden Themen:

  - [Grundlegendes zur Anpassungsdatei](understanding-the-customization-file.md)

  - [Connect-Abschnitt der Anpassungsdatei](customization-file-connect-section.md)

  - [SQL-Abschnitt der Anpassungsdatei](customization-file-sql-section.md)

  - [UserList-Abschnitt der Anpassungsdatei](customization-file-userlist-section.md)

  - [Logs-Abschnitt der Anpassungsdatei](customization-file-logs-section.md)

  - [Erforderliche Clienteinstellungen](https://msdn.microsoft.com/library/ff836356\(v=office.15\))

  - [Schreiben eines eigenen benutzerdefinierten Handlers](https://msdn.microsoft.com/library/jj249402\(v=office.15\))

