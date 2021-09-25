---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 59f3034fa4217f3ee43cda959e07fd0bc9f8f784
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551646"
---
# <a name="exchange_store_version_num"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert Versionsinformationen für die Microsoft Exchange Server, mit denen Konten in einem Microsoft Office Outlook-Profil verbunden sind.
  
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
  
- Hauptversionsnummer, die in der Regel erhöht wird, wenn eine Version erhebliche neue Features und Änderungen an der Funktionalität enthält.
    
 _wMinorVersion_
  
- Nebenversionsnummer, die einer bestimmten Hauptversionsnummer entspricht und in der Regel erhöht wird, wenn eine Version kleinere neue Features oder wichtige Korrekturen enthält.
    
 _wBuild_
  
- Hauptbuildnummer, die bestimmten Haupt- und Nebenversionsnummern entspricht und in der Regel in einer internen Version erhöht wird, die neue Features oder Fixes enthält. Dieser Wert wird auch erhöht, wenn die Version ein wichtiger interner Codezweig oder Meilenstein ist, z. B. ein Release-Kandidat.
    
 _wMinorBuild_
  
- Kleinere Buildnummer, die in der Regel in einer internen Version erhöht wird, die neue Features oder Fixes enthält, die einem bestimmten Hauptbuild entsprechen, der eine Hauptcodeverzweigung oder einen Meilenstein angibt.
    
## <a name="see-also"></a>Siehe auch



[Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
  
[PidTagProfileServerFullVersion (kanonische Eigenschaft)](pidtagprofileserverfullversion-canonical-property.md)

