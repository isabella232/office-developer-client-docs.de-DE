---
title: Verwenden von ADO mit ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 80c87f57a96f98de704e3cfa9b7689a522e4a7af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312747"
---
# <a name="using-ado-with-ado-md"></a>Verwenden von ADO mit ADO MD


**Gilt für**: Access 2013, Office 2013

ADO und ADO MD sind verwandte, aber separate Objektmodelle. ADO stellt Objekte zum Herstellen von Verbindungen mit Datenquellen, Ausführen von Befehlen, Abrufen von Tabellendaten und Schemametadaten in einem Tabellenformat sowie zum Anzeigen von Fehlerinformationen des Anbieters bereit. ADO MD stellt Objekte zum Abrufen multidimensionaler Daten und zum Anzeigen multidimensionaler Schemametadaten bereit.

Beim Verwenden eines MDPs können Sie auswählen, ob Sie ADO, ADO MD oder beide Bibliotheken mit Ihrer Anwendung verwenden. Durch Verweisen auf beide Bibliotheken innerhalb eines Projekts haben Sie vollständigen Zugriff auf die Funktionalität Ihres MDPs.

Es ist es für Benutzer sinnvoll, eine vereinfachte, tabellarische Sicht eines multidimensionalen Datasets zu verwenden. Dies wird durch das Verwenden des ADO- [Recordset](recordset-object-ado.md)-Objekts ermöglicht. Geben Sie die Datenquelle für das [Cellset](cellset-object-ado-md.md)-Objekt als ***Source***-Parameter für die [Open](open-method-ado-recordset.md)-Methode eines **Recordset**Objekts an, statt als Quelle für ein ADO MD-**Cellset**-Objekt.

Es kann auch nützlich sein, die Schemametadaten in einer tabellarischen Ansicht und nicht als Objekthierarchie anzuzeigen. Die ADO [](openschema-method-ado.md) -Methode OpenSchema für das [Connection](connection-object-ado.md) -Objekt ermöglicht es dem Benutzer, ein **Recordset** mit Schemainformationen zu öffnen. Der ***QueryType*** -Parameter der **OpenSchema** -Methode verfügt über mehrere [SchemaEnum](schemaenum.md) -Werte, die sich speziell auf MDPs beziehen. Diese Werte sind:

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Um ADO-Aufzählungswerte mit ADO MD-Eigenschaften oder -Methoden zu verwenden, muss das Projekt auf die ADO- und die ADO MD-Bibliothek verweisen. Sie können z. B. die ADO- **adState** -Aufzählungswerte mit der ADO MD- [State](state-property-ado-md.md)-Eigenschaft verwenden. Weitere Informationen zum Einrichten von Verweisen auf Bibliotheken finden Sie in der Dokumentation zu Ihrem Entwicklungstool.

Weitere Informationen zu ADO-Objekten und -Methoden finden Sie in der [ADO-API-Referenz](ado-api-reference.md).

