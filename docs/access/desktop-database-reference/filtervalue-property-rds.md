---
title: FilterValue-Eigenschaft (RDS)
TOCTitle: FilterValue Property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 818a38c4c7d11442b1deb7ddeef72a828283c897
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887334"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="34eb5-102">FilterValue-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="34eb5-102">FilterValue Property (RDS)</span></span>


<span data-ttu-id="34eb5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34eb5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="34eb5-104">Gibt den Wert an, mit dem Datensätze gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34eb5-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="34eb5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34eb5-105">Syntax</span></span>

<span data-ttu-id="34eb5-106">*DataControl*. FilterValue = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="34eb5-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="34eb5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="34eb5-107">Parameters</span></span>

  - <span data-ttu-id="34eb5-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="34eb5-108">*DataControl*</span></span>

  - <span data-ttu-id="34eb5-109">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="34eb5-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="34eb5-110">*String*</span><span class="sxs-lookup"><span data-stu-id="34eb5-110">*String*</span></span>

  - <span data-ttu-id="34eb5-111">Ein **String** -Wert, der stellt ein der Datenwert mit dem gefiltert (z. B. 'Programmierer' oder 125) aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="34eb5-111">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>

## <a name="remarks"></a><span data-ttu-id="34eb5-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34eb5-112">Remarks</span></span>

<span data-ttu-id="34eb5-p101">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientseitigen Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="34eb5-p101">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="34eb5-117">Nullwerte führen zu Konflikten der Datentypen.</span><span class="sxs-lookup"><span data-stu-id="34eb5-117">Null values result in a type mismatch error.</span></span>

