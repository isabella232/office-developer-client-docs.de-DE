---
title: GetChildren-Methode (ADO)
TOCTitle: GetChildren Method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06474b6c4ecb29388367f8ceac7c7676002e1384
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602658"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="ce576-102">GetChildren-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ce576-102">GetChildren Method (ADO)</span></span>


<span data-ttu-id="ce576-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce576-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="ce576-104">Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, dessen Zeilen die untergeordneten Elemente einer Auflistung eines [Record](record-object-ado.md) darstellen.</span><span class="sxs-lookup"><span data-stu-id="ce576-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce576-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce576-105">Syntax</span></span>

<span data-ttu-id="ce576-106">**Festlegen** *Recordset-Objekt*  =  *Datensatz*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="ce576-106">**Set** *recordset* = *record*.GetChildren</span></span>

<span data-ttu-id="ce576-107"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="ce576-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="ce576-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce576-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="ce576-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce576-109">Return value</span></span>
>>>>>>> <span data-ttu-id="ce576-110">master</span><span class="sxs-lookup"><span data-stu-id="ce576-110">master</span></span>

<span data-ttu-id="ce576-p101">Ein **Recordset** -Objekt, bei dem jede Zeile ein untergeordnetes Element des aktuellen **Record** -Objekts darstellt. Das untergeordnete Element eines **Record**, der ein Verzeichnis darstellt, sind beispielsweise die Dateien und Unterverzeichnisse innerhalb des übergeordneten Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="ce576-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce576-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce576-113">Remarks</span></span>

<span data-ttu-id="ce576-p102">Der Anbieter bestimmt, welche Spalten im zurückgegebenen **Recordset** -Objekt vorhanden sind. Ein Anbieter für Dokumentquellen gibt beispielsweise immer ein **Recordset** -Ressourcenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ce576-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

