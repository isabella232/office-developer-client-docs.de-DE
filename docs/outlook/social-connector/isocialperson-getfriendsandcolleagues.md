---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.
ms.openlocfilehash: 678aaaee4ba1496c013ac59da12770473707f597
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560368"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameter

_personsCollection_
  
> [out] Eine XML-Zeichenfolge, die eine Gruppe von Freunden der Person darstellt und der Definition von **Freunden** entspricht, die im XML-Schema für Outlook OSC-Anbietererweiterung (Social Connector) definiert ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der OSC ruft **GetFriendsAndColleagues auf,** wenn der OSC-Anbieter die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt. Wenn der OSC zunächst die **GetFriendsAndColleagues-Methode** für den Outlook Benutzer aufruft, der beim sozialen Netzwerk angemeldet ist, gibt **GetFriendsAndColleagues** eine XML-Zeichenfolge zurück, die Freunde des angemeldeten Benutzers im sozialen Netzwerk darstellt. Die XML-Zeichenfolge entspricht der XML-Schemadefinition **"friends"** und gibt ein **Personenelement** (das auch der OSC-Anbieterschemadefinition entspricht) für jeden Friend an. 
  
When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder. Dieser Ordner ist spezifisch für das soziale Netzwerk und befindet sich im Standardmäßigen Outlook Speicher des angemeldeten Benutzers. Weitere Informationen dazu, wie der OSC die Informationen von Freunden in einem Kontaktordner zwischenspeichert, finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md)
  
Die Informationen für jeden im _Parameter "personsCollection"_ zurückgegebenen Freund entsprechen der XML-Schemadefinition für **die Person.** Das **Personenelement** unterstützt viele Informationen für jeden Freund, einschließlich der SMTP-E-Mail-Adressen (die den Elementen **emailAddress**, **emailAddress2** und **emailAddress3** zugeordnet sind), die der Freund im sozialen Netzwerk angegeben hat, und die Benutzer-ID (die dem **userID-Element** zugeordnet ist), die diesen Freund im sozialen Netzwerk identifiziert. 
  
Um Aktivitäten für einen im Personenbereich ausgewählten Outlook Benutzers anzuzeigen, versucht osc, den Benutzer mit jedem von **GetFriendsAndColleagues zurückgegebenen** Freund zuzuordnen. Der OSC vergleicht dazu die SMTP-Adresse des ausgewählten Outlook Benutzers mit den E-Mail-Adressen, die jeder Freund im sozialen Netzwerk angegeben hat. Wenn der OSC eine übereinstimmende SMTP-E-Mail-Adresse findet, verwendet osc die entsprechende **UserID** des Freundes, um die [ISocialSession::GetPerson-Methode](isocialsession-getperson.md) aufzurufen. Dies geschieht, um ein [ISocialPerson-Objekt](isocialpersoniunknown.md) für diesen Freund abzurufen, das es dem OSC ermöglicht, Aktivitäten und Bilder dieses Freundes aus dem sozialen Netzwerk abzurufen. 
  
Wenn der ausgewählte Outlook Benutzer jedoch nicht dieselbe SMTP-Adresse für ein Konto im sozialen Netzwerk angibt oder wenn der Outlook Benutzer kein Konto in diesem sozialen Netzwerk hat, kann osc keine Übereinstimmung für diesen Benutzer finden und zeigt keine Aktivitäten für diesen Benutzer im sozialen Netzwerk an.
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Abrufen von Informationen zu Freunden](getting-friends-information.md)

