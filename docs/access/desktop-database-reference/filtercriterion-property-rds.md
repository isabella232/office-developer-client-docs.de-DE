---
title: FilterCriterion-Eigenschaft (RDS)
TOCTitle: FilterCriterion Property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5567265aba8d4490837ab69572a553d4aa1c1e1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869764"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="77cb8-102">FilterCriterion-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="77cb8-102">FilterCriterion Property (RDS)</span></span>


<span data-ttu-id="77cb8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77cb8-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="77cb8-104">Gibt den im Filterwert zu verwendenden Auswertungsoperator an.</span><span class="sxs-lookup"><span data-stu-id="77cb8-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="77cb8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77cb8-105">Syntax</span></span>

<span data-ttu-id="77cb8-106">*DataControl*. FilterCriterion = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="77cb8-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="77cb8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="77cb8-107">Parameters</span></span>

  - <span data-ttu-id="77cb8-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="77cb8-108">*DataControl*</span></span>

  - <span data-ttu-id="77cb8-109">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="77cb8-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="77cb8-110">*String*</span><span class="sxs-lookup"><span data-stu-id="77cb8-110">*String*</span></span>

  - <span data-ttu-id="77cb8-111">Ein **String** -Wert, der den Auswertungsoperator für [FilterValue](filtervalue-property-rds.md) zu den Datensätzen angibt.</span><span class="sxs-lookup"><span data-stu-id="77cb8-111">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="77cb8-112">Kann eine der folgenden sein: \<, \<=, \>, \>=, = oder \< \>.</span><span class="sxs-lookup"><span data-stu-id="77cb8-112">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>

## <a name="remarks"></a><span data-ttu-id="77cb8-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77cb8-113">Remarks</span></span>

<span data-ttu-id="77cb8-p102">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md) -Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="77cb8-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="77cb8-118">Die "\!=" Operator ist nicht gültig für **FilterCriterion**; Verwenden Sie stattdessen "\<\>".</span><span class="sxs-lookup"><span data-stu-id="77cb8-118">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="77cb8-p103">Wenn Sie die Filter- und Sortiereigenschaften festgelegt haben und die **Reset** -Methode aufrufen, wird das Rowset zuerst gefiltert und dann sortiert. Bei aufsteigender Sortierung befinden sich die NULL-Werte oben, bei absteigender Sortierung befinden sich die NULL-Werte unten (aufsteigend ist das Standardverhalten).</span><span class="sxs-lookup"><span data-stu-id="77cb8-p103">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted. For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>

