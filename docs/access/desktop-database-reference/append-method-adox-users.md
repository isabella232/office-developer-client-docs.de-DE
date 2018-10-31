---
title: Append-Methode (ADOX Users)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc8f7a2d217a25a8404765aa05bae19fdccad2c3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863864"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="1ab6e-102">Append-Methode (ADOX Users)</span><span class="sxs-lookup"><span data-stu-id="1ab6e-102">Append Method (ADOX Users)</span></span>


<span data-ttu-id="1ab6e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ab6e-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="1ab6e-104">Fügt der [Users](user-object-adox.md)-Auflistung ein neues [User](users-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="1ab6e-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ab6e-105">Syntax</span></span>

<span data-ttu-id="1ab6e-106">*Benutzer*. Fügen Sie*Benutzer*\[,*Kennwort*\]</span><span class="sxs-lookup"><span data-stu-id="1ab6e-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="1ab6e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="1ab6e-107">Parameters</span></span>

  - <span data-ttu-id="1ab6e-108">*User*</span><span class="sxs-lookup"><span data-stu-id="1ab6e-108">*User*</span></span>

  - <span data-ttu-id="1ab6e-109">Ein **Variant** -Wert, der das anzufügende **User** -Objekt enthält oder den Namen des zu erstellenden und anzufügenden Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1ab6e-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="1ab6e-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="1ab6e-110">*Password*</span></span>

  - <span data-ttu-id="1ab6e-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ab6e-111">Optional.</span></span> <span data-ttu-id="1ab6e-112">Ein **String** -Wert, der das Kennwort für den Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="1ab6e-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="1ab6e-113">Der Parameter *Password* entspricht dem Wert, der durch die [ChangePassword](changepassword-method-adox.md) -Methode des **User** -Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="1ab6e-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ab6e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ab6e-114">Remarks</span></span>

<span data-ttu-id="1ab6e-p102">Die **Users** Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dar, die Elemente dieser bestimmten Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="1ab6e-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="1ab6e-117">Wenn der Anbieter das Erstellen von Benutzern nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1ab6e-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <span data-ttu-id="1ab6e-118">[!HINWEIS] Bevor ein **User** -Objekt an die **Users** -Auflistung eines **Group** -Objekts angefügt wird, muss ein **User** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Users** -Auflistung des **Catalog** -Objekts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1ab6e-118">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


