---
title: SortColumn-Eigenschaft (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54e6df1f2a94bd59f1e4cf9f9c0be77d785a3048
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709264"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="3e75c-102">SortColumn-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="3e75c-102">SortColumn property (RDS)</span></span>

<span data-ttu-id="3e75c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e75c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e75c-104">Gibt die Spalte an, nach der die Datensätze sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e75c-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e75c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e75c-105">Syntax</span></span>

<span data-ttu-id="3e75c-106">*DataControl*. SortColumn = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="3e75c-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="3e75c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e75c-107">Parameters</span></span>

|<span data-ttu-id="3e75c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e75c-108">Parameter</span></span>|<span data-ttu-id="3e75c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e75c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3e75c-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3e75c-110">*DataControl*</span></span> |<span data-ttu-id="3e75c-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3e75c-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="3e75c-112">*String*</span><span class="sxs-lookup"><span data-stu-id="3e75c-112">*String*</span></span> |<span data-ttu-id="3e75c-113">Ein **String** -Wert, der den Namen oder Alias der Spalte angibt, nach der die Datensätze sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e75c-113">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3e75c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e75c-114">Remarks</span></span>

<span data-ttu-id="3e75c-p101">Die Eigenschaften **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md) -Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3e75c-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="3e75c-119">Um ein **Recordset-Objekt**zu sortieren, müssen Sie zuerst alle ausstehenden Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="3e75c-119">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="3e75c-120">Bei Verwendung der **RDS. DataControl**, können Sie die [SubmitChanges](submitchanges-method-rds.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e75c-120">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="3e75c-121">Beispielsweise, wenn Ihre **RDS. DataControl** ist mit dem Namen ADC1, würde der Code ADC1 werden. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="3e75c-121">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="3e75c-122">Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e75c-122">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="3e75c-123">Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3e75c-123">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="3e75c-124">Beispielsweise könnte der Code myRS.UpdateBatch oder.</span><span class="sxs-lookup"><span data-stu-id="3e75c-124">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="3e75c-125">Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e75c-125">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="3e75c-126">Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3e75c-126">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="3e75c-127">Beispielsweise könnte der Code myRS.UpdateBatch oder ADC1. Recordset.UpdateBatch lauten.</span><span class="sxs-lookup"><span data-stu-id="3e75c-127">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>

