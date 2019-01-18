---
title: Datenanbieter (Access PC-Datenbank-Referenz)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 46d9cf80bfdd15f48d876fe63a617c9b30931fd3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705897"
---
# <a name="data-providers"></a>Datenanbieter


**Betrifft**: Access 2013, Office 2013

Datenprovider stellen unterschiedliche Datenquellen wie SQL-Datenbanken, indiziert-sequenzielle Dateien, Kalkulationstabellen, Dokumentspeicher und E-Mail-Dateien dar. Datenprovider machen Daten mithilfe eines so genannten Rowsets einheitlich verfügbar.

ADO ist leistungsfähig und flexibel, weil damit auf mehrere verschiedene Datenprovider zugegriffen und dennoch dasselbe Programmiermodell verfügbar gemacht werden kann, unabhängig von den jeweiligen Features eines bestimmten Datenproviders. Da sich jedoch jeder Datenprovider unterscheidet, hängt die Interaktionsweise der Anwendung mit ADO vom jeweiligen Datenprovider ab.

Beispielsweise sind die Funktionen und Features von den OLE DB-Anbieter für SQL Server, die Zugriff auf Microsoft SQL Server-Datenbanken verwendet wird, erheblich sich von denen des Microsoft OLE DB-Anbieter für Internet Publishing, mit dem Datei Zugriff auf verwendet wird speichert auf einem Webserver.

