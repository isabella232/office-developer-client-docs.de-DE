---
title: Delete-Methode (ADOX Collections)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bfb9e12f32da56aecd9338e51d6e4656714b6c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871332"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="2fd79-102">Delete-Methode (ADOX Collections)</span><span class="sxs-lookup"><span data-stu-id="2fd79-102">Delete Method (ADOX Collections)</span></span>


<span data-ttu-id="2fd79-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fd79-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="2fd79-104">Entfernt ein Objekt aus einer Auflistung.</span><span class="sxs-lookup"><span data-stu-id="2fd79-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fd79-105">Syntax</span></span>

<span data-ttu-id="2fd79-106">*Auflistung*. Löschen von*Namen*</span><span class="sxs-lookup"><span data-stu-id="2fd79-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="2fd79-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fd79-107">Parameters</span></span>

  - <span data-ttu-id="2fd79-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="2fd79-108">*Name*</span></span>

  - <span data-ttu-id="2fd79-109">Ein **Variant** -Wert, der den Namen oder die Position (Index) des zu löschenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="2fd79-109">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fd79-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fd79-110">Remarks</span></span>

<span data-ttu-id="2fd79-111">Wenn der *Name* nicht in der Auflistung vorhanden ist, wird ein Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="2fd79-111">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="2fd79-p101">Für [Tables](tables-collection-adox.md)- und [Users](users-collection-adox.md)-Auflistungen tritt ein Fehler auf, wenn der Anbieter das Löschen von Tabellen oder gegebenenfalls Benutzern nicht unterstützt. Für [Procedures](procedures-collection-adox.md)- und [Views](views-collection-adox.md)-Auflistungen tritt bei der Verwendung von **Delete** ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2fd79-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

