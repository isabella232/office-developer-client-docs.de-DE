---
title: FilterColumn-Eigenschaft (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1af06abc634d0ef1984d325722aac814214b28d
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949460"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="12002-102">FilterColumn-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="12002-102">FilterColumn property (RDS)</span></span>

<span data-ttu-id="12002-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12002-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12002-104">Zeigt die Spalte an, für die die Filterkriterien ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="12002-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="12002-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12002-105">Syntax</span></span>

<span data-ttu-id="12002-106">*DataControl*. FilterColumn = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="12002-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="12002-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="12002-107">Parameters</span></span>

|<span data-ttu-id="12002-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12002-108">Parameter</span></span>|<span data-ttu-id="12002-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12002-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="12002-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="12002-110">*DataControl*</span></span> |<span data-ttu-id="12002-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="12002-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="12002-112">*String*</span><span class="sxs-lookup"><span data-stu-id="12002-112">*String*</span></span> |<span data-ttu-id="12002-p101">Ein **String** -Wert, der die Spalte angibt, für die die Filterkriterien ausgewertet werden. Die Filterkriterien werden in der [FilterCriterion](filtercriterion-property-rds.md)-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="12002-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="12002-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="12002-115">Remarks</span></span>

<span data-ttu-id="12002-116">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und **FilterColumn** ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache.</span><span class="sxs-lookup"><span data-stu-id="12002-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="12002-117">Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet.</span><span class="sxs-lookup"><span data-stu-id="12002-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="12002-118">Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt.</span><span class="sxs-lookup"><span data-stu-id="12002-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> 

<span data-ttu-id="12002-119">Die [Reset](reset-method-rds.md) -Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="12002-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

