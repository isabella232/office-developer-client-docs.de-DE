---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407655"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameter

_personsCollection_
  
> [out] Eine XML-Zeichenfolge, die eine Gruppe von Freunden der Person  darstellt und die der Definition von Freunden entspricht, die im XML-Schema für die Erweiterbarkeit des Outlook Social Connector (OSC)-Anbieters definiert ist. 
    
## <a name="remarks"></a>Hinweise

Das OSC ruft **GetFriendsAndColleagues auf,** wenn der OSC-Anbieter die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt. Wenn das OSC zunächst die **GetFriendsAndColleagues-Methode** für den Outlook-Benutzer aufruft, der beim sozialen Netzwerk angemeldet ist, gibt **GetFriendsAndColleagues** eine XML-Zeichenfolge zurück, die Freunde des angemeldeten Benutzers im sozialen Netzwerk darstellt. Die XML-Zeichenfolge entspricht der **Friends-XML-Schemadefinition** und gibt ein Person-Element (das auch der Schemadefinition des OSC-Anbieters entspricht) für jeden Freund an.  
  
Wenn **GetFriendsAndColleagues die Freundesinformationen** für den angemeldeten Benutzer zurückgibt, speichert das OSC diese Informationen in einem Kontaktordner. Dieser Ordner ist spezifisch für das soziale Netzwerk und befindet sich im Standardspeicher des angemeldeten Benutzers Outlook Speicher. Weitere Informationen dazu, wie das OSC die Informationen von Freunden in einem Kontaktordner zwischenspeichert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
Die Informationen für jeden im  _parameter personsCollection zurückgegebenen_ Freund entsprechen der XML-Schemadefinition für **Person**. Das **Person-Element** unterstützt viele Informationen für jeden Freund, einschließlich der SMTP-E-Mail-Adressen (die den **Elementen emailAddress,** **emailAddress2** und **emailAddress3** zugeordnet sind), die der Freund im sozialen Netzwerk angegeben hat, und die Benutzer-ID (die dem **userID-Element** zugeordnet ist), die diesen Freund im sozialen Netzwerk identifiziert. 
  
Zum Anzeigen von Aktivitäten für Outlook Benutzer, der im Personenbereich ausgewählt ist, versucht das OSC, den Benutzer mit jedem von **GetFriendsAndColleagues** zurückgegebenen Freund zu verfeinern. Das OSC führt dies durch Abgleichen der SMTP-Adresse des ausgewählten Outlook-Benutzers mit den E-Mail-Adressen aus, die jeder Freund im sozialen Netzwerk angegeben hat. Wenn das OSC eine übereinstimmende SMTP-E-Mail-Adresse findet, verwendet das OSC die entsprechende **userID** des Freundes, um die [ISocialSession::GetPerson-Methode auf](isocialsession-getperson.md) aufruft. Dies wird zum Abrufen eines [ISocialPerson-Objekts](isocialpersoniunknown.md) für diesen Freund verwendet, mit dem das OSC dann Aktivitäten und Bilder dieses Freundes aus dem sozialen Netzwerk abrufen kann. 
  
Wenn der ausgewählte Outlook-Benutzer jedoch nicht dieselbe SMTP-Adresse für ein Konto im sozialen Netzwerk anbeigt, oder wenn der Outlook-Benutzer kein Konto in diesem sozialen Netzwerk hat, kann das OsC keine Übereinstimmung für diesen Benutzer finden und keine Aktivitäten für diesen Benutzer im sozialen Netzwerk anzeigen.
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Abrufen von Informationen zu Freunden](getting-friends-information.md)

