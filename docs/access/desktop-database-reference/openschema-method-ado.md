---
title: OpenSchema-Methode (ADO)
TOCTitle: OpenSchema Method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba0cdb22ee9234e935635038b86ac792dd5753cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475907"
---
# <a name="openschema-method-ado"></a>OpenSchema-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013


Ruft Datenbank-Schemainformationen vom Anbieter ab.

## <a name="syntax"></a>Syntax

**Legen Sie *** Recordset* = *Verbindung*. OpenSchema (* QueryType * *Kriterien*, *SchemaID*)

## <a name="return-values"></a>Rückgabewert

Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, das Schemainformationen enthält. Das **Recordset** -Objekt wird schreibgeschützt als statischer Cursor geöffnet. Die *QueryType* bestimmt, welche Spalten im **Recordset-Objekt**angezeigt werden.

## <a name="parameters"></a>Parameter

  - *QueryType*

  - Ein [SchemaEnum](schemaenum.md)-Wert, der den Typ der auszuführenden Schemaabfrage darstellt.

  - *Criteria*

  - Optional. Ein Array von Abfrage Einschränkungen für jede Option *QueryType* , wie in **SchemaEnum**aufgeführt.

  - *SchemaID*

  - Die GUID für eine vom Anbieter Schemaabfrage nicht vom OLE DB-Spezifikation definiert. Dieser Parameter ist erforderlich, wenn die *QueryType* auf **AdSchemaProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.

## <a name="remarks"></a>Hinweise

Die **OpenSchema** -Methode gibt selbsterläuternde Informationen zur Datenquelle zurück (z. B. welche Tabellen sich in der Datenquelle und welche Spalten sich in den Tabellen befinden sowie die unterstützten Datentypen).

Das *QueryType* -Argument ist eine GUID, der angibt, die Spalten (Schemas) zurückgegeben. Die OLE DB-Spezifikation enthält eine vollständige Liste der Schemas.

Das Argument *Criteria* beschränkt die Ergebnisse einer Schemaabfrage. *Criteria* gibt ein Array mit Werten an, die in einer entsprechenden Teilmenge der Spalten (auch als *Einschränkungsspalten* bezeichnet) im resultierenden **Recordset**-Objekt vorkommen müssen.

Die Konstante **AdSchemaProviderSpecific** wird für das Argument *QueryType* verwendet, wenn der Anbieter nicht den oben aufgeführten eigene nicht standardmäßige Schemaabfragen definiert. Wenn diese Konstante verwendet wird, muss das Argument *SchemaID* übergeben Sie die GUID der Schemaabfrage ausführen. *QueryType* auf **AdSchemaProviderSpecific** festgelegt ist, jedoch nicht *SchemaID* bereitgestellt wird, wird ein Fehler ausgelöst.

Die Anbieter müssen nicht alle standardmäßigen OLE DB-Schemaabfragen unterstützen. Gemäß der OLE DB-Spezifikation sind insbesondere nur **adSchemaTables**, **adSchemaColumns** und **adSchemaProviderTypes** erforderlich. Der Anbieter ist jedoch nicht erforderlich, wenn für diese Schemaabfragen oben aufgeführten *Kriterien* Nebenbedingungen.

**Remote Data Service-Verwendung** **OpenSchema** -Methode ist nicht verfügbar für ein clientseitiges [Connection](connection-object-ado.md) -Objekt.


> [!NOTE]
> <P>In Visual Basic können Spalten, die im von der <STRONG>OpenSchema</STRONG>-Methode für das <STRONG>Connection</STRONG>-Objekt zurückgegebene <STRONG>Recordset</STRONG>-Objekt eine 4-Byte-Ganzzahl ohne Vorzeichen (DBTYPE UI4) enthalten, nicht mit anderen Variablen verglichen werden. Weitere Informationen zu den OLE DB-Datentypen erhalten Sie in Chapter 13 und Appendix A der <EM>Microsoft OLE DB Programmer's Reference</EM>.</P>


