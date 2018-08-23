---
title: Geschlecht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588454"
---
# <a name="gender"></a>Geschlecht

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Elemente

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



[PidTagGender (kanonische Eigenschaft)](pidtaggender-canonical-property.md)

