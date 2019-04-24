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
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert Versionsinformationen für den Microsoft Exchange-Server, mit dem Konten in einem Microsoft Office Outlook-Profil verbunden sind.
  
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
  
- Die Hauptversionsnummer, die in der Regel erhöht wird, wenn eine Version wichtige neue Features und Änderungen an der Funktionalität enthält.
    
 _wMinorVersion_
  
- Nebenversionsnummer, die einer bestimmten Hauptversionsnummer entspricht und in der Regel erhöht wird, wenn eine Version kleinere neue Features oder wichtige Fixes enthält.
    
 _wBuild_
  
- Große Buildnummer, die bestimmten Haupt-und Nebenversionsnummern entspricht und in der Regel in einer internen Version mit neuen Features oder Fixes erhöht wird. Dieser Wert wird auch erhöht, wenn es sich bei der Version um einen wichtigen internen Code Zweig oder einen Meilenstein handelt, beispielsweise einen Release Candidate.
    
 _wMinorBuild_
  
- Minor Build number, die in der Regel in einer internen Version erhöht wird, die neue Features oder Fixes enthält, die einem bestimmten Haupt-Build entsprechen, der einen wichtigen Code Zweig oder Meilenstein kennzeichnet.
    
## <a name="see-also"></a>Siehe auch



[Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
  
[Kanonische Pidtagprofileserverfullversion (-Eigenschaft](pidtagprofileserverfullversion-canonical-property.md)

