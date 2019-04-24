---
title: Änderungen in Access (Access-Desktopdatenbankreferenz)
TOCTitle: Changes in Access
description: Access umfasst keine Unterstützung für Access-Datenprojekte (ADPs). In Access wird erstmals ein neuer Anwendungstyp verwendet, der es Ihnen ermöglicht, eine webbasierte Access-App zu erstellen.
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: de2ff21598639b445f5ff84240b115704b484209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296500"
---
# <a name="changes-in-access"></a>Änderungen in Access

**Gilt für:** Access 2013 | Office 2013

Access umfasst keine Unterstützung für Access-Datenprojekte (ADPs). In Access wird erstmals ein neuer Anwendungstyp verwendet, der es Ihnen ermöglicht, eine webbasierte Access-App zu erstellen. Mithilfe dieses Anwendungstyps können Sie webbasierte Anwendungen erstellen, die die Leistungsfähigkeit von SQL Server lokal oder in der Cloud nutzen.

In einer Access-App auf SharePoint Server beim Erstellen einer Tabelle, einer Abfrage oder eines Datenmakros im Access-Client, in dem Sie Tabellen, Ansichten oder Trigger in einer SQL Server-Datenbank erstellen. Mit dem Access-Client können Sie Ihre Datenbank in anderen Anwendungen öffnen, die eine Verbindung mit SQL Server herstellen. So können Sie Ihre Daten freigeben oder Daten aus anderen Systemen in Ihre Access-App laden.

Mit Office 365 und Access können Sie Anwendungen erstellen, die Ihre Benutzer erreichen, ohne dass Sie sich Gedanken um Probleme bei Bereitstellung und Installation oder um die Kompatibilität von Betriebssystemen machen müssen. Erstellen Sie Ihre App an einem Ort, und geben Sie sie mit den leistungsstarken Funktionen von SQL Azure und SQL Server im Web frei.

[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview), die Cloudversion von SQL Server, bietet keine Unterstützung für Features, die für die Funktion von Access-Datenprojekten (ADPs) erforderlich sind. Für die Unterstützung von ADPs in SQL Azure, Access wären erhebliche Änderungen nötig.

Daher unterstützt Access keine ADPs. ADPs waren ein hervorragendes Tool für die Arbeit mit SQL Server in einer lokalen Umgebung, jedoch hat sich seit der Einführung von ADPs in Access 2000 viel geändert. Die Benutzer erwarten nun, dass ihnen ihre Datenbank standortunabhängig zur Verfügung stehen.

## <a name="adp-support-and-the-future"></a>ADP-Unterstützung und die Zukunft

ADPs funktionieren nach wie vor in früheren Versionen von Access. Sie können weiterhin Ihre ADP-Anwendungen entwickeln, und wir werden weiterhin Support für frühere Versionen von Access im Rahmen des standardmäßigen [Support Lifecycle](https://support.microsoft.com/lifecycle/search) bieten. Es wird kein Update älterer Versionen von Access geben, um neue Versionen von SQL Server oder SQL Azure zu unterstützen. Daher kann es zu Problemen kommen, wenn Sie SQL Server 2012 oder höher mit Ihren ADPs verwenden. ADPs unterstützen weiterhin SQL 2008 R2 und frühere Versionen.

Für die Zukunft haben ADP-Entwickler verschiedene Möglichkeiten:

- **Konvertieren in eine Access-App** – Mit Access können Sie Ihre Tabellen in eine neue Access-App importieren. Formulare für Ihre Anwendung werden automatisch für Sie erstellt. Sie können den Funktionsumfang der von Access erstellten Basisformulare erweitern, und Benutzer können Ihre Anwendung im Web verwenden. Zwar stehen einige der Funktionen, die Sie in ADPs verwenden, derzeit möglicherweise nicht zur Verfügung, Sie können jedoch davon ausgehen, dass sich Microsoft weiterhin intensiv mit Produktverbesserungen für diesen Anwendungstyps beschäftigen wird.

- **Konvertieren in eine verknüpfte Desktopdatenbank** – Access unterstützt weiterhin die Erstellung von Desktopdatenbanken im ACCDB-Dateiformat. Sie können Ihre Anwendung einschließlich aller vorhandenen Formulare und Berichte in das ACCDB-Format konvertieren und die Daten in SQL Server belassen. Mithilfe verknüpfter Tabellen können Sie eine Verknüpfung mit der SQL Server-Datenbank herstellen, und Ihre Anwendung arbeitet weiterhin mit denselben Daten.

- **Erstellen einer Hybridanwendung** – Wenn Sie über eine große Anwendung verfügen und nicht alles gleichzeitig konvertieren möchten, können Sie Ihre Daten in eine Access-App importieren und von einer ACCDB-Datei eine Verknüpfung mit der SQL Server-Datenbank herstellen. Dies ermöglicht Ihnen eine schrittweise Migration, bei der Sie Formulare und Funktionen nach und nach zur Ihrer Access-App hinzufügen und dabei Ihre Clientanwendung als eine ACCDB-Datei verwalten, deren Tabellen mit der SQL Server-Datenbank hinter der Access-App verknüpft sind.

- **Upgrade auf .NET Framework** – Ihre Anwendung ist möglicherweise so komplex, dass sich der Umstieg auf eine professionelle Entwicklungsplattform wie z. B. .NET Framework empfiehlt. SQL Server vereinfacht die Nutzung Ihrer bereits vorhandenen Datenbankinfrastruktur und die Erweiterung des Funktionsumfangs Ihrer Anwendung, ohne dass ein umfangreiches Umschreiben des Codes erforderlich ist.

## <a name="conclusion"></a>Schlussbemerkung

Access ist dafür konzipiert, Datenbanken mit der Cloud zu verbinden, indem auf SharePoint Server- und SQL Server-Technologien aufgebaut wird, und die Arbeit mit Office 365 zu erleichtern. Access wurde entwickelt, um Sie beim Erstellen und Freigeben datenintensiver Geschäfts-Apps zu unterstützen, die Sie für Ihre Geschäftsabläufe benötigen.

## <a name="see-also"></a>Siehe auch

- [Neuigkeiten in Access 2013 für Entwickler](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


