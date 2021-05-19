---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433724"
---
# <a name="exchange_store_version_num"></a><span data-ttu-id="4c9fc-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="4c9fc-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="4c9fc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c9fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c9fc-105">Speichert Versionsinformationen für die Microsoft Exchange Server, mit der Konten in einem Microsoft Office Outlook verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="4c9fc-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4c9fc-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4c9fc-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="4c9fc-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="4c9fc-107">Members</span></span>

 <span data-ttu-id="4c9fc-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="4c9fc-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="4c9fc-109">Hauptversionsnummer, die in der Regel erhöht wird, wenn eine Version wichtige neue Features und Änderungen in der Funktionalität enthält.</span><span class="sxs-lookup"><span data-stu-id="4c9fc-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="4c9fc-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="4c9fc-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="4c9fc-111">Nebenversionsnummer, die einer bestimmten Hauptversionsnummer entspricht und in der Regel erhöht wird, wenn eine Version kleinere neue Features oder wichtige Korrekturen enthält.</span><span class="sxs-lookup"><span data-stu-id="4c9fc-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="4c9fc-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="4c9fc-112">_wBuild_</span></span>
  
- <span data-ttu-id="4c9fc-113">Hauptbaunummer, die bestimmten Haupt- und Nebenversionsnummern entspricht und in einer internen Version, die neue Features oder Korrekturen enthält, in der Regel erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="4c9fc-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="4c9fc-114">Dieser Wert wird auch erhöht, wenn es sich bei der Veröffentlichung um einen wichtigen internen Codezweig oder Meilenstein handelt, z. B. einen Veröffentlichungskandidaten.</span><span class="sxs-lookup"><span data-stu-id="4c9fc-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="4c9fc-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="4c9fc-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="4c9fc-116">Kleinere Buildnummer, die in der Regel in einer internen Version erhöht wird, die neue Features oder Korrekturen enthält, die einem bestimmten Hauptbaustein entspricht, der eine Hauptcodeverzweigung oder einen Meilenstein kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="4c9fc-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c9fc-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c9fc-117">See also</span></span>



[<span data-ttu-id="4c9fc-118">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="4c9fc-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="4c9fc-119">PidTagProfileServerFullVersion (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4c9fc-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

