---
title: Geschlecht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791777"
---
# <a name="gender"></a>Geschlecht

  
  
**Betrifft**: Outlook 
  
Gibt die möglichen Werte für das Geschlecht der messaging-Benutzer an.
  
## <a name="quick-info"></a>QuickInfo

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a>Members

 _genderMin_
  
> Die minimale Anzahl von unterschiedliche Werte für das Geschlecht unterstützt.
    
 _genderUnspecified_
  
> Das Geschlecht ist nicht für die messaging-Benutzer angegeben.
    
 _genderFemale_
  
> Der messaging-Benutzer ist Weiblich.
    
 _genderMale_
  
> Der messaging-Benutzer ist Männlich.
    
 _genderCount_
  
> Die Anzahl der unterschiedlichen Werte für das Geschlecht unterstützt.
    
 _genderMax_
  
> Die maximale Anzahl von unterschiedlichen Werten für das Geschlecht unterstützt.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagGender-Eigenschaft](pidtaggender-canonical-property.md)

