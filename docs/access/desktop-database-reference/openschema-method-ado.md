---
title: OpenSchema-Methode (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 846d1c0f73ba4a17f166fffc7c1bb4682ad31d49
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921166"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="d90f5-102">OpenSchema-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="d90f5-102">OpenSchema method (ADO)</span></span>


<span data-ttu-id="d90f5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d90f5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="d90f5-104">Ruft Datenbank-Schemainformationen vom Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="d90f5-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="d90f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90f5-105">Syntax</span></span>

<span data-ttu-id="d90f5-106">**Legen Sie \*\*\* Recordset* = *Verbindung*. OpenSchema (* QueryType \* *Kriterien*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="d90f5-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="d90f5-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d90f5-107">Return values</span></span>

<span data-ttu-id="d90f5-108">Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, das Schemainformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d90f5-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="d90f5-109">Das **Recordset** -Objekt wird schreibgeschützt als statischer Cursor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d90f5-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="d90f5-110">Die *QueryType* bestimmt, welche Spalten im **Recordset-Objekt**angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d90f5-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="d90f5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d90f5-111">Parameters</span></span>

  - <span data-ttu-id="d90f5-112">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="d90f5-112">*QueryType*</span></span>

  - <span data-ttu-id="d90f5-113">Ein [SchemaEnum](schemaenum.md)-Wert, der den Typ der auszuführenden Schemaabfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="d90f5-113">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>

  - <span data-ttu-id="d90f5-114">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="d90f5-114">*Criteria*</span></span>

  - <span data-ttu-id="d90f5-115">Optional.</span><span class="sxs-lookup"><span data-stu-id="d90f5-115">Optional.</span></span> <span data-ttu-id="d90f5-116">Ein Array von Abfrage Einschränkungen für jede Option *QueryType* , wie in **SchemaEnum**aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d90f5-116">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>

  - <span data-ttu-id="d90f5-117">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="d90f5-117">*SchemaID*</span></span>

  - <span data-ttu-id="d90f5-118">Die GUID für eine vom Anbieter Schemaabfrage nicht vom OLE DB-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="d90f5-118">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="d90f5-119">Dieser Parameter ist erforderlich, wenn die *QueryType* auf **AdSchemaProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d90f5-119">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d90f5-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d90f5-120">Remarks</span></span>

<span data-ttu-id="d90f5-121">Die **OpenSchema** -Methode gibt selbsterläuternde Informationen zur Datenquelle zurück (z. B. welche Tabellen sich in der Datenquelle und welche Spalten sich in den Tabellen befinden sowie die unterstützten Datentypen).</span><span class="sxs-lookup"><span data-stu-id="d90f5-121">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="d90f5-122">Das *QueryType* -Argument ist eine GUID, der angibt, die Spalten (Schemas) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d90f5-122">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="d90f5-123">Die OLE DB-Spezifikation enthält eine vollständige Liste der Schemas.</span><span class="sxs-lookup"><span data-stu-id="d90f5-123">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="d90f5-p105">Das Argument *Criteria* beschränkt die Ergebnisse einer Schemaabfrage. *Criteria* gibt ein Array mit Werten an, die in einer entsprechenden Teilmenge der Spalten (auch als *Einschränkungsspalten* bezeichnet) im resultierenden **Recordset**-Objekt vorkommen müssen.</span><span class="sxs-lookup"><span data-stu-id="d90f5-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="d90f5-126">Die Konstante **AdSchemaProviderSpecific** wird für das Argument *QueryType* verwendet, wenn der Anbieter nicht den oben aufgeführten eigene nicht standardmäßige Schemaabfragen definiert.</span><span class="sxs-lookup"><span data-stu-id="d90f5-126">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="d90f5-127">Wenn diese Konstante verwendet wird, muss das Argument *SchemaID* übergeben Sie die GUID der Schemaabfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="d90f5-127">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="d90f5-128">*QueryType* auf **AdSchemaProviderSpecific** festgelegt ist, jedoch nicht *SchemaID* bereitgestellt wird, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d90f5-128">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="d90f5-129">Die Anbieter müssen nicht alle standardmäßigen OLE DB-Schemaabfragen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d90f5-129">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="d90f5-130">Gemäß der OLE DB-Spezifikation sind insbesondere nur **adSchemaTables**, **adSchemaColumns** und **adSchemaProviderTypes** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d90f5-130">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="d90f5-131">Der Anbieter ist jedoch nicht erforderlich, wenn für diese Schemaabfragen oben aufgeführten *Kriterien* Nebenbedingungen.</span><span class="sxs-lookup"><span data-stu-id="d90f5-131">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="d90f5-132">**Remote Data Service-Verwendung** **OpenSchema** -Methode ist nicht verfügbar für ein clientseitiges [Connection](connection-object-ado.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d90f5-132">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d90f5-p108">In Visual Basic können Spalten, die im von der <STRONG>OpenSchema</STRONG>-Methode für das <STRONG>Connection</STRONG>-Objekt zurückgegebene <STRONG>Recordset</STRONG>-Objekt eine 4-Byte-Ganzzahl ohne Vorzeichen (DBTYPE UI4) enthalten, nicht mit anderen Variablen verglichen werden. Weitere Informationen zu den OLE DB-Datentypen erhalten Sie in Chapter 13 und Appendix A der <EM>Microsoft OLE DB Programmer's Reference</EM>.</span><span class="sxs-lookup"><span data-stu-id="d90f5-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <STRONG>Recordset</STRONG> returned from the <STRONG>OpenSchema</STRONG> method on the <STRONG>Connection</STRONG> object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the <EM>Microsoft OLE DB Programmer's Reference</EM>.</span></span></P>


