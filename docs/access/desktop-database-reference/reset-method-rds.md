---
title: Reset-Methode (RDS - Access-desktop-Datenbank (engl.))
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e336a7ddf4db6e927c185b33a4138ab8dd5d5e9a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925968"
---
# <a name="reset-method-rds"></a><span data-ttu-id="0df02-102">Reset-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="0df02-102">Reset method (RDS)</span></span>


<span data-ttu-id="0df02-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0df02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0df02-104">Führt auf der Grundlage der angegebenen Eigenschaften zum Sortieren und Filtern die Sortierung und Filterung für ein clientseitiges **Recordset** -Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="0df02-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0df02-105">Syntax</span></span>

<span data-ttu-id="0df02-106">*DataControl*. Zurücksetzen (*Wert*)</span><span class="sxs-lookup"><span data-stu-id="0df02-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="0df02-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0df02-107">Parameters</span></span>

  - <span data-ttu-id="0df02-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="0df02-108">*DataControl*</span></span>

  - <span data-ttu-id="0df02-109">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0df02-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="0df02-110">*Value*</span><span class="sxs-lookup"><span data-stu-id="0df02-110">*value*</span></span>

  - <span data-ttu-id="0df02-p101">Optional. Ein **Boolean** -Wert, der **True** (Standardeinstellung) ist, wenn Sie das aktuelle "gefilterte" Rowset filtern möchten. **False** gibt an, dass Sie das urspüngliche Rowset filtern, wobei alle vorherigen Filteroptionen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0df02-p101">Optional. A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>

## <a name="remarks"></a><span data-ttu-id="0df02-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0df02-114">Remarks</span></span>

<span data-ttu-id="0df02-p102">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) bieten Funktionalitäten zum Filtern im clientseitigen Cache. Die Funktion zum Sortieren fordert aus einer Spalte Datensätze nach Werten an. Die Funktion zum Filtern zeigt auf der Grundlage eines Suchkriteriums eine Teilmenge von Datensätzen an, wobei das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache beibehalten wird. Die **Reset** -Methode führt das Kriterium aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0df02-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="0df02-p103">Wenn an den ursprünglichen Daten noch nicht übermittelte Änderungen vorgenommen wurde, schlägt die **Reset** -Methode fehl. Verwenden Sie zunächst die [SubmitChanges](submitchanges-method-rds.md)-Methode, um alle Änderungen in einem **Recordset** -Objekt mit Lese-/Schreibzugriff zu speichern, und sortieren oder filtern Sie die Datensätze anschließend mithilfe der **Reset** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0df02-p103">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail. First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="0df02-121">Wenn Sie mehrere Filter für Ihr Rowset ausführen möchten, können Sie die optionalen verwenden *boolesches* Argument mit der Methode **Zurücksetzen** .</span><span class="sxs-lookup"><span data-stu-id="0df02-121">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method.</span></span> <span data-ttu-id="0df02-122">Im folgenden Beispiel wird dargestellt, wie Sie dazu vorgehen:</span><span class="sxs-lookup"><span data-stu-id="0df02-122">The following example shows how to do this:</span></span>

