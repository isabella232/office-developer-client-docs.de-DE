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
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Speichert die Versionsinformationen für den Microsoft Exchange Server, die mit Konten in einem Microsoft Office Outlook-Profil verbunden sind.
  
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
  
- Nummer der Hauptversion, die in der Regel erhöht wird, wenn eine Version signifikante neue Features und Änderungen in Funktionen enthält.
    
 _wMinorVersion_
  
- Nummer der Nebenversion, die eine bestimmte Hauptversionsnummer entspricht und, wird im Allgemeinen erhöht, wenn eine Version minor neue Funktionen und wichtige Updates enthält.
    
 _wBuild_
  
- Haupt-Buildnummer an, die bestimmte Haupt- und Hilfsintervalle Versionsnummern entspricht und, wird im Allgemeinen in eine interne Version, die neue Funktionen und Fixes enthält erhöht. Dieser Wert wird auch erhöht, wenn die Version einer Haupt-interner Code Zweigniederlassung oder Meilenstein, wie ein Release Candidate ist.
    
 _wMinorBuild_
  
- Minor Buildnummer an, die in der Regel in einer internen Veröffentlichung erhöht wird, die enthält neue Features oder korrigiert entspricht einem bestimmten Haupt-Build, der einer Haupt-Code Zweigniederlassung oder Meilenstein bezeichnet.
    
## <a name="see-also"></a>Siehe auch



[Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
  
[PidTagProfileServerFullVersion (kanonische Eigenschaft)](pidtagprofileserverfullversion-canonical-property.md)

