---
title: OpenSchema-Methode (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a204f6e86a1c50be49400430f53dd99468668a9e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949999"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="39112-102">OpenSchema-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="39112-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="39112-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39112-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39112-104">Ruft Datenbank-Schemainformationen vom Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="39112-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="39112-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39112-105">Syntax</span></span>

<span data-ttu-id="39112-106">**Legen Sie \*\*\* Recordset* = *Verbindung*. OpenSchema (* QueryType \* *Kriterien*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="39112-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="39112-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="39112-107">Return values</span></span>

<span data-ttu-id="39112-108">Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, das Schemainformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="39112-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="39112-109">Das **Recordset** -Objekt wird schreibgeschützt als statischer Cursor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="39112-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="39112-110">Die *QueryType* bestimmt, welche Spalten im **Recordset-Objekt**angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="39112-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="39112-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39112-111">Parameters</span></span>

|<span data-ttu-id="39112-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="39112-112">Parameter</span></span>|<span data-ttu-id="39112-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39112-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="39112-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="39112-114">*QueryType*</span></span> |<span data-ttu-id="39112-115">Ein [SchemaEnum](schemaenum.md)-Wert, der den Typ der auszuführenden Schemaabfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="39112-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="39112-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="39112-116">*Criteria*</span></span> |<span data-ttu-id="39112-117">Optional.</span><span class="sxs-lookup"><span data-stu-id="39112-117">Optional.</span></span> <span data-ttu-id="39112-118">Ein Array von Abfrage Einschränkungen für jede Option *QueryType* , wie in **SchemaEnum**aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="39112-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="39112-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="39112-119">*SchemaID*</span></span> |<span data-ttu-id="39112-120">Die GUID für eine vom Anbieter Schemaabfrage nicht vom OLE DB-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="39112-120">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="39112-121">Dieser Parameter ist erforderlich, wenn die *QueryType* auf **AdSchemaProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="39112-121">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="39112-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39112-122">Remarks</span></span>

<span data-ttu-id="39112-123">Die **OpenSchema** -Methode gibt selbsterläuternde Informationen zur Datenquelle zurück (z. B. welche Tabellen sich in der Datenquelle und welche Spalten sich in den Tabellen befinden sowie die unterstützten Datentypen).</span><span class="sxs-lookup"><span data-stu-id="39112-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="39112-124">Das *QueryType* -Argument ist eine GUID, der angibt, die Spalten (Schemas) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39112-124">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="39112-125">Die OLE DB-Spezifikation enthält eine vollständige Liste der Schemas.</span><span class="sxs-lookup"><span data-stu-id="39112-125">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="39112-p105">Das Argument *Criteria* beschränkt die Ergebnisse einer Schemaabfrage. *Criteria* gibt ein Array mit Werten an, die in einer entsprechenden Teilmenge der Spalten (auch als *Einschränkungsspalten* bezeichnet) im resultierenden **Recordset**-Objekt vorkommen müssen.</span><span class="sxs-lookup"><span data-stu-id="39112-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="39112-128">Die Konstante **AdSchemaProviderSpecific** wird für das Argument *QueryType* verwendet, wenn der Anbieter nicht den oben aufgeführten eigene nicht standardmäßige Schemaabfragen definiert.</span><span class="sxs-lookup"><span data-stu-id="39112-128">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="39112-129">Wenn diese Konstante verwendet wird, muss das Argument *SchemaID* übergeben Sie die GUID der Schemaabfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="39112-129">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="39112-130">*QueryType* auf **AdSchemaProviderSpecific** festgelegt ist, jedoch nicht *SchemaID* bereitgestellt wird, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="39112-130">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="39112-131">Die Anbieter müssen nicht alle standardmäßigen OLE DB-Schemaabfragen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39112-131">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="39112-132">Gemäß der OLE DB-Spezifikation sind insbesondere nur **adSchemaTables**, **adSchemaColumns** und **adSchemaProviderTypes** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39112-132">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="39112-133">Der Anbieter ist jedoch nicht erforderlich, wenn für diese Schemaabfragen oben aufgeführten *Kriterien* Nebenbedingungen.</span><span class="sxs-lookup"><span data-stu-id="39112-133">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="39112-134">**Remote Data Service-Verwendung** **OpenSchema** -Methode ist nicht verfügbar für ein clientseitiges [Connection](connection-object-ado.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="39112-134">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="39112-p108">In Visual Basic können Spalten, die im von der <STRONG>OpenSchema</STRONG>-Methode für das <STRONG>Connection</STRONG>-Objekt zurückgegebene <STRONG>Recordset</STRONG>-Objekt eine 4-Byte-Ganzzahl ohne Vorzeichen (DBTYPE UI4) enthalten, nicht mit anderen Variablen verglichen werden. Weitere Informationen zu den OLE DB-Datentypen erhalten Sie in Chapter 13 und Appendix A der <EM>Microsoft OLE DB Programmer's Reference</EM>.</span><span class="sxs-lookup"><span data-stu-id="39112-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <STRONG>Recordset</STRONG> returned from the <STRONG>OpenSchema</STRONG> method on the <STRONG>Connection</STRONG> object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the <EM>Microsoft OLE DB Programmer's Reference</EM>.</span></span></P>


