---
title: Index. Clustered-Eigenschaft (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 060963dc47c933fee903cd9b220adb45c7f63df6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291852"
---
# <a name="indexclustered-property-dao"></a><span data-ttu-id="9d5dc-102">Index. Clustered-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="9d5dc-102">Index.Clustered property (DAO)</span></span>

<span data-ttu-id="9d5dc-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d5dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d5dc-p101">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ab ein **Index**-Objekt einen gruppierten Index für eine Tabelle darstellt (gilt nur für Microsoft Access-Arbeitsbereiche). **Boolean**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9d5dc-p101">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5dc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d5dc-106">Syntax</span></span>

<span data-ttu-id="9d5dc-107">*Ausdruck* . Gruppierten</span><span class="sxs-lookup"><span data-stu-id="9d5dc-107">*expression* .Clustered</span></span>

<span data-ttu-id="9d5dc-108">*Ausdruck* Ein Ausdruck, der ein **Index** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9d5dc-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5dc-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d5dc-109">Remarks</span></span>

<span data-ttu-id="9d5dc-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span><span class="sxs-lookup"><span data-stu-id="9d5dc-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="9d5dc-p102">Einige IISAM-Desktop-Datenbankenformate verwenden gruppierte Indizes. Ein gruppierter Index besteht aus einem oder mehreren Nichtschlüsselfeldern, die (in Kombination) alle Datensätze einer Tabelle in einer vordefinierten Reihenfolge anordnen. Ein gruppierter Index ermöglicht einen effizienten Zugriff auf Datensätze in einer Tabelle, in der Indexwerte möglicherweise nicht eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="9d5dc-p102">Some IISAM desktop database formats use clustered indexes. A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order. A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="9d5dc-114">Bei einem neuen, noch keiner Auflistung angefügten **Index**-Objekt ist die **Clustered**-Eigenschaft nicht schreibgeschützt. Bei einem vorhandenen **Index**-Objekt in einer **Indexes**-Auflistung ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9d5dc-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>

> [!NOTE]
> - <span data-ttu-id="9d5dc-115">Microsoft Access-Datenbanken ignorieren die **Clustered**-Eigenschaft, da das Microsoft Access-Datenbankmodul keine gruppierten Indizes unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9d5dc-115">Microsoft Access database engine databases ignore the **Clustered** property because the Microsoft Access database engine doesn't support clustered indexes.</span></span>
> - <span data-ttu-id="9d5dc-116">Bei ODBC-Datenquellen gibt die **Clustered** -Eigenschaft immer **false**zurück; Es wird nicht ermittelt, ob die ODBC-Datenquelle einen gruppierten Index hat.</span><span class="sxs-lookup"><span data-stu-id="9d5dc-116">For ODBC data sources, the **Clustered** property always returns **False**; it does not detect whether or not the ODBC data source has a clustered index.</span></span>


