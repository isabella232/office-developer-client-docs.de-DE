---
title: Änderungen in Access (Zugriff PC-Datenbank-Referenz)
TOCTitle: Changes in Access
description: Access umfasst keine Unterstützung für Access-Datenprojekte (ADPs). In Access wird erstmals ein neuer Anwendungstyp verwendet, der es Ihnen ermöglicht, eine webbasierte Access-App zu erstellen.
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 4563ccafb9f4078f7016abf6d5bb96ac37b4bddd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878801"
---
# <a name="changes-in-access"></a>Änderungen in Access

**Gilt für:** Access 2013 | Office 2013

Access umfasst keine Unterstützung für Access-Datenprojekte (ADPs). In Access wird erstmals ein neuer Anwendungstyp verwendet, der es Ihnen ermöglicht, eine webbasierte Access-App zu erstellen. Mithilfe dieser Anwendungstyp können Sie webbasierten Anwendungen erstellen, die verwenden die Leistungsfähigkeit von SQL Server lokal oder in der Cloud.

In einer Access-app auf SharePoint-Server Wenn Sie einer Tabelle, einer Abfrage oder ein Datenmakro in Access-Client erstellen, in der Sie Tabellen, Sichten oder Trigger in einer SQL Server-Datenbank erstellen, mit dem Access-Client, können Sie Ihre Datenbank in andere Anwendungen, Conn öffnen die externen Inhaltstypen für SqlServer. So können Sie Ihre Daten freigeben oder Daten aus anderen Systemen in Ihre Access-App laden.

Mit Office 365 und Access können Sie Anwendungen erstellen, die Ihre Benutzer erreichen, ohne dass Sie sich Gedanken um Probleme bei Bereitstellung und Installation oder um die Kompatibilität von Betriebssystemen machen müssen. Erstellen Sie Ihre App an einem Ort, und geben Sie sie mit den leistungsstarken Funktionen von SQL Azure und SQL Server im Web frei.

[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview), die Cloudversion von SQL Server, bietet keine Unterstützung für Features, die für die Funktion von Access-Datenprojekten (ADPs) erforderlich sind. Für die Unterstützung von ADPs in SQL Azure, Access wären erhebliche Änderungen nötig.

Aus diesen Gründen unterstützt Access keine ADPs. ADPs worden ein hervorragendes Tool für die Arbeit mit SQL Server in einer lokalen Umgebung; viel wurde jedoch seit ADPs in Access 2000 eingeführt wurden geändert. Die Benutzer erwarten nun, dass ihnen ihre Datenbank standortunabhängig zur Verfügung stehen.

## <a name="adp-support-and-the-future"></a>ADP-Unterstützung und die Zukunft

ADPs funktionieren nach wie vor in früheren Versionen von Access. Sie können weiterhin Ihre ADP-Anwendungen entwickeln, und wir werden weiterhin Support für frühere Versionen von Access im Rahmen des standardmäßigen [Support Lifecycle](https://support.microsoft.com/lifecycle/search) bieten. Es wird kein Update älterer Versionen von Access geben, um neue Versionen von SQL Server oder SQL Azure zu unterstützen. Daher kann es zu Problemen kommen, wenn Sie SQL Server 2012 oder höher mit Ihren ADPs verwenden. ADPs unterstützen weiterhin SQL 2008 R2 und frühere Versionen.

Für die Zukunft haben ADP-Entwickler verschiedene Möglichkeiten:

- **Konvertieren in eine Access-app** – Using Access können Sie die Tabellen in einer neuen Access-app importieren und Formulare für die Anwendung automatisch für Sie erstellt werden. Sie können die Funktionalität Basis Formulare, die Access erstellt wird, erweitern, und Benutzer können die Anwendung im Web verwenden. Zwar stehen einige der Funktionen, die Sie in ADPs verwenden, derzeit möglicherweise nicht zur Verfügung, Sie können jedoch davon ausgehen, dass sich Microsoft weiterhin intensiv mit Produktverbesserungen für diesen Anwendungstyps beschäftigen wird.

- **Konvertieren in eine verknüpfte desktop-Datenbank** – Access weiterhin erstellen Desktopdatenbanken in das ACCDB-Dateiformat unterstützt. Sie können Ihre Anwendung einschließlich aller vorhandenen Formulare und Berichte in das ACCDB-Format konvertieren und die Daten in SQL Server belassen. Sie können mit SQL Server-Datenbank mithilfe von verknüpften Tabellen verknüpfen, und Ihre Anwendung weiterhin mit denselben Daten ausgeführt werden.

- **Erstellen einer Hybrid-Anwendung** – Wenn die Anwendung groß ist und Sie nicht alles gleichzeitig konvertieren möchten, können Sie Ihre Daten in einer Access-app und Verknüpfen mit der SQL Server-Datenbank von einer ACCDB importieren. Auf diese Weise können Sie schrittweise, Migration hinzufügen Formulare und Funktionen über einen Zeitraum zu Ihrer Access-app beim Verwalten der Clientanwendung als einer ACCDB mit verknüpften Tabellen mit der SQL Server-Datenbank hinter der Access-app.

- **Durchführen eines Upgrades auf .NET Framework** – die Anwendung möglicherweise komplex erwägen, eine professionelle Entwicklungsplattform wie .NET Framework. SQL Server soll, verwenden Sie die vorhandene Datenbankinfrastruktur, und erweitern die Funktionalität der Anwendung ohne erheblich umschreiben des Codes zu erleichtern.

## <a name="conclusion"></a>Schlussbemerkung

Access ist dafür konzipiert, Datenbanken mit der Cloud zu verbinden, indem auf SharePoint Server- und SQL Server-Technologien aufgebaut wird, und die Arbeit mit Office 365 zu erleichtern. Access wurde entwickelt, um Sie beim Erstellen und Freigeben datenintensiver Geschäfts-Apps zu unterstützen, die Sie für Ihre Geschäftsabläufe benötigen.

## <a name="see-also"></a>Siehe auch

- [Neu in Access 2013 für Entwickler](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


