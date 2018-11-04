---
title: Append-Methode (ADOX Groups)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d552539b84972b4a20fe0bff39b6c8570719bcf7
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950160"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="a4c7e-102">Append-Methode (ADOX Groups)</span><span class="sxs-lookup"><span data-stu-id="a4c7e-102">Append method (ADOX Groups)</span></span>

<span data-ttu-id="a4c7e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4c7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4c7e-104">Fügt der [Groups](group-object-adox.md)-Auflistung ein neues [Group](groups-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4c7e-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4c7e-105">Syntax</span></span>

<span data-ttu-id="a4c7e-106">*Gruppen*. Fügen Sie die*Gruppe*</span><span class="sxs-lookup"><span data-stu-id="a4c7e-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="a4c7e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4c7e-107">Parameters</span></span>

|<span data-ttu-id="a4c7e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4c7e-108">Parameter</span></span>|<span data-ttu-id="a4c7e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4c7e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a4c7e-110">*Group*</span><span class="sxs-lookup"><span data-stu-id="a4c7e-110">*Group*</span></span> |<span data-ttu-id="a4c7e-111">Das anzufügende **Group** -Objekt oder der Name der zu erstellenden und anzufügenden Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a4c7e-111">The **Group** object to append or the name of the group to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a4c7e-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4c7e-112">Remarks</span></span>

<span data-ttu-id="a4c7e-p101">Die **Groups** -Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.</span><span class="sxs-lookup"><span data-stu-id="a4c7e-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="a4c7e-115">Wenn der Anbieter das Erstellen von Gruppen nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a4c7e-115">An error will occur if the provider does not support creating groups.</span></span>

> [!NOTE]
> <span data-ttu-id="a4c7e-116">[!HINWEIS] Bevor ein **Group** -Objekt an die **Groups** -Auflistung eines **User** -Objekts angefügt wird, muss ein **Group** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Groups** -Auflistung des **Catalog** -Objekts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a4c7e-116">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


