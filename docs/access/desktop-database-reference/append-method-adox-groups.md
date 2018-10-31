---
title: Append-Method (ADOX Groups)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be31cc01122aa24eff2acb8396be2caab33c7dd4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863059"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="8048b-102">Append-Method (ADOX Groups)</span><span class="sxs-lookup"><span data-stu-id="8048b-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="8048b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8048b-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="8048b-104">Fügt der [Groups](group-object-adox.md)-Auflistung ein neues [Group](groups-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="8048b-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8048b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8048b-105">Syntax</span></span>

<span data-ttu-id="8048b-106">*Gruppen*. Fügen Sie die*Gruppe*</span><span class="sxs-lookup"><span data-stu-id="8048b-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="8048b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8048b-107">Parameters</span></span>

  - <span data-ttu-id="8048b-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="8048b-108">*Group*</span></span>

  - <span data-ttu-id="8048b-109">Das anzufügende **Group** -Objekt oder der Name der zu erstellenden und anzufügenden Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8048b-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="8048b-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8048b-110">Remarks</span></span>

<span data-ttu-id="8048b-p101">Die **Groups** -Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.</span><span class="sxs-lookup"><span data-stu-id="8048b-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="8048b-113">Wenn der Anbieter das Erstellen von Gruppen nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8048b-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <span data-ttu-id="8048b-114">[!HINWEIS] Bevor ein **Group** -Objekt an die **Groups** -Auflistung eines **User** -Objekts angefügt wird, muss ein **Group** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Groups** -Auflistung des **Catalog** -Objekts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="8048b-114">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


