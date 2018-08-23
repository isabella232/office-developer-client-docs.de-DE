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
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594474"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="5caca-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="5caca-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="5caca-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5caca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5caca-105">Speichert die Versionsinformationen für den Microsoft Exchange Server, die mit Konten in einem Microsoft Office Outlook-Profil verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="5caca-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5caca-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="5caca-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="5caca-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="5caca-107">Members</span></span>

 <span data-ttu-id="5caca-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="5caca-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="5caca-109">Nummer der Hauptversion, die in der Regel erhöht wird, wenn eine Version signifikante neue Features und Änderungen in Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="5caca-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="5caca-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="5caca-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="5caca-111">Nummer der Nebenversion, die eine bestimmte Hauptversionsnummer entspricht und, wird im Allgemeinen erhöht, wenn eine Version minor neue Funktionen und wichtige Updates enthält.</span><span class="sxs-lookup"><span data-stu-id="5caca-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="5caca-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="5caca-112">_wBuild_</span></span>
  
- <span data-ttu-id="5caca-113">Haupt-Buildnummer an, die bestimmte Haupt- und Hilfsintervalle Versionsnummern entspricht und, wird im Allgemeinen in eine interne Version, die neue Funktionen und Fixes enthält erhöht.</span><span class="sxs-lookup"><span data-stu-id="5caca-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="5caca-114">Dieser Wert wird auch erhöht, wenn die Version einer Haupt-interner Code Zweigniederlassung oder Meilenstein, wie ein Release Candidate ist.</span><span class="sxs-lookup"><span data-stu-id="5caca-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="5caca-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="5caca-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="5caca-116">Minor Buildnummer an, die in der Regel in einer internen Veröffentlichung erhöht wird, die enthält neue Features oder korrigiert entspricht einem bestimmten Haupt-Build, der einer Haupt-Code Zweigniederlassung oder Meilenstein bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5caca-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5caca-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5caca-117">See also</span></span>



[<span data-ttu-id="5caca-118">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="5caca-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="5caca-119">PidTagProfileServerFullVersion (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5caca-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

