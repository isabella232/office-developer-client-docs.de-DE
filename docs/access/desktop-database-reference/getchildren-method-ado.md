---
title: GetChildren-Methode (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722025"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="80338-102">GetChildren-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="80338-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="80338-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80338-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="80338-104">Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, dessen Zeilen die untergeordneten Elemente einer Auflistung eines [Record](record-object-ado.md) darstellen.</span><span class="sxs-lookup"><span data-stu-id="80338-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="80338-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="80338-105">Syntax</span></span>

<span data-ttu-id="80338-106">**Festlegen** *Recordset-Objekt*  =  *Datensatz*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="80338-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="80338-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80338-107">Return value</span></span>

<span data-ttu-id="80338-p101">Ein **Recordset** -Objekt, bei dem jede Zeile ein untergeordnetes Element des aktuellen **Record** -Objekts darstellt. Das untergeordnete Element eines **Record**, der ein Verzeichnis darstellt, sind beispielsweise die Dateien und Unterverzeichnisse innerhalb des übergeordneten Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="80338-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="80338-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80338-110">Remarks</span></span>

<span data-ttu-id="80338-p102">Der Anbieter bestimmt, welche Spalten im zurückgegebenen **Recordset** -Objekt vorhanden sind. Ein Anbieter für Dokumentquellen gibt beispielsweise immer ein **Recordset** -Ressourcenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="80338-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

