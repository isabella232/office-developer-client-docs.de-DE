---
title: SubmitChanges-Methode (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b5c18aa12519e9206702eb2a152e6f0d084edc9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026344"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="6946c-102">SubmitChanges-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="6946c-102">SubmitChanges method (RDS)</span></span>

<span data-ttu-id="6946c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6946c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6946c-104">Sendet ausstehende Änderungen des lokal zwischengespeicherten und aktualisierbaren [Recordset](recordset-object-ado.md)-Objekts an die in der [Connect](connect-property-rds.md)-Eigenschaft oder der [URL](url-property-rds.md)-Eigenschaft angegebene Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="6946c-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6946c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6946c-105">Syntax</span></span>

<span data-ttu-id="6946c-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="6946c-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="6946c-107">*DataFactory*. SubmitChanges*Connection*, *Recordset-Objekt*</span><span class="sxs-lookup"><span data-stu-id="6946c-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="6946c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6946c-108">Parameters</span></span>

|<span data-ttu-id="6946c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6946c-109">Parameter</span></span>|<span data-ttu-id="6946c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6946c-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6946c-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="6946c-111">*DataControl*</span></span> |<span data-ttu-id="6946c-112">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6946c-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="6946c-113">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="6946c-113">*DataFactory*</span></span> |<span data-ttu-id="6946c-114">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6946c-114">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="6946c-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="6946c-115">*Connection*</span></span> |<span data-ttu-id="6946c-116">Ein **String** -Wert, der die mit der **Connect** -Eigenschaft des **RDS.DataControl** -Objekts erstellte Verbindung darstellt.</span><span class="sxs-lookup"><span data-stu-id="6946c-116">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>|
|<span data-ttu-id="6946c-117">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="6946c-117">*Recordset*</span></span> |<span data-ttu-id="6946c-118">Eine Objektvariable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6946c-118">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6946c-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6946c-119">Remarks</span></span>

<span data-ttu-id="6946c-120">Die Eigenschaften [Connect](connect-property-rds.md), [Server](server-property-rds.md) und [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) müssen festgelegt sein, bevor Sie die **SubmitChanges** -Methode für das **RDS.DataControl** -Objekt verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6946c-120">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="6946c-121">Wenn Sie die [CancelUpdate](cancelupdate-method-rds.md)-Methode aufrufen, nachdem Sie die **SubmitChanges** -Methode für dasselbe **Recordset** -Objekt aufgerufen haben, schlägt der Aufruf von **CancelUpdate** fehl, da die Änderungen bereits übernommen wurden.</span><span class="sxs-lookup"><span data-stu-id="6946c-121">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="6946c-122">Es werden nur die geänderten Objekte zur Änderung gesendet. Die Änderungen werden entweder alle erfolgreich vorgenommen oder sie schlagen alle fehl.</span><span class="sxs-lookup"><span data-stu-id="6946c-122">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="6946c-123">Sie können nur mit dem *standardmäßigen* **RDSServer.DataFactory** -Objekt **SubmitChanges** verwenden.</span><span class="sxs-lookup"><span data-stu-id="6946c-123">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="6946c-124">Diese Methode kann nicht für benutzerdefinierte Geschäftsobjekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6946c-124">Custom business objects can't use this method.</span></span>

<span data-ttu-id="6946c-125">Wenn die **URL** -Eigenschaft festgelegt wurde, sendet **SubmitChanges** Änderungen an den durch die URL angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="6946c-125">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

