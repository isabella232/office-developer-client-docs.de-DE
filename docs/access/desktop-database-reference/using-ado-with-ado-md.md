---
title: Verwenden von ADO mit ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5d74f4d587462290fa99bb2524b4dc264af9d591
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588875"
---
# <a name="using-ado-with-ado-md"></a>Verwenden von ADO mit ADO MD


**Gilt für**: Access 2013, Office 2013

ADO und ADO MD sind verwandte, aber separate Objektmodelle. ADO stellt Objekte zum Herstellen von Verbindungen mit Datenquellen, Ausführen von Befehlen, Abrufen von Tabellendaten und Schemametadaten in einem Tabellenformat sowie zum Anzeigen von Fehlerinformationen des Anbieters bereit. ADO MD stellt Objekte zum Abrufen multidimensionaler Daten und zum Anzeigen multidimensionaler Schemametadaten bereit.

Beim Verwenden eines MDPs können Sie auswählen, ob Sie ADO, ADO MD oder beide Bibliotheken mit Ihrer Anwendung verwenden. Durch Verweisen auf beide Bibliotheken innerhalb eines Projekts haben Sie vollständigen Zugriff auf die Funktionalität Ihres MDPs.

Es ist es für Benutzer sinnvoll, eine vereinfachte, tabellarische Sicht eines multidimensionalen Datasets zu verwenden. Dies wird durch das Verwenden des ADO- [Recordset](recordset-object-ado.md)-Objekts ermöglicht. Geben Sie die Quelle für Ihr [Cellset](cellset-object-ado-md.md) als ***Source** _ -Parameter für die [Open-Methode](open-method-ado-recordset.md) eines _*Recordset**-Objekts an, anstatt als Quelle für ein ADO MD **Cellset -Objekt.**

Es kann auch hilfreich sein, die Schemametadaten in einer Tabellenansicht anstatt als Hierarchie von Objekten anzuzeigen. Die ADO [OpenSchema-Methode](openschema-method-ado.md) für das [Connection-Objekt](connection-object-ado.md) ermöglicht es dem Benutzer, ein **Recordset** mit Schemainformationen zu öffnen. Der **_QueryType_*_-Parameter der* _OpenSchema-Methode** weist mehrere [SchemaEnum-Werte](schemaenum.md) auf, die sich speziell auf MDPs beziehen. Die folgenden Werte sind:

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Um ADO-Aufzählungswerte mit ADO MD-Eigenschaften oder -Methoden zu verwenden, muss das Projekt auf die ADO- und die ADO MD-Bibliothek verweisen. Sie können z. B. die ADO- **adState** -Aufzählungswerte mit der ADO MD- [State](state-property-ado-md.md)-Eigenschaft verwenden. Weitere Informationen zum Einrichten von Verweisen auf Bibliotheken finden Sie in der Dokumentation zu Ihrem Entwicklungstool.

Weitere Informationen zu ADO-Objekten und -Methoden finden Sie in der [ADO-API-Referenz](ado-api-reference.md).

