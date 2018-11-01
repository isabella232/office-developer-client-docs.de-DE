---
title: FilterColumn-Eigenschaft (RDS)
TOCTitle: FilterColumn Property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9cf03a2cbff06919981ac940f5b2962062a850c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877800"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="6f3eb-102">FilterColumn-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="6f3eb-102">FilterColumn Property (RDS)</span></span>


<span data-ttu-id="6f3eb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f3eb-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="6f3eb-104">Zeigt die Spalte an, für die die Filterkriterien ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="6f3eb-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f3eb-105">Syntax</span></span>

<span data-ttu-id="6f3eb-106">*DataControl*. FilterColumn = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="6f3eb-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="6f3eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f3eb-107">Parameters</span></span>

  - <span data-ttu-id="6f3eb-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="6f3eb-108">*DataControl*</span></span>

  - <span data-ttu-id="6f3eb-109">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6f3eb-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="6f3eb-110">*String*</span><span class="sxs-lookup"><span data-stu-id="6f3eb-110">*String*</span></span>

  - <span data-ttu-id="6f3eb-p101">Ein **String** -Wert, der die Spalte angibt, für die die Filterkriterien ausgewertet werden. Die Filterkriterien werden in der [FilterCriterion](filtercriterion-property-rds.md)-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="6f3eb-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f3eb-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f3eb-113">Remarks</span></span>

<span data-ttu-id="6f3eb-p102">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und **FilterColumn** ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md) -Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6f3eb-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

