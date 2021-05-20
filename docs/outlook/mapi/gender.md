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
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428648"
---
# <a name="gender"></a>Geschlecht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die möglichen Werte für das Geschlecht eines Messagingbenutzers an.
  
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
  
> Die Mindestanzahl unterschiedlicher Werte, die für das Geschlecht unterstützt werden.
    
 _genderUnspecified_
  
> Das Geschlecht wird für den Messagingbenutzer nicht angegeben.
    
 _genderFemale_
  
> Der Messagingbenutzer ist weiblich.
    
 _genderMale_
  
> Der Messagingbenutzer ist männlich.
    
 _genderCount_
  
> Die Anzahl der verschiedenen Werte, die für das Geschlecht unterstützt werden.
    
 _genderMax_
  
> Die maximale Anzahl unterschiedlicher Werte, die für das Geschlecht unterstützt werden.
    
## <a name="see-also"></a>Siehe auch



[PidTagGender (kanonische Eigenschaft)](pidtaggender-canonical-property.md)

