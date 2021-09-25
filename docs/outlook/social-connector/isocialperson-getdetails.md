---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Ruft eine Zeichenfolge ab, die Details für die Person darstellt, z. B. den Vornamen, den Nachnamen und eine URL zu einem Profilbild.
ms.openlocfilehash: d0b78fad082327db049c5bb0b69308df71f74f1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574524"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Ruft eine Zeichenfolge ab, die Details für die Person darstellt, z. B. den Vornamen, den Nachnamen und eine URL zu einem Profilbild. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parameter

_details_
  
> [out] Ein XML-Zeichenfolgenwert, der die Details für eine Person darstellt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die zurückgegebene DETAIL-XML-Zeichenfolge muss der Schemadefinition für **Person** entsprechen, wie im Schema für die Osc-Anbietererweiterung (Social Connector) Outlook. 
  
Der OSC ruft **GetDetails auf,** wenn der OSC-Anbieter die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt. Wenn der OSC zunächst die Aktivitäten von Freunden für den angemeldeten Benutzer abruft, ruft es [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)auf und speichert die Informationen von Freunden in einem Kontaktordner, der für das soziale Netzwerk spezifisch ist, im Standardmäßigen Outlook Speicher des angemeldeten Benutzers. Anschließend ruft der OSC **"GetFriendsAndColleagues"** oder **"GetDetails"** nur dann auf, wenn das Aktualisierungsintervall für den Cache abgelaufen ist. Weitere Informationen dazu, wie der OSC die Informationen von Freunden in einem Kontaktordner zwischenspeichert, finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md)
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

