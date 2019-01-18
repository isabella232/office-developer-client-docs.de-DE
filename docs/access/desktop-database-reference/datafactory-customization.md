---
title: DataFactory-Anpassung
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5fc1c284ee7aae77c4fb067ad57d50200119594
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700024"
---
# <a name="datafactory-customization"></a>DataFactory-Anpassung


**Betrifft**: Access 2013, Office 2013

Durch Remote Data Service (RDS) wird eine Möglichkeit bereitgestellt, problemlosen Datenzugriff in einem dreistufigen Client-/Server-System auszuführen. Durch ein Clientdatensteuerelement werden die Parameter für Verbindungs- und Befehlszeichenfolgen zum Ausführen einer Abfrage für eine Remotedatenquelle oder Parameter für Verbindungszeichenfolgen und [Recordset](recordset-object-ado.md)-Objekte zum Ausführen einer Aktualisierung angegeben.

Die Parameter werden einem Serverprogramm übergeben, durch das die Datenzugriffsoperation für die Remotedatenquelle ausgeführt wird. Durch RDS wird ein Standardserverprogramm, das [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt, bereitgestellt. Durch das **RDSServer.DataFactory** -Objekt werden alle von einer Abfrage an den Client erzeugten **Recordset** -Objekte zurückgegeben.

**RDSServer.DataFactory** ist jedoch auf das Ausführen von Abfragen und Aktualisierungen beschränkt. Eine Überprüfung oder Verarbeitung der Verbindungs- oder Befehlszeichenfolgen kann nicht ausgeführt werden.

Sie können mit ADO angeben, dass **DataFactory** in Verbindung mit einem anderen Serverprogrammtyp, einem *Handler*, verwendet werden soll. Durch den Handler können Clientverbindungs- und -befehlszeichenfolgen geändert werden, bevor sie zum Zugreifen auf die Datenquelle verwendet werden. Außerdem können durch den Handler Zugriffsrechte erzwungen werden, durch die die Fähigkeit des Clients zum Lesen und Schreiben von Daten in der Datenquelle gesteuert wird.

Die vom Handler zum Ändern von Clientparametern und Zugriffsrechten verwendeten Parameter werden in Abschnitten einer Anpassungsdatei angegeben.

Weitere Informationen zum Anpassen des **DataFactory** -Objekts finden Sie unter den folgenden Themen:

- [Grundlegendes zur Anpassungsdatei](understanding-the-customization-file.md)
- [Verbinden von Datei-Abschnitt der Anpassungsdatei](customization-file-connect-section.md)
- [Anpassungsdatei – SQL-Abschnitt](customization-file-sql-section.md)
- [Anpassungsdatei – UserList-Abschnitt](customization-file-userlist-section.md)
- [Anpassungsdatei – Protokollabschnitt](customization-file-logs-section.md)
- [Erforderliche Clienteinstellungen](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [Schreiben eines eigenen benutzerdefinierten Handlers](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
