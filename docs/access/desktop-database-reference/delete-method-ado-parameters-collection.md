---
title: Delete-Methode (Parameters-Auflistung in ADO)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e519d40a081b132cd09030e9ba97de9e8987af99
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881958"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="dfbf4-102">Delete-Methode (Parameters-Auflistung in ADO)</span><span class="sxs-lookup"><span data-stu-id="dfbf4-102">Delete Method (ADO Parameters Collection)</span></span>


<span data-ttu-id="dfbf4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfbf4-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="dfbf4-104">Ein Objekt wird aus der [Parameters](parameters-collection-ado.md)-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dfbf4-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbf4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfbf4-105">Syntax</span></span>

<span data-ttu-id="dfbf4-106">*Parameter*. *Index* löschen</span><span class="sxs-lookup"><span data-stu-id="dfbf4-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="dfbf4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfbf4-107">Parameters</span></span>

  - <span data-ttu-id="dfbf4-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="dfbf4-108">*Index*</span></span>

  - <span data-ttu-id="dfbf4-109">Ein **String** -Wert, der den Namen des zu löschenden Objekts oder die Position des Objekts (Index) in der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="dfbf4-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfbf4-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dfbf4-110">Remarks</span></span>

<span data-ttu-id="dfbf4-p101">Wenn Sie die **Delete** -Methode für eine Auflistung verwenden, können Sie eines der Objekte aus der Auflistung entfernen. Diese Methode steht nur für die **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts zur Verfügung. Sie müssen die [Name](parameter-object-ado.md)-Eigenschaft des [Parameter](name-property-ado.md)-Objekts oder dessen Auflistungsindex verwenden, wenn Sie die **Delete** -Methode aufrufen. Eine Objektvariable ist kein gültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="dfbf4-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

