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
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="86626-102">Verwenden von ADO mit ADO MD</span><span class="sxs-lookup"><span data-stu-id="86626-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="86626-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86626-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86626-p101">ADO und ADO MD sind verwandte, aber separate Objektmodelle. ADO stellt Objekte zum Herstellen von Verbindungen mit Datenquellen, Ausführen von Befehlen, Abrufen von Tabellendaten und Schemametadaten in einem Tabellenformat sowie zum Anzeigen von Fehlerinformationen des Anbieters bereit. ADO MD stellt Objekte zum Abrufen multidimensionaler Daten und zum Anzeigen multidimensionaler Schemametadaten bereit.</span><span class="sxs-lookup"><span data-stu-id="86626-p101">ADO and ADO MD are related but separate object models. ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information. ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="86626-p102">Beim Verwenden eines MDPs können Sie auswählen, ob Sie ADO, ADO MD oder beide Bibliotheken mit Ihrer Anwendung verwenden. Durch Verweisen auf beide Bibliotheken innerhalb eines Projekts haben Sie vollständigen Zugriff auf die Funktionalität Ihres MDPs.</span><span class="sxs-lookup"><span data-stu-id="86626-p102">When working with an MDP you may choose to use ADO, ADO MD, or both with your application. By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="86626-109">Es ist es für Benutzer sinnvoll, eine vereinfachte, tabellarische Sicht eines multidimensionalen Datasets zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="86626-109">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset.</span></span> <span data-ttu-id="86626-110">Dies wird durch das Verwenden des ADO- [Recordset](recordset-object-ado.md)-Objekts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="86626-110">You can do this by using the ADO [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="86626-111">Geben Sie die Datenquelle für das [Cellset](cellset-object-ado-md.md)-Objekt als ***Source***-Parameter für die [Open](open-method-ado-recordset.md)-Methode eines **Recordset**Objekts an, statt als Quelle für ein ADO MD-**Cellset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="86626-111">Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="86626-112">Es kann auch nützlich sein, die Schemametadaten in einer tabellarischen Ansicht und nicht als Objekthierarchie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="86626-112">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</span></span> <span data-ttu-id="86626-113">Die ADO [](openschema-method-ado.md) -Methode OpenSchema für das [Connection](connection-object-ado.md) -Objekt ermöglicht es dem Benutzer, ein **Recordset** mit Schemainformationen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="86626-113">The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information.</span></span> <span data-ttu-id="86626-114">Der ***QueryType*** -Parameter der **OpenSchema** -Methode verfügt über mehrere [SchemaEnum](schemaenum.md) -Werte, die sich speziell auf MDPs beziehen.</span><span class="sxs-lookup"><span data-stu-id="86626-114">The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs.</span></span> <span data-ttu-id="86626-115">Diese Werte sind:</span><span class="sxs-lookup"><span data-stu-id="86626-115">These values are:</span></span>

  - <span data-ttu-id="86626-116">**adSchemaCubes**</span><span class="sxs-lookup"><span data-stu-id="86626-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="86626-117">**adSchemaDimensions**</span><span class="sxs-lookup"><span data-stu-id="86626-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="86626-118">**adSchemaHierarchies**</span><span class="sxs-lookup"><span data-stu-id="86626-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="86626-119">**adSchemaLevels**</span><span class="sxs-lookup"><span data-stu-id="86626-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="86626-120">**adSchemaMeasures**</span><span class="sxs-lookup"><span data-stu-id="86626-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="86626-121">**adSchemaMembers**</span><span class="sxs-lookup"><span data-stu-id="86626-121">**adSchemaMembers**</span></span>

<span data-ttu-id="86626-p105">Um ADO-Aufzählungswerte mit ADO MD-Eigenschaften oder -Methoden zu verwenden, muss das Projekt auf die ADO- und die ADO MD-Bibliothek verweisen. Sie können z. B. die ADO- **adState** -Aufzählungswerte mit der ADO MD- [State](state-property-ado-md.md)-Eigenschaft verwenden. Weitere Informationen zum Einrichten von Verweisen auf Bibliotheken finden Sie in der Dokumentation zu Ihrem Entwicklungstool.</span><span class="sxs-lookup"><span data-stu-id="86626-p105">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries. For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property. For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="86626-125">Weitere Informationen zu ADO-Objekten und -Methoden finden Sie in der [ADO-API-Referenz](ado-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="86626-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

