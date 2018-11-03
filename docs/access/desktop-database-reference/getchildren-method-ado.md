---
title: GetChildren-Methode (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcc687e5151e95d61939c30aa4c6be4063b67c47
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931267"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="45024-102">GetChildren-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="45024-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="45024-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45024-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="45024-104">Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, dessen Zeilen die untergeordneten Elemente einer Auflistung eines [Record](record-object-ado.md) darstellen.</span><span class="sxs-lookup"><span data-stu-id="45024-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45024-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45024-105">Syntax</span></span>

<span data-ttu-id="45024-106">**Festlegen** *Recordset-Objekt*  =  *Datensatz*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="45024-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="45024-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45024-107">Return value</span></span>

<span data-ttu-id="45024-p101">Ein **Recordset** -Objekt, bei dem jede Zeile ein untergeordnetes Element des aktuellen **Record** -Objekts darstellt. Das untergeordnete Element eines **Record**, der ein Verzeichnis darstellt, sind beispielsweise die Dateien und Unterverzeichnisse innerhalb des übergeordneten Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="45024-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="45024-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45024-110">Remarks</span></span>

<span data-ttu-id="45024-p102">Der Anbieter bestimmt, welche Spalten im zurückgegebenen **Recordset** -Objekt vorhanden sind. Ein Anbieter für Dokumentquellen gibt beispielsweise immer ein **Recordset** -Ressourcenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="45024-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

