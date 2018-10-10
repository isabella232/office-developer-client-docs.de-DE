---
title: SortColumn-Eigenschaft (RDS)
TOCTitle: SortColumn Property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85f2b031ac105bf900548e90eda6c0feb4b78f96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474903"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="a4b96-102">SortColumn-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="a4b96-102">SortColumn Property (RDS)</span></span>


<span data-ttu-id="a4b96-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4b96-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a4b96-104">Gibt die Spalte an, nach der die Datensätze sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a4b96-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4b96-105">Syntax</span></span>

<span data-ttu-id="a4b96-106">*DataControl*. SortColumn = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a4b96-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="a4b96-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4b96-107">Parameters</span></span>

  - <span data-ttu-id="a4b96-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="a4b96-108">*DataControl*</span></span>

  - <span data-ttu-id="a4b96-109">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4b96-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="a4b96-110">*String*</span><span class="sxs-lookup"><span data-stu-id="a4b96-110">*String*</span></span>

  - <span data-ttu-id="a4b96-111">Ein **String** -Wert, der den Namen oder Alias der Spalte angibt, nach der die Datensätze sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a4b96-111">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b96-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4b96-112">Remarks</span></span>

<span data-ttu-id="a4b96-p101">Die Eigenschaften **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md) -Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a4b96-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="a4b96-117">Um ein **Recordset-Objekt**zu sortieren, müssen Sie zuerst alle ausstehenden Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="a4b96-117">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="a4b96-118">Bei Verwendung der **RDS. DataControl**, können Sie die [SubmitChanges](submitchanges-method-rds.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4b96-118">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="a4b96-119">Beispielsweise, wenn Ihre **RDS. DataControl** ist mit dem Namen ADC1, würde der Code ADC1 werden. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="a4b96-119">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="a4b96-120">Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4b96-120">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="a4b96-121">Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a4b96-121">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="a4b96-122">Beispielsweise könnte der Code myRS.UpdateBatch oder.</span><span class="sxs-lookup"><span data-stu-id="a4b96-122">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="a4b96-123">Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4b96-123">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="a4b96-124">Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a4b96-124">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="a4b96-125">Beispielsweise könnte der Code myRS.UpdateBatch oder ADC1. Recordset.UpdateBatch lauten.</span><span class="sxs-lookup"><span data-stu-id="a4b96-125">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>

