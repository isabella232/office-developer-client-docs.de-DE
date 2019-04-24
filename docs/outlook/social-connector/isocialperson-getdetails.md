---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Ruft eine Zeichenfolge ab, die Details für die Person darstellt, wie den Vornamen, den Nachnamen und eine URL zu einem Profilbild.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286143"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Ruft eine Zeichenfolge ab, die Details für die Person darstellt, wie den Vornamen, den Nachnamen und eine URL zu einem Profilbild. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parameter

_details_
  
> Out Ein XML-Zeichenfolgenwert, der die Details für eine Person darstellt.
    
## <a name="remarks"></a>Bemerkungen

Die XML-Zeichenfolge zurückgegebene _Details_ muss mit der Schema Definition für **Person**übereinstimmen, wie im Schema for Outlook Social Connector (OSC)-Anbieter Erweiterbarkeit definiert.
  
OSC ruft **getDetails** auf, wenn der osc-Anbieter die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt. Wenn der OSC anfänglich die Aktivitäten von Freunden für den angemeldeten Benutzer abruft, ruft er [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)auf und speichert die Informationen der Freunde in einem für das soziale netzwerkspezifischen Kontakteordner im standardmäßigen Outlook-Speicher des angemeldeten Benutzers. . Anschließend ruft der OSC **GetFriendsAndColleagues** oder getDetails **** nur auf, wenn das Aktualisierungsintervall für den Cache abgelaufen ist. Weitere Informationen dazu, wie der OSC Freundes Informationen in einem Ordner Kontakte speichert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

