---
title: Datenanbieter (Access Desktop Database Reference)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 46d9cf80bfdd15f48d876fe63a617c9b30931fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295065"
---
# <a name="data-providers"></a>Datenanbieter


**Gilt für**: Access 2013, Office 2013

Datenprovider stellen unterschiedliche Datenquellen wie SQL-Datenbanken, indiziert-sequenzielle Dateien, Kalkulationstabellen, Dokumentspeicher und E-Mail-Dateien dar. Datenprovider machen Daten mithilfe eines so genannten Rowsets einheitlich verfügbar.

ADO ist leistungsfähig und flexibel, weil damit auf mehrere verschiedene Datenprovider zugegriffen und dennoch dasselbe Programmiermodell verfügbar gemacht werden kann, unabhängig von den jeweiligen Features eines bestimmten Datenproviders. Da sich jedoch jeder Datenprovider unterscheidet, hängt die Interaktionsweise der Anwendung mit ADO vom jeweiligen Datenprovider ab.

Beispielsweise unterscheiden sich die Funktionen und Funktionen des OLE DB-Anbieters für SQL Server, der für den Zugriff auf Microsoft SQL Server-Datenbanken verwendet wird, erheblich von denen des Microsoft OLE DB-Anbieters für Internet Publishing, der für den Zugriff auf die Datei verwendet wird. Speicher auf einem Webserver.

