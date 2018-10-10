---
title: Create-Methode (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475457"
---
# <a name="create-method-adox"></a><span data-ttu-id="bb11a-102">Create-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="bb11a-102">Create Method (ADOX)</span></span>


<span data-ttu-id="bb11a-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb11a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="bb11a-104">Erstellt einen neuen Katalog.</span><span class="sxs-lookup"><span data-stu-id="bb11a-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb11a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb11a-105">Syntax</span></span>

<span data-ttu-id="bb11a-106">*Katalog*. *ConnectString* erstellen</span><span class="sxs-lookup"><span data-stu-id="bb11a-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="bb11a-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="bb11a-107">Parameters</span></span>

  - <span data-ttu-id="bb11a-108">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="bb11a-108">*ConnectString*</span></span>

  - <span data-ttu-id="bb11a-109">Ein **String** -Wert, der verwendet wird, um eine Verbindung mit der Datenquelle herzustellen.</span><span class="sxs-lookup"><span data-stu-id="bb11a-109">A **String** value used to connect to the data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb11a-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb11a-110">Remarks</span></span>

<span data-ttu-id="bb11a-p101">Die **Create**-Methode erstellt und öffnet ein neues ADO-[Connection](connection-object-ado.md)-Objekt für die in *ConnectString* angegebene Datenquelle. Bei erfolgreicher Ausführung wird das neue **Connection**-Objekt der [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bb11a-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="bb11a-113">Wenn der Anbieter das Erstellen von neuen Katalogen nicht unterstützt, tritt ein Fehler auf,.</span><span class="sxs-lookup"><span data-stu-id="bb11a-113">An error will occur if the provider does not support creating new catalogs.</span></span>

