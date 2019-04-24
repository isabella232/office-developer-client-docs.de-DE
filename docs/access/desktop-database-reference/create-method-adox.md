---
title: Create-Methode (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295422"
---
# <a name="create-method-adox"></a><span data-ttu-id="fa8ed-102">Create-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fa8ed-102">Create method (ADOX)</span></span>

<span data-ttu-id="fa8ed-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa8ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa8ed-104">Erstellt einen neuen Katalog.</span><span class="sxs-lookup"><span data-stu-id="fa8ed-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa8ed-105">Syntax</span></span>

<span data-ttu-id="fa8ed-106">*Katalog*. Erstellen\*\* von connectcollection</span><span class="sxs-lookup"><span data-stu-id="fa8ed-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="fa8ed-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa8ed-107">Parameters</span></span>

|<span data-ttu-id="fa8ed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa8ed-108">Parameter</span></span>|<span data-ttu-id="fa8ed-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa8ed-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fa8ed-110">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="fa8ed-110">*ConnectString*</span></span> |<span data-ttu-id="fa8ed-111">Ein **String** -Wert, der verwendet wird, um eine Verbindung mit der Datenquelle herzustellen.</span><span class="sxs-lookup"><span data-stu-id="fa8ed-111">A **String** value used to connect to the data source.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fa8ed-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa8ed-112">Remarks</span></span>

<span data-ttu-id="fa8ed-p101">Die **Create**-Methode erstellt und öffnet ein neues ADO-[Connection](connection-object-ado.md)-Objekt für die in *ConnectString* angegebene Datenquelle. Bei erfolgreicher Ausführung wird das neue **Connection**-Objekt der [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fa8ed-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="fa8ed-115">Wenn der Anbieter das Erstellen von neuen Katalogen nicht unterstützt, tritt ein Fehler auf,.</span><span class="sxs-lookup"><span data-stu-id="fa8ed-115">An error will occur if the provider does not support creating new catalogs.</span></span>

