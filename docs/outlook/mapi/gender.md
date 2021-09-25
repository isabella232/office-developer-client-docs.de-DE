---
title: Geschlecht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 68c4fbf9e18906ed993dde30060c49e06a79fc7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580195"
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
  
> Die Mindestanzahl der verschiedenen Werte, die für das Geschlecht unterstützt werden.
    
 _genderUnspecified_
  
> Das Geschlecht wird für den Messagingbenutzer nicht angegeben.
    
 _genderFemale_
  
> Der Messaging-Benutzer ist student.
    
 _genderMale_
  
> Der Messaging-Benutzer ist ein Männchen.
    
 _genderCount_
  
> Die Anzahl der unterschiedlichen Werte, die für das Geschlecht unterstützt werden.
    
 _genderMax_
  
> Die maximale Anzahl unterschiedlicher Werte, die für das Geschlecht unterstützt werden.
    
## <a name="see-also"></a>Siehe auch



[PidTagGender (kanonische Eigenschaft)](pidtaggender-canonical-property.md)

