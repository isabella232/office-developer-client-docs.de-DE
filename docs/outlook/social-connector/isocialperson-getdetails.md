---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Ruft eine Zeichenfolge, die Details zu einem Profilbild der Person ein, beispielsweise den Vornamen, Nachnamen sowie eine URL darstellt.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795962"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Ruft eine Zeichenfolge, die Details zu einem Profilbild der Person ein, beispielsweise den Vornamen, Nachnamen sowie eine URL darstellt. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parameter

_Details_
  
> [out] Ein XML-String-Wert, der die Details für eine Person darstellt.
    
## <a name="remarks"></a>Hinweise

Die zurückgegebene _Details_ XML-Zeichenfolge muss die Schemadefinition für die **Person**, gemäß Definition im Schema für Outlook Social Connector (OSC)-Erweiterbarkeit des Providers entsprechen.
  
Die OSC-Aufrufe **GetDetails** , wenn der OSC-Anbieter unterstützt zwischengespeichert oder Hybrid Synchronisierung von Freunde im sozialen Netzwerk. Wenn der OSC anfänglich Freunde Aktivitäten für den angemeldeten Benutzer erhält, ruft [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), und speichert Freunde Informationen in einem Kontakteordner speziell für die sozialen Netzwerk, in der Outlook-Standardspeicher des angemeldeten Benutzers . Anschließend wird die OSC nicht **GetFriendsAndColleagues** oder **GetDetails** aufgerufen, wenn das Aktualisierungsintervall für den Cache abgelaufen ist. Weitere Informationen dazu, wie die OSC Informationen in einem Kontakteordner Freunde zwischenspeichert finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson: IUnknown](isocialpersoniunknown.md)

