---
title: SortDirection-Eigenschaft (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aef8b658bbe16c7b56c97900edb5a9c6bf1e8a0c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929643"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="2c70d-102">SortDirection-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="2c70d-102">SortDirection property (RDS)</span></span>


<span data-ttu-id="2c70d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c70d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="2c70d-104">Gibt eine aufsteigende oder absteigende Sortierreihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="2c70d-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c70d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c70d-105">Syntax</span></span>

<span data-ttu-id="2c70d-106">*DataControl*. SortDirection = *Wert*</span><span class="sxs-lookup"><span data-stu-id="2c70d-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="2c70d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c70d-107">Parameters</span></span>

  - <span data-ttu-id="2c70d-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="2c70d-108">*DataControl*</span></span>

  - <span data-ttu-id="2c70d-109">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2c70d-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="2c70d-110">*Wert*</span><span class="sxs-lookup"><span data-stu-id="2c70d-110">*Value*</span></span>

  - <span data-ttu-id="2c70d-p101">Ein **Boolean** -Wert, der eine aufsteigende Sortierreihenfolge angibt, wenn er auf **True** festgelegt ist. **False** gibt eine absteigende Reihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="2c70d-p101">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending. **False** indicates descending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c70d-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c70d-113">Remarks</span></span>

<span data-ttu-id="2c70d-p102">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die **Reset** -Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2c70d-p102">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

