---
title: Delete-Methode (ADOX Collections)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708634"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="c9769-102">Delete-Methode (ADOX Collections)</span><span class="sxs-lookup"><span data-stu-id="c9769-102">Delete method (ADOX Collections)</span></span>

<span data-ttu-id="c9769-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9769-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9769-104">Entfernt ein Objekt aus einer Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c9769-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9769-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9769-105">Syntax</span></span>

<span data-ttu-id="c9769-106">*Auflistung*. Löschen von*Namen*</span><span class="sxs-lookup"><span data-stu-id="c9769-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="c9769-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9769-107">Parameters</span></span>

|<span data-ttu-id="c9769-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9769-108">Parameter</span></span>|<span data-ttu-id="c9769-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9769-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c9769-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="c9769-110">*Name*</span></span> |<span data-ttu-id="c9769-111">Ein **Variant** -Wert, der den Namen oder die Position (Index) des zu löschenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c9769-111">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c9769-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9769-112">Remarks</span></span>

<span data-ttu-id="c9769-113">Wenn der *Name* nicht in der Auflistung vorhanden ist, wird ein Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="c9769-113">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="c9769-p101">Für [Tables](tables-collection-adox.md)- und [Users](users-collection-adox.md)-Auflistungen tritt ein Fehler auf, wenn der Anbieter das Löschen von Tabellen oder gegebenenfalls Benutzern nicht unterstützt. Für [Procedures](procedures-collection-adox.md)- und [Views](views-collection-adox.md)-Auflistungen tritt bei der Verwendung von **Delete** ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9769-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

