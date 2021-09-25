---
title: OpenSchema-Methode (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0a51fbff30d9a7fdf47d21a7f5842d591db0a67d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565205"
---
# <a name="openschema-method-ado"></a>OpenSchema-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Ruft Datenbank-Schemainformationen vom Anbieter ab.

## <a name="syntax"></a>Syntax

**Set**_recordset_  =  *connection*. OpenSchema (*QueryType*, *Criteria*, *SchemaID*)

## <a name="return-values"></a>Rückgabewerte

Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, das Schemainformationen enthält. Das **Recordset** -Objekt wird schreibgeschützt als statischer Cursor geöffnet. Mit dem *QueryType*-Parameter wird festgelegt, welche Spalten im **Recordset**-Objekt angezeigt werden.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*QueryType* |Ein [SchemaEnum](schemaenum.md)-Wert, der den Typ der auszuführenden Schemaabfrage darstellt.|
|*Criteria* |Optional. Ein Array mit Abfrageeinschränkungen für jede *QueryType*-Option (**SchemaEnum** aufgeführt).|
|*SchemaID* |GUID zur Abfrage eines Anbieterschemas, die nicht in der OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *QueryType* auf **adSchemaProviderSpecific** festgelegt ist. Andernfalls wird er nicht verwendet.|

## <a name="remarks"></a>HinwBemerkungeneise

Die **OpenSchema**-Methode gibt selbsterläuternde Informationen zur Datenquelle zurück (z. B. welche Tabellen sich in der Datenquelle und welche Spalten sich in den Tabellen befinden sowie die unterstützten Datentypen).

Das Argument *QueryType* ist eine GUID, die die zurückgegebenen Spalten (Schemas) angibt. Die OLE DB-Spezifikation enthält eine vollständige Liste der Schemas.

Das Argument *Criteria* beschränkt die Ergebnisse einer Schemaabfrage. *Criteria* gibt ein Array mit Werten an, die in einer entsprechenden Teilmenge der Spalten (auch als *Einschränkungsspalten* bezeichnet) im resultierenden **Recordset**-Objekt vorkommen müssen.

Die Konstante **adSchemaProviderSpecific** wird für das Argument *QueryType* verwendet, wenn der Anbieter eigene nicht standardmäßige Schemaabfragen definiert, die nicht den oben aufgeführten entsprechen. Bei Verwendung dieser Konstante muss das Argument *SchemaID* die GUID der Schemaabfrage übergeben, damit diese ausgeführt werden kann. Wird *QueryType* auf **adSchemaProviderSpecific** festgelegt aber keine *SchemaID* angegeben, tritt ein Fehler auf.

Die Anbieter müssen nicht alle standardmäßigen OLE DB-Schemaabfragen unterstützen. Gemäß der OLE DB-Spezifikation sind insbesondere nur **adSchemaTables**, **adSchemaColumns** und **adSchemaProviderTypes** erforderlich. Der Anbieter muss für diese Schemaabfragen jedoch nicht die oben aufgeführten *Criteria*-Einschränkungen unterstützen.

**Remote data service usage** Die **OpenSchema-Methode** ist für ein clientseitiges [Connection-Objekt](connection-object-ado.md) nicht verfügbar.

> [!NOTE]
> In Visual Basic können Spalten, die im von der **OpenSchema**-Methode für das **Connection**-Objekt zurückgegebene **Recordset**-Objekt eine 4-Byte-Ganzzahl ohne Vorzeichen (DBTYPE UI4) enthalten, nicht mit anderen Variablen verglichen werden. Weitere Informationen zu den OLE DB-Datentypen erhalten Sie in Chapter 13 und Appendix A der *Microsoft OLE DB Programmer's Reference*.


