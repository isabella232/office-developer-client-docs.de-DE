---
title: SortColumn-Eigenschaft (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bccd0eb536ec67937e8c3659b2ac62ef49a0bb3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924064"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="c656a-102">SortColumn-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="c656a-102">SortColumn property (RDS)</span></span>


<span data-ttu-id="c656a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c656a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c656a-104">Gibt die Spalte an, nach der die Datensätze sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c656a-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="c656a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c656a-105">Syntax</span></span>

<span data-ttu-id="c656a-106">*DataControl*. SortColumn = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c656a-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="c656a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c656a-107">Parameters</span></span>

  - <span data-ttu-id="c656a-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="c656a-108">*DataControl*</span></span>

  - <span data-ttu-id="c656a-109">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c656a-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="c656a-110">*String*</span><span class="sxs-lookup"><span data-stu-id="c656a-110">*String*</span></span>

  - <span data-ttu-id="c656a-111">Ein **String** -Wert, der den Namen oder Alias der Spalte angibt, nach der die Datensätze sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c656a-111">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>

## <a name="remarks"></a><span data-ttu-id="c656a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c656a-112">Remarks</span></span>

<span data-ttu-id="c656a-p101">Die Eigenschaften **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md) -Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c656a-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="c656a-117">Um ein **Recordset-Objekt**zu sortieren, müssen Sie zuerst alle ausstehenden Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="c656a-117">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="c656a-118">Bei Verwendung der **RDS. DataControl**, können Sie die [SubmitChanges](submitchanges-method-rds.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c656a-118">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="c656a-119">Beispielsweise, wenn Ihre **RDS. DataControl** ist mit dem Namen ADC1, würde der Code ADC1 werden. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="c656a-119">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="c656a-120">Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c656a-120">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="c656a-121">Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c656a-121">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="c656a-122">Beispielsweise könnte der Code myRS.UpdateBatch oder.</span><span class="sxs-lookup"><span data-stu-id="c656a-122">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="c656a-123">Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c656a-123">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="c656a-124">Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c656a-124">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="c656a-125">Beispielsweise könnte der Code myRS.UpdateBatch oder ADC1. Recordset.UpdateBatch lauten.</span><span class="sxs-lookup"><span data-stu-id="c656a-125">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>

