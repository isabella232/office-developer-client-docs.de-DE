---
title: Append-Methode (ADOX Users)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707598"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="f84b6-102">Append-Methode (ADOX Users)</span><span class="sxs-lookup"><span data-stu-id="f84b6-102">Append method (ADOX Users)</span></span>

<span data-ttu-id="f84b6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f84b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f84b6-104">Fügt der [Users](user-object-adox.md)-Auflistung ein neues [User](users-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="f84b6-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f84b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f84b6-105">Syntax</span></span>

<span data-ttu-id="f84b6-106">*Benutzer*. Fügen Sie*Benutzer*\[,*Kennwort*\]</span><span class="sxs-lookup"><span data-stu-id="f84b6-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="f84b6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f84b6-107">Parameters</span></span>

|<span data-ttu-id="f84b6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f84b6-108">Parameter</span></span>|<span data-ttu-id="f84b6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f84b6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f84b6-110">*User*</span><span class="sxs-lookup"><span data-stu-id="f84b6-110">*User*</span></span> |<span data-ttu-id="f84b6-111">Ein **Variant** -Wert, der das anzufügende **User** -Objekt enthält oder den Namen des zu erstellenden und anzufügenden Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f84b6-111">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>|
|<span data-ttu-id="f84b6-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="f84b6-112">*Password*</span></span> |<span data-ttu-id="f84b6-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="f84b6-113">Optional.</span></span> <span data-ttu-id="f84b6-114">Ein **String** -Wert, der das Kennwort für den Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="f84b6-114">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="f84b6-115">Der Parameter *Password* entspricht dem Wert, der durch die [ChangePassword](changepassword-method-adox.md) -Methode des **User** -Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="f84b6-115">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f84b6-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f84b6-116">Remarks</span></span>

<span data-ttu-id="f84b6-p102">Die **Users** Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dar, die Elemente dieser bestimmten Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="f84b6-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="f84b6-119">Wenn der Anbieter das Erstellen von Benutzern nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="f84b6-119">An error will occur if the provider does not support creating users.</span></span>

> [!NOTE]
> <span data-ttu-id="f84b6-120">[!HINWEIS] Bevor ein **User** -Objekt an die **Users** -Auflistung eines **Group** -Objekts angefügt wird, muss ein **User** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Users** -Auflistung des **Catalog** -Objekts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f84b6-120">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


