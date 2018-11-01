---
title: Recordset- und SourceRecordset-Eigenschaft (RDS)
TOCTitle: Recordset, SourceRecordset Properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 08fe0f569b36fe0b3403cb564dc53eadf2edff8c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887180"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="56831-102">Recordset- und SourceRecordset-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="56831-102">Recordset, SourceRecordset Properties (RDS)</span></span>


<span data-ttu-id="56831-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56831-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56831-104">Gibt das **Recordset** -Objekt an, das von einem benutzerdefinierten Geschäftsobjekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56831-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="56831-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56831-105">Syntax</span></span>

<span data-ttu-id="56831-106">*DataControl*. SourceRecordset = *Recordset-Objekt*</span><span class="sxs-lookup"><span data-stu-id="56831-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="56831-107">*Recordset* = *DataControl*. Recordset-Objekt</span><span class="sxs-lookup"><span data-stu-id="56831-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="56831-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56831-108">Parameters</span></span>

  - <span data-ttu-id="56831-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="56831-109">*DataControl*</span></span>

  - <span data-ttu-id="56831-110">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="56831-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="56831-111">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="56831-111">*Recordset*</span></span>

  - <span data-ttu-id="56831-112">Eine Objektvariable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="56831-112">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="56831-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56831-113">Remarks</span></span>

<span data-ttu-id="56831-114">Sie können die **SourceRecordset** -Eigenschaft auf ein [Recordset](recordset-object-ado.md) festlegen, das von einem benutzerdefinierten Geschäftsobjekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56831-114">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="56831-p101">Diese Eigenschaften ermöglichen es einer Anwendung, den Bindungsprozess anhand eines benutzerdefinierten Prozesses zu verarbeiten. Die Eigenschafen empfangen ein Rowset, das in ein **Recordset** -Objekt eingebunden ist, sodass Sie das **Recordset** -Objekt direkt verarbeiten können, z. B. mit Aktionen wie dem Festlegen von Eigenschaften oder Iteration durch das **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="56831-p101">These properties allow an application to handle the binding process by means of a custom process. They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="56831-117">Sie können zur Laufzeit im Skriptcode die **SourceRecordset** -Eigenschaft festlegen oder die **Recordset** -Eigenschaft lesen.</span><span class="sxs-lookup"><span data-stu-id="56831-117">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="56831-118">**SourceRecordset** ist eine lesegeschützte Eigenschaft im Gegensatz zur **Recordset** -Eigenschaft, die schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="56831-118">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

