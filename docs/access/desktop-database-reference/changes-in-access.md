---
title: Änderungen in Access (Zugriff PC-Datenbank-Referenz)
TOCTitle: Changes in Access
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3363d1bc3e9b2157ce8d7855a588b98a819246e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475116"
---
# <a name="changes-in-access"></a>Änderungen in Access

**Gilt für:** Access 2013 | Office 2013

Access umfasst keine Unterstützung für Access-Datenprojekte (ADPs). In Access wird erstmals ein neuer Anwendungstyp verwendet, der es Ihnen ermöglicht, eine webbasierte Access-App zu erstellen. Mithilfe dieses Anwendungstyps können Sie webbasierte Anwendungen erstellen, die die Leistungsfähigkeit von SQL Server lokal oder in der Cloud nutzen.

In Access wird erstmals ein neuer Anwendungstyp verwendet, der es Ihnen ermöglicht, eine webbasierte AccessApp zu erstellen. Mithilfe dieses Anwendungstyps können Sie webbasierte Anwendungen erstellen, die die Leistungsfähigkeit von SQL Server lokal oder in der Cloud nutzen.

In einer Access-App auf SharePoint Server beim Erstellen einer Tabelle, einer Abfrage oder eines Datenmakros im Access-Client, in dem Sie Tabellen, Ansichten oder Trigger in einer SQL Server-Datenbank erstellen. Mit dem Access-Client können Sie Ihre Datenbank in anderen Anwendungen öffnen, die eine Verbindung mit SQL Server herstellen. So können Sie Ihre Daten freigeben oder Daten aus anderen Systemen in Ihre Access-App laden.

Mit Office 365 und Access können Sie Anwendungen erstellen, die Ihre Benutzer erreichen, ohne dass Sie sich Gedanken um Probleme bei Bereitstellung und Installation oder um die Kompatibilität von Betriebssystemen machen müssen. Erstellen Sie Ihre App an einem Ort, und geben Sie sie mit den leistungsstarken Funktionen von SQL Azure und SQL Server im Web frei.

[SQL Azure](https://msdn.microsoft.com/library/azure/ee336279.aspx), die Cloudversion von SQL Server, bietet keine Unterstützung für Features, die für die Funktion von Access-Datenprojekten (ADPs) erforderlich sind. Für die Unterstützung von ADPs in SQL Azure, Access wären erhebliche Änderungen nötig.

Aus diesen Gründen unterstützt Access keine ADPs. ADPs waren ein hervorragendes Tool für die Arbeit mit SQL Server in einer lokalen Umgebung, jedoch hat sich seit der Einführung von ADPs in Access 2000 viel geändert. Die Benutzer erwarten nun, dass ihnen ihre Datenbank standortunabhängig zur Verfügung stehen.

## <a name="adp-support-and-the-future"></a>ADP-Unterstützung und die Zukunft

ADPs funktionieren nach wie vor in früheren Versionen von Access. Sie können weiterhin Ihre ADP-Anwendungen entwickeln, und wir werden weiterhin Support für frühere Versionen von Access im Rahmen des standardmäßigen [Support Lifecycle](https://support.microsoft.com/gp/lifeselect) bieten. Es wird kein Update älterer Versionen von Access geben, um neue Versionen von SQL Server oder SQL Azure zu unterstützen. Daher kann es zu Problemen kommen, wenn Sie SQL Server 2012 oder höher mit Ihren ADPs verwenden. ADPs unterstützen weiterhin SQL 2008 R2 und frühere Versionen.

Für die Zukunft haben ADP-Entwickler verschiedene Möglichkeiten:

- **Konvertieren in eine Access-app** – Using Access können Sie die Tabellen in einer neuen Access-app importieren und Formulare für die Anwendung automatisch für Sie erstellt werden. Sie können den Funktionsumfang der von Access erstellten Basisformulare erweitern, und Benutzer können Ihre Anwendung im Web verwenden. Zwar stehen einige der Funktionen, die Sie in ADPs verwenden, derzeit möglicherweise nicht zur Verfügung, Sie können jedoch davon ausgehen, dass sich Microsoft weiterhin intensiv mit Produktverbesserungen für diesen Anwendungstyps beschäftigen wird.

- **Konvertieren in eine verknüpfte desktop-Datenbank** – Access weiterhin erstellen Desktopdatenbanken in das ACCDB-Dateiformat unterstützt. Sie können Ihre Anwendung einschließlich aller vorhandenen Formulare und Berichte in das ACCDB-Format konvertieren und die Daten in SQL Server belassen. Mithilfe verknüpfter Tabellen können Sie eine Verknüpfung mit der SQL Server-Datenbank herstellen, und Ihre Anwendung arbeitet weiterhin mit denselben Daten.

- **Erstellen einer Hybrid-Anwendung** – Wenn die Anwendung groß ist und Sie nicht alles gleichzeitig konvertieren möchten, können Sie Ihre Daten in einer Access-app und Verknüpfen mit der SQL Server-Datenbank von einer ACCDB importieren. Dies ermöglicht Ihnen eine schrittweise Migration, bei der Sie Formulare und Funktionen nach und nach zur Ihrer Access-App hinzufügen und dabei Ihre Clientanwendung als eine ACCDB-Datei verwalten, deren Tabellen mit der SQL Server-Datenbank hinter der Access-App verknüpft sind.

- **Durchführen eines Upgrades auf .NET Framework** – die Anwendung möglicherweise komplexe genug sind, die zu berücksichtigen sind, verschieben in eine professionelle Entwicklungsplattform wie .NET Framework. SQL Server soll die vorhandene Datenbankinfrastruktur können, die Sie bereits erstellt haben, und erweitern die Funktionalität Ihrer Anwendung ohne erheblich umschreiben des Codes, zu erleichtern.

## <a name="conclusion"></a>Schlussbemerkung

Access ist dafür konzipiert, Datenbanken mit der Cloud zu verbinden, indem auf SharePoint Server- und SQL Server-Technologien aufgebaut wird, und die Arbeit mit Office 365 zu erleichtern. Access wurde entwickelt, um Sie beim Erstellen und Freigeben datenintensiver Geschäfts-Apps zu unterstützen, die Sie für Ihre Geschäftsabläufe benötigen.

## <a name="see-also"></a>Siehe auch

- [Neuigkeiten in Access für Entwickler](https://msdn.microsoft.com/library/jj250134\(v=office.15\))
- [Microsoft Support Lifecycle](https://support.microsoft.com/lifecycle/)
- [Microsoft Azure SQL-Datenbank](https://msdn.microsoft.com/library/azure/ee336279.aspx)

