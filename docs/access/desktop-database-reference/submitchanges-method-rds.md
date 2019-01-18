---
title: SubmitChanges-Methode (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ea7f3e27a75b4483cb8cf46e27d4492f831cff33
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714444"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="02b4a-102">SubmitChanges-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="02b4a-102">SubmitChanges method (RDS)</span></span>

<span data-ttu-id="02b4a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02b4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02b4a-104">Sendet ausstehende Änderungen des lokal zwischengespeicherten und aktualisierbaren [Recordset](recordset-object-ado.md)-Objekts an die in der [Connect](connect-property-rds.md)-Eigenschaft oder der [URL](url-property-rds.md)-Eigenschaft angegebene Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="02b4a-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="02b4a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02b4a-105">Syntax</span></span>

<span data-ttu-id="02b4a-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="02b4a-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="02b4a-107">*DataFactory*. SubmitChanges*Connection*, *Recordset-Objekt*</span><span class="sxs-lookup"><span data-stu-id="02b4a-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="02b4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02b4a-108">Parameters</span></span>

|<span data-ttu-id="02b4a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="02b4a-109">Parameter</span></span>|<span data-ttu-id="02b4a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02b4a-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="02b4a-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="02b4a-111">*DataControl*</span></span> |<span data-ttu-id="02b4a-112">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="02b4a-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="02b4a-113">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="02b4a-113">*DataFactory*</span></span> |<span data-ttu-id="02b4a-114">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="02b4a-114">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="02b4a-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="02b4a-115">*Connection*</span></span> |<span data-ttu-id="02b4a-116">Ein **String** -Wert, der die mit der **Connect** -Eigenschaft des **RDS.DataControl** -Objekts erstellte Verbindung darstellt.</span><span class="sxs-lookup"><span data-stu-id="02b4a-116">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>|
|<span data-ttu-id="02b4a-117">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="02b4a-117">*Recordset*</span></span> |<span data-ttu-id="02b4a-118">Eine Objektvariable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="02b4a-118">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="02b4a-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02b4a-119">Remarks</span></span>

<span data-ttu-id="02b4a-120">Die Eigenschaften [Connect](connect-property-rds.md), [Server](server-property-rds.md) und [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) müssen festgelegt sein, bevor Sie die **SubmitChanges** -Methode für das **RDS.DataControl** -Objekt verwenden können.</span><span class="sxs-lookup"><span data-stu-id="02b4a-120">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="02b4a-121">Wenn Sie die [CancelUpdate](cancelupdate-method-rds.md)-Methode aufrufen, nachdem Sie die **SubmitChanges** -Methode für dasselbe **Recordset** -Objekt aufgerufen haben, schlägt der Aufruf von **CancelUpdate** fehl, da die Änderungen bereits übernommen wurden.</span><span class="sxs-lookup"><span data-stu-id="02b4a-121">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="02b4a-122">Es werden nur die geänderten Objekte zur Änderung gesendet. Die Änderungen werden entweder alle erfolgreich vorgenommen oder sie schlagen alle fehl.</span><span class="sxs-lookup"><span data-stu-id="02b4a-122">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="02b4a-123">Sie können nur mit dem *standardmäßigen* **RDSServer.DataFactory** -Objekt **SubmitChanges** verwenden.</span><span class="sxs-lookup"><span data-stu-id="02b4a-123">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="02b4a-124">Diese Methode kann nicht für benutzerdefinierte Geschäftsobjekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02b4a-124">Custom business objects can't use this method.</span></span>

<span data-ttu-id="02b4a-125">Wenn die **URL** -Eigenschaft festgelegt wurde, sendet **SubmitChanges** Änderungen an den durch die URL angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="02b4a-125">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

