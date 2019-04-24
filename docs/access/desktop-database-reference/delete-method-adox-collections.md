---
title: Delete-Methode (ADOX-Auflistungen)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294078"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="52c68-102">Delete-Methode (ADOX-Auflistungen)</span><span class="sxs-lookup"><span data-stu-id="52c68-102">Delete method (ADOX Collections)</span></span>

<span data-ttu-id="52c68-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52c68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52c68-104">Entfernt ein Objekt aus einer Auflistung.</span><span class="sxs-lookup"><span data-stu-id="52c68-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52c68-105">Syntax</span></span>

<span data-ttu-id="52c68-106">*Sammlung*. *Name* löschen</span><span class="sxs-lookup"><span data-stu-id="52c68-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="52c68-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="52c68-107">Parameters</span></span>

|<span data-ttu-id="52c68-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="52c68-108">Parameter</span></span>|<span data-ttu-id="52c68-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52c68-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="52c68-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="52c68-110">*Name*</span></span> |<span data-ttu-id="52c68-111">Ein **Variant** -Wert, der den Namen oder die Position (Index) des zu löschenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="52c68-111">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>|

## <a name="remarks"></a><span data-ttu-id="52c68-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52c68-112">Remarks</span></span>

<span data-ttu-id="52c68-113">Wenn der Name nicht in der Auflistung vorhanden ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="52c68-113">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="52c68-p101">Für [Tables](tables-collection-adox.md)- und [Users](users-collection-adox.md)-Auflistungen tritt ein Fehler auf, wenn der Anbieter das Löschen von Tabellen oder gegebenenfalls Benutzern nicht unterstützt. Für [Procedures](procedures-collection-adox.md)- und [Views](views-collection-adox.md)-Auflistungen tritt bei der Verwendung von **Delete** ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52c68-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

