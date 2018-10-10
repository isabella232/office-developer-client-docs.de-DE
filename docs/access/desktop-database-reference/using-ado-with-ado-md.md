---
title: Verwenden von ADO mit ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 492efdcef5f71daf50ac84eec5e61ef4ed07fd5a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474503"
---
# <a name="using-ado-with-ado-md"></a>Verwenden von ADO mit ADO MD


**Betrifft**: Access 2013 | Office 2013

ADO und ADO MD sind verwandte, aber separate Objektmodelle. ADO stellt Objekte zum Herstellen von Verbindungen mit Datenquellen, Ausführen von Befehlen, Abrufen von Tabellendaten und Schemametadaten in einem Tabellenformat sowie zum Anzeigen von Fehlerinformationen des Anbieters bereit. ADO MD stellt Objekte zum Abrufen multidimensionaler Daten und zum Anzeigen multidimensionaler Schemametadaten bereit.

Beim Verwenden eines MDPs können Sie auswählen, ob Sie ADO, ADO MD oder beide Bibliotheken mit Ihrer Anwendung verwenden. Durch Verweisen auf beide Bibliotheken innerhalb eines Projekts haben Sie vollständigen Zugriff auf die Funktionalität Ihres MDPs.

Es ist es für Benutzer sinnvoll, eine vereinfachte, tabellarische Sicht eines multidimensionalen Datasets zu verwenden. Dies wird durch das Verwenden des ADO- [Recordset](recordset-object-ado.md)-Objekts ermöglicht. Geben Sie die Datenquelle für Ihre [Zellmenge](cellset-object-ado-md.md) nicht als Quelle für ein ADO MD- **Zellmenge**, sondern als der ***Source*** -Parameter für die [Open](open-method-ado-recordset.md) -Methode eines **Recordset-Objekts**.

Sie können auch die Schemametadaten nicht als eine Hierarchie von Objekten, sondern in einer Tabellenansicht anzeigen hilfreich sein. Die ADO- [OpenSchema](openschema-method-ado.md) -Methode auf das [Connection](connection-object-ado.md) -Objekt ermöglicht es dem Benutzer zum Öffnen eines **Recordset-Objekts** , Schemainformationen enthält. Der ***QueryType*** -Parameter der **OpenSchema** -Methode hat mehrere [SchemaEnum](schemaenum.md) -Werte, die speziell MDPs betreffen. Diese Werte sind:

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Um ADO-Aufzählungswerte mit ADO MD-Eigenschaften oder -Methoden zu verwenden, muss das Projekt auf die ADO- und die ADO MD-Bibliothek verweisen. Sie können z. B. die ADO- **adState** -Aufzählungswerte mit der ADO MD- [State](state-property-ado-md.md)-Eigenschaft verwenden. Weitere Informationen zum Einrichten von Verweisen auf Bibliotheken finden Sie in der Dokumentation zu Ihrem Entwicklungstool.

Weitere Informationen zu ADO-Objekten und -Methoden finden Sie in der [ADO-API-Referenz](ado-api-reference.md).

