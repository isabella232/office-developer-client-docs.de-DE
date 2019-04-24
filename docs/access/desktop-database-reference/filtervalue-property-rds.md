---
title: FilterValue-Eigenschaft (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70dca16f4a949cc6088779c1406e0c77cb477ba1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292405"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="4dd3c-102">FilterValue-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="4dd3c-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="4dd3c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dd3c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4dd3c-104">Gibt den Wert an, mit dem Datensätze gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4dd3c-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dd3c-105">Syntax</span></span>

<span data-ttu-id="4dd3c-106">*DataControl*. FilterValue = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="4dd3c-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="4dd3c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dd3c-107">Parameters</span></span>

|<span data-ttu-id="4dd3c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dd3c-108">Parameter</span></span>|<span data-ttu-id="4dd3c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dd3c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4dd3c-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="4dd3c-110">*DataControl*</span></span> |<span data-ttu-id="4dd3c-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4dd3c-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="4dd3c-112">*String*</span><span class="sxs-lookup"><span data-stu-id="4dd3c-112">*String*</span></span> |<span data-ttu-id="4dd3c-113">Ein **String** -Wert, der einen Datenwert darstellt, mit dem Datensätze gefiltert werden sollen (beispielsweise "Programmierer" oder 125).</span><span class="sxs-lookup"><span data-stu-id="4dd3c-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="4dd3c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dd3c-114">Remarks</span></span>

<span data-ttu-id="4dd3c-115">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache.</span><span class="sxs-lookup"><span data-stu-id="4dd3c-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="4dd3c-116">Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet.</span><span class="sxs-lookup"><span data-stu-id="4dd3c-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="4dd3c-117">Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt.</span><span class="sxs-lookup"><span data-stu-id="4dd3c-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="4dd3c-118">Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset**-Objekt durch ein aktualisierbares **Recordset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4dd3c-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="4dd3c-119">Nullwerte führen zu Konflikten der Datentypen.</span><span class="sxs-lookup"><span data-stu-id="4dd3c-119">Null values result in a type mismatch error.</span></span>

