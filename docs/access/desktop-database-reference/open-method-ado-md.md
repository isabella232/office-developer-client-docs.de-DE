---
title: Open-Methode (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288399"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="6b2c2-102">Open-Methode (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="6b2c2-102">Open method (ADO MD)</span></span>

<span data-ttu-id="6b2c2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b2c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b2c2-104">Ruft die Ergebnisse einer multidimensionalen Abfrage ab, und gibt die Ergebnisse an eine Zellmenge zurück.</span><span class="sxs-lookup"><span data-stu-id="6b2c2-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b2c2-105">Syntax</span></span>

<span data-ttu-id="6b2c2-106">*Cellset*. Open*Source*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="6b2c2-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="6b2c2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b2c2-107">Parameters</span></span>

|<span data-ttu-id="6b2c2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b2c2-108">Parameter</span></span>|<span data-ttu-id="6b2c2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b2c2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6b2c2-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="6b2c2-110">*Source*</span></span> |<span data-ttu-id="6b2c2-p101">Optional. Ein **Variant**-Wert, der eine gültige multidimensionale Abfrage ergibt, z. B. eine MDX-Abfrage (Multidimensional Expression). Das *Source*-Argument entspricht der [Source](source-property-ado-md.md)-Eigenschaft. Weitere Informationen zu MDX finden Sie in der Dokumentation zu OLE DB für OLAP im Microsoft Data Access Components SDK.</span><span class="sxs-lookup"><span data-stu-id="6b2c2-p101">Optional. A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query. The *Source* argument corresponds to the [Source](source-property-ado-md.md) property. For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="6b2c2-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="6b2c2-115">*ActiveConnection*</span></span> |<span data-ttu-id="6b2c2-p102">Optional. Ein **Variant**-Ausdruck, der eine Zeichenfolge ergibt, die entweder einen gültigen Namen einer ADO-[Connection](connection-object-ado.md)-Objektvariable oder eine Definition für eine Verbindung angibt. Das *ActiveConnection*-Argument gibt die Verbindung an, die verwendet werden soll, um das [Cellset](cellset-object-ado-md.md)-Objekt zu öffnen. Wenn Sie eine Verbindungsdefinition für dieses Argument weitergeben, öffnet ADO eine neue Verbindung mithilfe der angegebenen Parameter. Das *ActiveConnection*-Argument entspricht der [ActiveConnection](activeconnection-property-ado-md.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6b2c2-p102">Optional. A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection. The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object. If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters. The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6b2c2-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b2c2-121">Remarks</span></span>

<span data-ttu-id="6b2c2-122">Die **Open**-Methode erzeugt einen Fehler, wenn einer der Parameter ausgelassen wird und vor dem Öffnen des **Cellset**-Objekts der entsprechende Eigenschaftswert nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="6b2c2-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

