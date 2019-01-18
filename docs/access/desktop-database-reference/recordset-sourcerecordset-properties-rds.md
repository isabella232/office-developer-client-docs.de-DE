---
title: Recordset- und SourceRecordset-Eigenschaft (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f83ab385b1fab511ab71ea9ff3456fe466efa17c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703524"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="b93ba-102">Recordset- und SourceRecordset-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="b93ba-102">Recordset, SourceRecordset properties (RDS)</span></span>

<span data-ttu-id="b93ba-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b93ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b93ba-104">Gibt das **Recordset** -Objekt an, das von einem benutzerdefinierten Geschäftsobjekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b93ba-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b93ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b93ba-105">Syntax</span></span>

<span data-ttu-id="b93ba-106">*DataControl*. SourceRecordset = *Recordset-Objekt*</span><span class="sxs-lookup"><span data-stu-id="b93ba-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="b93ba-107">*Recordset* = *DataControl*. Recordset-Objekt</span><span class="sxs-lookup"><span data-stu-id="b93ba-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="b93ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b93ba-108">Parameters</span></span>

|<span data-ttu-id="b93ba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b93ba-109">Parameter</span></span>|<span data-ttu-id="b93ba-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b93ba-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b93ba-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b93ba-111">*DataControl*</span></span> |<span data-ttu-id="b93ba-112">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b93ba-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="b93ba-113">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="b93ba-113">*Recordset*</span></span> |<span data-ttu-id="b93ba-114">Eine Objektvariable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b93ba-114">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b93ba-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b93ba-115">Remarks</span></span>

<span data-ttu-id="b93ba-116">Sie können die **SourceRecordset** -Eigenschaft auf ein [Recordset](recordset-object-ado.md) festlegen, das von einem benutzerdefinierten Geschäftsobjekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b93ba-116">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="b93ba-p101">Diese Eigenschaften ermöglichen es einer Anwendung, den Bindungsprozess anhand eines benutzerdefinierten Prozesses zu verarbeiten. Die Eigenschafen empfangen ein Rowset, das in ein **Recordset** -Objekt eingebunden ist, sodass Sie das **Recordset** -Objekt direkt verarbeiten können, z. B. mit Aktionen wie dem Festlegen von Eigenschaften oder Iteration durch das **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b93ba-p101">These properties allow an application to handle the binding process by means of a custom process. They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="b93ba-119">Sie können zur Laufzeit im Skriptcode die **SourceRecordset** -Eigenschaft festlegen oder die **Recordset** -Eigenschaft lesen.</span><span class="sxs-lookup"><span data-stu-id="b93ba-119">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="b93ba-120">**SourceRecordset** ist eine lesegeschützte Eigenschaft im Gegensatz zur **Recordset** -Eigenschaft, die schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="b93ba-120">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

