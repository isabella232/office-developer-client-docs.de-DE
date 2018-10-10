---
title: Append-Method (ADOX Groups)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475694"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="613a3-102">Append-Method (ADOX Groups)</span><span class="sxs-lookup"><span data-stu-id="613a3-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="613a3-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="613a3-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="613a3-104">Fügt der [Groups](group-object-adox.md)-Auflistung ein neues [Group](groups-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="613a3-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="613a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="613a3-105">Syntax</span></span>

<span data-ttu-id="613a3-106">*Gruppen*. Fügen Sie die*Gruppe*</span><span class="sxs-lookup"><span data-stu-id="613a3-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="613a3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="613a3-107">Parameters</span></span>

  - <span data-ttu-id="613a3-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="613a3-108">*Group*</span></span>

  - <span data-ttu-id="613a3-109">Das anzufügende **Group** -Objekt oder der Name der zu erstellenden und anzufügenden Gruppe.</span><span class="sxs-lookup"><span data-stu-id="613a3-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="613a3-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="613a3-110">Remarks</span></span>

<span data-ttu-id="613a3-p101">Die **Groups** -Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.</span><span class="sxs-lookup"><span data-stu-id="613a3-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="613a3-113">Wenn der Anbieter das Erstellen von Gruppen nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="613a3-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <P><span data-ttu-id="613a3-114">[!HINWEIS] Bevor ein <STRONG>Group</STRONG> -Objekt an die <STRONG>Groups</STRONG> -Auflistung eines <STRONG>User</STRONG> -Objekts angefügt wird, muss ein <STRONG>Group</STRONG> -Objekt mit demselben <A href="name-property-adox.md">Namen</A> wie das anzufügende Objekt bereits in der <STRONG>Groups</STRONG> -Auflistung des <STRONG>Catalog</STRONG> -Objekts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="613a3-114">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


