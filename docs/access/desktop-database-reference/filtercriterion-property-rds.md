---
title: FilterCriterion-Eigenschaft (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65541e8f64c5a019679252246edbe8027130c4ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292426"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="15ce4-102">FilterCriterion-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="15ce4-102">FilterCriterion property (RDS)</span></span>

<span data-ttu-id="15ce4-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15ce4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15ce4-104">Gibt den im Filterwert zu verwendenden Auswertungsoperator an.</span><span class="sxs-lookup"><span data-stu-id="15ce4-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ce4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15ce4-105">Syntax</span></span>

<span data-ttu-id="15ce4-106">*DataControl*. FilterCriterion = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="15ce4-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="15ce4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="15ce4-107">Parameters</span></span>

|<span data-ttu-id="15ce4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="15ce4-108">Parameter</span></span>|<span data-ttu-id="15ce4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15ce4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="15ce4-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="15ce4-110">*DataControl*</span></span> |<span data-ttu-id="15ce4-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="15ce4-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="15ce4-112">*String*</span><span class="sxs-lookup"><span data-stu-id="15ce4-112">*String*</span></span> |<span data-ttu-id="15ce4-113">Ein **String** -Wert, der den Auswertungsoperator für [FilterValue](filtervalue-property-rds.md) zu den Datensätzen angibt.</span><span class="sxs-lookup"><span data-stu-id="15ce4-113">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="15ce4-114">Kann \<eine der folgenden sein:, \<=, \>, \>=, =, oder. \< \></span><span class="sxs-lookup"><span data-stu-id="15ce4-114">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>|

## <a name="remarks"></a><span data-ttu-id="15ce4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15ce4-115">Remarks</span></span>

<span data-ttu-id="15ce4-p102">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset**-Objekt durch ein aktualisierbares **Recordset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="15ce4-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="15ce4-120">Der Operator\!"=" ist für **FilterCriterion**ungültig; Verwenden Sie stattdessen "\<\>".</span><span class="sxs-lookup"><span data-stu-id="15ce4-120">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="15ce4-p103">Wenn Sie die Filter- und Sortiereigenschaften festgelegt haben und die **Reset** -Methode aufrufen, wird das Rowset zuerst gefiltert und dann sortiert. Bei aufsteigender Sortierung befinden sich die NULL-Werte oben, bei absteigender Sortierung befinden sich die NULL-Werte unten (aufsteigend ist das Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="15ce4-p103">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted. For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>

