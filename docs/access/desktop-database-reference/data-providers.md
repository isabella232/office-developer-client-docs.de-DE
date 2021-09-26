---
title: Datenanbieter (Access-Desktopdatenbankreferenz)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ecc26839906a4be89a76d8f42e9f0431e36851e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589799"
---
# <a name="data-providers"></a>Datenanbieter


**Gilt für**: Access 2013, Office 2013

Datenprovider stellen unterschiedliche Datenquellen wie SQL-Datenbanken, indiziert-sequenzielle Dateien, Kalkulationstabellen, Dokumentspeicher und E-Mail-Dateien dar. Datenprovider machen Daten mithilfe eines so genannten Rowsets einheitlich verfügbar.

ADO ist leistungsfähig und flexibel, weil damit auf mehrere verschiedene Datenprovider zugegriffen und dennoch dasselbe Programmiermodell verfügbar gemacht werden kann, unabhängig von den jeweiligen Features eines bestimmten Datenproviders. Da sich jedoch jeder Datenprovider unterscheidet, hängt die Interaktionsweise der Anwendung mit ADO vom jeweiligen Datenprovider ab.

Beispielsweise unterscheiden sich die Funktionen und Features des OLE DB-Anbieters für SQL Server, der für den Zugriff auf Microsoft SQL Server Datenbanken verwendet wird, erheblich von denen des Microsoft OLE DB-Anbieters für Internet Publishing, der für den Zugriff auf Dateispeicher auf einem Webserver verwendet wird.

