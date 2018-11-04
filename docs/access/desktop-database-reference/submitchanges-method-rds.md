---
title: SubmitChanges-Methode (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba6b6ff2d373a8b05d0839d4cc113f48b47d8cad
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949586"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="8d630-102">SubmitChanges-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="8d630-102">SubmitChanges method (RDS)</span></span>

<span data-ttu-id="8d630-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d630-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d630-104">Sendet ausstehende Änderungen des lokal zwischengespeicherten und aktualisierbaren [Recordset](recordset-object-ado.md)-Objekts an die in der [Connect](connect-property-rds.md)-Eigenschaft oder der [URL](url-property-rds.md)-Eigenschaft angegebene Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="8d630-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d630-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d630-105">Syntax</span></span>

<span data-ttu-id="8d630-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="8d630-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="8d630-107">*DataFactory*. SubmitChanges*Connection*, *Recordset-Objekt*</span><span class="sxs-lookup"><span data-stu-id="8d630-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="8d630-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d630-108">Parameters</span></span>

|<span data-ttu-id="8d630-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d630-109">Parameter</span></span>|<span data-ttu-id="8d630-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d630-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8d630-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="8d630-111">*DataControl*</span></span> |<span data-ttu-id="8d630-112">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d630-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="8d630-113">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="8d630-113">*DataFactory*</span></span> |<span data-ttu-id="8d630-114">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d630-114">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="8d630-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="8d630-115">*Connection*</span></span> |<span data-ttu-id="8d630-116">Ein **String** -Wert, der die mit der **Connect** -Eigenschaft des **RDS.DataControl** -Objekts erstellte Verbindung darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d630-116">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>|
|<span data-ttu-id="8d630-117">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="8d630-117">*Recordset*</span></span> |<span data-ttu-id="8d630-118">Eine Objektvariable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d630-118">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8d630-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d630-119">Remarks</span></span>

<span data-ttu-id="8d630-120">Die Eigenschaften [Connect](connect-property-rds.md), [Server](server-property-rds.md) und [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) müssen festgelegt sein, bevor Sie die **SubmitChanges** -Methode für das **RDS.DataControl** -Objekt verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8d630-120">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="8d630-121">Wenn Sie die [CancelUpdate](cancelupdate-method-rds.md)-Methode aufrufen, nachdem Sie die **SubmitChanges** -Methode für dasselbe **Recordset** -Objekt aufgerufen haben, schlägt der Aufruf von **CancelUpdate** fehl, da die Änderungen bereits übernommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8d630-121">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="8d630-122">Es werden nur die geänderten Objekte zur Änderung gesendet. Die Änderungen werden entweder alle erfolgreich vorgenommen oder sie schlagen alle fehl.</span><span class="sxs-lookup"><span data-stu-id="8d630-122">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="8d630-123">Sie können nur mit dem *standardmäßigen* **RDSServer.DataFactory** -Objekt **SubmitChanges** verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d630-123">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="8d630-124">Diese Methode kann nicht für benutzerdefinierte Geschäftsobjekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d630-124">Custom business objects can't use this method.</span></span>

<span data-ttu-id="8d630-125">Wenn die **URL** -Eigenschaft festgelegt wurde, sendet **SubmitChanges** Änderungen an den durch die URL angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="8d630-125">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

