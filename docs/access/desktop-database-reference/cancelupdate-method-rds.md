---
title: CancelUpdate-Methode (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 794c77c0ab6ab2abf22b04def8763fd1e0c51913
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949614"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="910c4-102">CancelUpdate-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="910c4-102">CancelUpdate method (RDS)</span></span>

<span data-ttu-id="910c4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="910c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="910c4-104">Verwirft alle an der aktuellen oder neuen Zeile eines [Recordset](recordset-object-ado.md)-Objekts vorgenommenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="910c4-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="910c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="910c4-105">Syntax</span></span>

<span data-ttu-id="910c4-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="910c4-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="910c4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="910c4-107">Parameters</span></span>

|<span data-ttu-id="910c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="910c4-108">Parameter</span></span>|<span data-ttu-id="910c4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="910c4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="910c4-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="910c4-110">*DataControl*</span></span> |<span data-ttu-id="910c4-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="910c4-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="910c4-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="910c4-112">Remarks</span></span>

<span data-ttu-id="910c4-p101">Der Cursordienst für OLE DB behält eine Kopie der ursprünglichen Werte bei und speichert die Änderungen zwischen. Wenn Sie **CancelUpdate** aufrufen, wird der Cache auf den leeren Zustand zurückgesetzt, und alle gebundenen Steuerelemente werden auf die ursprünglichen Daten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="910c4-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

