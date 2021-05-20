---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Ruft eine Zeichenfolge ab, die Details für die Person darstellt, z. B. den Vornamen, den Nachnamen und eine URL zu einem Profilbild.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427332"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Ruft eine Zeichenfolge ab, die Details für die Person darstellt, z. B. den Vornamen, den Nachnamen und eine URL zu einem Profilbild. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parameter

_details_
  
> [out] Ein XML-Zeichenfolgenwert, der die Details für eine Person darstellt.
    
## <a name="remarks"></a>Hinweise

Die zurückgegebene DETAIL-XML-Zeichenfolge muss der Schemadefinition für **Person** entsprechen, wie im Schema für die Erweiterbarkeit von Outlook Social Connector (OSC) definiert. 
  
Das OSC ruft **GetDetails auf,** wenn der #A0 die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt. Wenn das OSC zunächst die Aktivitäten von Freunden für den angemeldeten Benutzer erhält, ruft es [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)auf und speichert die Informationen von Freunden in einem kontaktspezifischen Ordner für das soziale Netzwerk im Standardspeicher des angemeldeten Benutzers Outlook. Anschließend wird vom OSC **getFriendsAndColleagues** oder **GetDetails** nur dann aufruft, wenn das Aktualisierungsintervall für den Cache abgelaufen ist. Weitere Informationen dazu, wie das OSC die Informationen von Freunden in einem Kontaktordner zwischenspeichert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

