---
title: Reset-Methode (RDS-Access-Desktop-Daten Bankreferenz)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306643"
---
# <a name="reset-method-rds"></a><span data-ttu-id="3b9e9-102">Reset-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="3b9e9-102">Reset method (RDS)</span></span>

<span data-ttu-id="3b9e9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b9e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b9e9-104">Führt auf der Grundlage der angegebenen Eigenschaften zum Sortieren und Filtern die Sortierung und Filterung für ein clientseitiges **Recordset** -Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="3b9e9-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b9e9-105">Syntax</span></span>

<span data-ttu-id="3b9e9-106">*DataControl*. Reset (*Wert*)</span><span class="sxs-lookup"><span data-stu-id="3b9e9-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="3b9e9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b9e9-107">Parameters</span></span>

|<span data-ttu-id="3b9e9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b9e9-108">Parameter</span></span>|<span data-ttu-id="3b9e9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b9e9-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3b9e9-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3b9e9-110">*DataControl*</span></span> |<span data-ttu-id="3b9e9-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b9e9-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="3b9e9-112">*Value*</span><span class="sxs-lookup"><span data-stu-id="3b9e9-112">*value*</span></span> |<span data-ttu-id="3b9e9-p101">Optional. Ein **Boolean** -Wert, der **True** (Standardeinstellung) ist, wenn Sie das aktuelle "gefilterte" Rowset filtern möchten. **False** gibt an, dass Sie das urspüngliche Rowset filtern, wobei alle vorherigen Filteroptionen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3b9e9-p101">Optional. A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3b9e9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b9e9-116">Remarks</span></span>

<span data-ttu-id="3b9e9-p102">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) bieten Funktionalitäten zum Filtern im clientseitigen Cache. Die Funktion zum Sortieren fordert aus einer Spalte Datensätze nach Werten an. Die Funktion zum Filtern zeigt auf der Grundlage eines Suchkriteriums eine Teilmenge von Datensätzen an, wobei das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache beibehalten wird. Die **Reset** -Methode führt das Kriterium aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3b9e9-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="3b9e9-p103">Wenn an den ursprünglichen Daten noch nicht übermittelte Änderungen vorgenommen wurde, schlägt die **Reset** -Methode fehl. Verwenden Sie zunächst die [SubmitChanges](submitchanges-method-rds.md)-Methode, um alle Änderungen in einem **Recordset** -Objekt mit Lese-/Schreibzugriff zu speichern, und sortieren oder filtern Sie die Datensätze anschließend mithilfe der **Reset** -Methode.</span><span class="sxs-lookup"><span data-stu-id="3b9e9-p103">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail. First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="3b9e9-p104">Wenn Sie mehrere Filter für Ihr Rowset ausführen möchten, können Sie das optionale Argument *Boolean* mit der **Reset**-Methode verwenden. Im folgenden Beispiel wird dargestellt, wie Sie dazu vorgehen:</span><span class="sxs-lookup"><span data-stu-id="3b9e9-p104">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method. The following example shows how to do this:</span></span>

