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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287035"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="0635b-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="0635b-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="0635b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0635b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0635b-105">Speichert Versionsinformationen für den Microsoft Exchange-Server, mit dem Konten in einem Microsoft Office Outlook-Profil verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="0635b-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0635b-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="0635b-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="0635b-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="0635b-107">Members</span></span>

 <span data-ttu-id="0635b-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="0635b-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="0635b-109">Die Hauptversionsnummer, die in der Regel erhöht wird, wenn eine Version wichtige neue Features und Änderungen an der Funktionalität enthält.</span><span class="sxs-lookup"><span data-stu-id="0635b-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="0635b-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="0635b-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="0635b-111">Nebenversionsnummer, die einer bestimmten Hauptversionsnummer entspricht und in der Regel erhöht wird, wenn eine Version kleinere neue Features oder wichtige Fixes enthält.</span><span class="sxs-lookup"><span data-stu-id="0635b-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="0635b-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="0635b-112">_wBuild_</span></span>
  
- <span data-ttu-id="0635b-113">Große Buildnummer, die bestimmten Haupt-und Nebenversionsnummern entspricht und in der Regel in einer internen Version mit neuen Features oder Fixes erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="0635b-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="0635b-114">Dieser Wert wird auch erhöht, wenn es sich bei der Version um einen wichtigen internen Code Zweig oder einen Meilenstein handelt, beispielsweise einen Release Candidate.</span><span class="sxs-lookup"><span data-stu-id="0635b-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="0635b-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="0635b-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="0635b-116">Minor Build number, die in der Regel in einer internen Version erhöht wird, die neue Features oder Fixes enthält, die einem bestimmten Haupt-Build entsprechen, der einen wichtigen Code Zweig oder Meilenstein kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0635b-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0635b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0635b-117">See also</span></span>



[<span data-ttu-id="0635b-118">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="0635b-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="0635b-119">Kanonische Pidtagprofileserverfullversion (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0635b-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

