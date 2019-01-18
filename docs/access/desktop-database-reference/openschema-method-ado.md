---
title: OpenSchema-Methode (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701011"
---
# <a name="openschema-method-ado"></a>OpenSchema-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Ruft Datenbank-Schemainformationen vom Anbieter ab.

## <a name="syntax"></a>Syntax

**Legen Sie *** Recordset* = *Verbindung*. OpenSchema (* QueryType * *Kriterien*, *SchemaID*)

## <a name="return-values"></a>Rückgabewerte

Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, das Schemainformationen enthält. Das **Recordset** -Objekt wird schreibgeschützt als statischer Cursor geöffnet. Die *QueryType* bestimmt, welche Spalten im **Recordset-Objekt**angezeigt werden.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*QueryType* |Ein [SchemaEnum](schemaenum.md)-Wert, der den Typ der auszuführenden Schemaabfrage darstellt.|
|*Criteria* |Optional. Ein Array von Abfrage Einschränkungen für jede Option *QueryType* , wie in **SchemaEnum**aufgeführt.|
|*SchemaID* |Die GUID für eine vom Anbieter Schemaabfrage nicht vom OLE DB-Spezifikation definiert. Dieser Parameter ist erforderlich, wenn die *QueryType* auf **AdSchemaProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.|

## <a name="remarks"></a>Hinweise

Die **OpenSchema** -Methode gibt selbsterläuternde Informationen zur Datenquelle zurück (z. B. welche Tabellen sich in der Datenquelle und welche Spalten sich in den Tabellen befinden sowie die unterstützten Datentypen).

Das *QueryType* -Argument ist eine GUID, der angibt, die Spalten (Schemas) zurückgegeben. Die OLE DB-Spezifikation enthält eine vollständige Liste der Schemas.

Das Argument *Criteria* beschränkt die Ergebnisse einer Schemaabfrage. *Criteria* gibt ein Array mit Werten an, die in einer entsprechenden Teilmenge der Spalten (auch als *Einschränkungsspalten* bezeichnet) im resultierenden **Recordset**-Objekt vorkommen müssen.

Die Konstante **AdSchemaProviderSpecific** wird für das Argument *QueryType* verwendet, wenn der Anbieter nicht den oben aufgeführten eigene nicht standardmäßige Schemaabfragen definiert. Wenn diese Konstante verwendet wird, muss das Argument *SchemaID* übergeben Sie die GUID der Schemaabfrage ausführen. *QueryType* auf **AdSchemaProviderSpecific** festgelegt ist, jedoch nicht *SchemaID* bereitgestellt wird, wird ein Fehler ausgelöst.

Die Anbieter müssen nicht alle standardmäßigen OLE DB-Schemaabfragen unterstützen. Gemäß der OLE DB-Spezifikation sind insbesondere nur **adSchemaTables**, **adSchemaColumns** und **adSchemaProviderTypes** erforderlich. Der Anbieter ist jedoch nicht erforderlich, wenn für diese Schemaabfragen oben aufgeführten *Kriterien* Nebenbedingungen.

**Remote Data Service-Verwendung** **OpenSchema** -Methode ist nicht verfügbar für ein clientseitiges [Connection](connection-object-ado.md) -Objekt.

> [!NOTE]
> In Visual Basic können Spalten, die im von der **OpenSchema**-Methode für das **Connection**-Objekt zurückgegebene **Recordset**-Objekt eine 4-Byte-Ganzzahl ohne Vorzeichen (DBTYPE UI4) enthalten, nicht mit anderen Variablen verglichen werden. Weitere Informationen zu den OLE DB-Datentypen erhalten Sie in Chapter 13 und Appendix A der *Microsoft OLE DB Programmer's Reference*.


