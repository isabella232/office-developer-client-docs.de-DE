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
# <a name="exchange_store_version_num"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert Versionsinformationen für die Microsoft Exchange Server, mit der Konten in einem Microsoft Office Outlook verbunden sind.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Elemente

 _wMajorVersion_
  
- Hauptversionsnummer, die in der Regel erhöht wird, wenn eine Version wichtige neue Features und Änderungen in der Funktionalität enthält.
    
 _wMinorVersion_
  
- Nebenversionsnummer, die einer bestimmten Hauptversionsnummer entspricht und in der Regel erhöht wird, wenn eine Version kleinere neue Features oder wichtige Korrekturen enthält.
    
 _wBuild_
  
- Hauptbaunummer, die bestimmten Haupt- und Nebenversionsnummern entspricht und in einer internen Version, die neue Features oder Korrekturen enthält, in der Regel erhöht wird. Dieser Wert wird auch erhöht, wenn es sich bei der Veröffentlichung um einen wichtigen internen Codezweig oder Meilenstein handelt, z. B. einen Veröffentlichungskandidaten.
    
 _wMinorBuild_
  
- Kleinere Buildnummer, die in der Regel in einer internen Version erhöht wird, die neue Features oder Korrekturen enthält, die einem bestimmten Hauptbaustein entspricht, der eine Hauptcodeverzweigung oder einen Meilenstein kennzeichnet.
    
## <a name="see-also"></a>Siehe auch



[Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
  
[PidTagProfileServerFullVersion (kanonische Eigenschaft)](pidtagprofileserverfullversion-canonical-property.md)

