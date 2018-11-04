---
title: Reset-Methode (RDS - Access-desktop-Datenbank (engl.))
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cebb2f464b63106545ff5b27b1722b6417b9dbe1
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949943"
---
# <a name="reset-method-rds"></a><span data-ttu-id="20ce1-102">Reset-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="20ce1-102">Reset method (RDS)</span></span>

<span data-ttu-id="20ce1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20ce1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20ce1-104">Führt auf der Grundlage der angegebenen Eigenschaften zum Sortieren und Filtern die Sortierung und Filterung für ein clientseitiges **Recordset** -Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="20ce1-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ce1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20ce1-105">Syntax</span></span>

<span data-ttu-id="20ce1-106">*DataControl*. Zurücksetzen (*Wert*)</span><span class="sxs-lookup"><span data-stu-id="20ce1-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="20ce1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="20ce1-107">Parameters</span></span>

|<span data-ttu-id="20ce1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="20ce1-108">Parameter</span></span>|<span data-ttu-id="20ce1-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20ce1-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="20ce1-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="20ce1-110">*DataControl*</span></span> |<span data-ttu-id="20ce1-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="20ce1-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="20ce1-112">*Value*</span><span class="sxs-lookup"><span data-stu-id="20ce1-112">*value*</span></span> |<span data-ttu-id="20ce1-p101">Optional. Ein **Boolean** -Wert, der **True** (Standardeinstellung) ist, wenn Sie das aktuelle "gefilterte" Rowset filtern möchten. **False** gibt an, dass Sie das urspüngliche Rowset filtern, wobei alle vorherigen Filteroptionen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="20ce1-p101">Optional. A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="20ce1-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20ce1-116">Remarks</span></span>

<span data-ttu-id="20ce1-p102">Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) bieten Funktionalitäten zum Filtern im clientseitigen Cache. Die Funktion zum Sortieren fordert aus einer Spalte Datensätze nach Werten an. Die Funktion zum Filtern zeigt auf der Grundlage eines Suchkriteriums eine Teilmenge von Datensätzen an, wobei das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache beibehalten wird. Die **Reset** -Methode führt das Kriterium aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="20ce1-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="20ce1-p103">Wenn an den ursprünglichen Daten noch nicht übermittelte Änderungen vorgenommen wurde, schlägt die **Reset** -Methode fehl. Verwenden Sie zunächst die [SubmitChanges](submitchanges-method-rds.md)-Methode, um alle Änderungen in einem **Recordset** -Objekt mit Lese-/Schreibzugriff zu speichern, und sortieren oder filtern Sie die Datensätze anschließend mithilfe der **Reset** -Methode.</span><span class="sxs-lookup"><span data-stu-id="20ce1-p103">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail. First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="20ce1-123">Wenn Sie mehrere Filter für Ihr Rowset ausführen möchten, können Sie die optionalen verwenden *boolesches* Argument mit der Methode **Zurücksetzen** .</span><span class="sxs-lookup"><span data-stu-id="20ce1-123">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method.</span></span> <span data-ttu-id="20ce1-124">Im folgenden Beispiel wird dargestellt, wie Sie dazu vorgehen:</span><span class="sxs-lookup"><span data-stu-id="20ce1-124">The following example shows how to do this:</span></span>

