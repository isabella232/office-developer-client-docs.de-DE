---
title: Open-Methode (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86a4dcd97171a1dc9817f69a6c010a363009e9ef
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949593"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="e3c04-102">Open-Methode (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e3c04-102">Open method (ADO MD)</span></span>

<span data-ttu-id="e3c04-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3c04-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3c04-104">Ruft die Ergebnisse einer multidimensionalen Abfrage ab, und gibt die Ergebnisse an eine Zellmenge zurück.</span><span class="sxs-lookup"><span data-stu-id="e3c04-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c04-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3c04-105">Syntax</span></span>

<span data-ttu-id="e3c04-106">*Zellmenge*. Open-*Source*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="e3c04-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="e3c04-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3c04-107">Parameters</span></span>

|<span data-ttu-id="e3c04-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3c04-108">Parameter</span></span>|<span data-ttu-id="e3c04-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3c04-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e3c04-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="e3c04-110">*Source*</span></span> |<span data-ttu-id="e3c04-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="e3c04-111">Optional.</span></span> <span data-ttu-id="e3c04-112">Ein **Variant-Wert** , der eine gültige multidimensionale Abfrage, beispielsweise eine Abfrage (Multidimensional Expression) ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="e3c04-112">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="e3c04-113">Das Argument *Source* entspricht die [Source](source-property-ado-md.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e3c04-113">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="e3c04-114">Weitere Informationen zu MDX finden Sie unter OLE DB für OLAP-Dokumentation, die in der Microsoft Data Access Components SDK.</span><span class="sxs-lookup"><span data-stu-id="e3c04-114">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="e3c04-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="e3c04-115">*ActiveConnection*</span></span> |<span data-ttu-id="e3c04-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="e3c04-116">Optional.</span></span> <span data-ttu-id="e3c04-117">Ein **Variant** -Ausdruck, der eine Zeichenfolge ergibt, die entweder einen gültigen Namen einer ADO- [Connection](connection-object-ado.md)-Objektvariable oder eine Definition für eine Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e3c04-117">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="e3c04-118">Das *ActiveConnection* -Argument gibt die Verbindung an, die zum Öffnen des [Cellset](cellset-object-ado-md.md) -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e3c04-118">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="e3c04-119">Wenn Sie eine Verbindungsdefinition für dieses Argument übergeben, öffnet ADO mithilfe der angegebenen Parameter eine neue Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e3c04-119">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="e3c04-120">Die [ActiveConnection](activeconnection-property-ado-md.md) -Eigenschaft entspricht das *ActiveConnection* -Argument.</span><span class="sxs-lookup"><span data-stu-id="e3c04-120">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e3c04-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3c04-121">Remarks</span></span>

<span data-ttu-id="e3c04-122">Die **Open** -Methode erzeugt einen Fehler, wenn einer der Parameter ausgelassen wird und vor dem Öffnen des **Cellset** -Objekts der entsprechende Eigenschaftswert nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e3c04-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

