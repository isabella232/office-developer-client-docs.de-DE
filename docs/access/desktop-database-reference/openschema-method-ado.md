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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288336"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="75e10-102">OpenSchema-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="75e10-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="75e10-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75e10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75e10-104">Ruft Datenbank-Schemainformationen vom Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="75e10-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="75e10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75e10-105">Syntax</span></span>

<span data-ttu-id="75e10-106">**Set \* \* \* Recordset* = -*Verbindung*. OpenSchema (* QueryType \*, *Criteria*, *Schema*-Nr.)</span><span class="sxs-lookup"><span data-stu-id="75e10-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="75e10-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="75e10-107">Return values</span></span>

<span data-ttu-id="75e10-108">Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, das Schemainformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="75e10-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="75e10-109">Das **Recordset** -Objekt wird schreibgeschützt als statischer Cursor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="75e10-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="75e10-110">Mit dem *QueryType*-Parameter wird festgelegt, welche Spalten im **Recordset**-Objekt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="75e10-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="75e10-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="75e10-111">Parameters</span></span>

|<span data-ttu-id="75e10-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75e10-112">Parameter</span></span>|<span data-ttu-id="75e10-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75e10-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="75e10-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="75e10-114">*QueryType*</span></span> |<span data-ttu-id="75e10-115">Ein [SchemaEnum](schemaenum.md)-Wert, der den Typ der auszuführenden Schemaabfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="75e10-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="75e10-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="75e10-116">*Criteria*</span></span> |<span data-ttu-id="75e10-117">Optional.</span><span class="sxs-lookup"><span data-stu-id="75e10-117">Optional.</span></span> <span data-ttu-id="75e10-118">Ein Array mit Abfrageeinschränkungen für jede *QueryType*-Option (**SchemaEnum** aufgeführt).</span><span class="sxs-lookup"><span data-stu-id="75e10-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="75e10-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="75e10-119">*SchemaID*</span></span> |<span data-ttu-id="75e10-p103">GUID zur Abfrage eines Anbieterschemas, die nicht in der OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *QueryType* auf **adSchemaProviderSpecific** festgelegt ist. Andernfalls wird er nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="75e10-p103">The GUID for a provider-schema query not defined by the OLE DB specification. This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="75e10-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75e10-122">Remarks</span></span>

<span data-ttu-id="75e10-123">Die **OpenSchema**-Methode gibt selbsterläuternde Informationen zur Datenquelle zurück (z. B. welche Tabellen sich in der Datenquelle und welche Spalten sich in den Tabellen befinden sowie die unterstützten Datentypen).</span><span class="sxs-lookup"><span data-stu-id="75e10-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="75e10-p104">Das Argument *QueryType* ist eine GUID, die die zurückgegebenen Spalten (Schemas) angibt. Die OLE DB-Spezifikation enthält eine vollständige Liste der Schemas.</span><span class="sxs-lookup"><span data-stu-id="75e10-p104">The *QueryType* argument is a GUID that indicates the columns (schemas) returned. The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="75e10-p105">Das Argument *Criteria* beschränkt die Ergebnisse einer Schemaabfrage. *Criteria* gibt ein Array mit Werten an, die in einer entsprechenden Teilmenge der Spalten (auch als *Einschränkungsspalten* bezeichnet) im resultierenden **Recordset**-Objekt vorkommen müssen.</span><span class="sxs-lookup"><span data-stu-id="75e10-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="75e10-p106">Die Konstante **adSchemaProviderSpecific** wird für das Argument *QueryType* verwendet, wenn der Anbieter eigene nicht standardmäßige Schemaabfragen definiert, die nicht den oben aufgeführten entsprechen. Bei Verwendung dieser Konstante muss das Argument *SchemaID* die GUID der Schemaabfrage übergeben, damit diese ausgeführt werden kann. Wird *QueryType* auf **adSchemaProviderSpecific** festgelegt aber keine *SchemaID* angegeben, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="75e10-p106">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above. When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute. If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="75e10-p107">Die Anbieter müssen nicht alle standardmäßigen OLE DB-Schemaabfragen unterstützen. Gemäß der OLE DB-Spezifikation sind insbesondere nur **adSchemaTables**, **adSchemaColumns** und **adSchemaProviderTypes** erforderlich. Der Anbieter muss für diese Schemaabfragen jedoch nicht die oben aufgeführten *Criteria*-Einschränkungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="75e10-p107">Providers are not required to support all of the OLE DB standard schema queries. Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification. However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="75e10-134">**Remote Data Service-Verwendung** Die **OpenSchema** -Methode ist in einem clientseitigen [Connection](connection-object-ado.md) -Objekt nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="75e10-134">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="75e10-p108">In Visual Basic können Spalten, die im von der **OpenSchema**-Methode für das **Connection**-Objekt zurückgegebene **Recordset**-Objekt eine 4-Byte-Ganzzahl ohne Vorzeichen (DBTYPE UI4) enthalten, nicht mit anderen Variablen verglichen werden. Weitere Informationen zu den OLE DB-Datentypen erhalten Sie in Chapter 13 und Appendix A der *Microsoft OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="75e10-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


