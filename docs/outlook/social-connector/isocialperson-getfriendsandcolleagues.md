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

_personencollection_
  
> Out Eine XML-Zeichenfolge, die eine Gruppe von Freunden der Person darstellt und der Definition der **Freunde** entspricht, die in der Erweiterbarkeit des XML-Schemas für Outlook Social Connector (OSC)-Anbieter definiert sind. 
    
## <a name="remarks"></a>Bemerkungen

OSC ruft **GetFriendsAndColleagues** auf, wenn der osc-Anbieter die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt. Wenn der OSC anfänglich die **GetFriendsAndColleagues** -Methode für den Outlook-Benutzer aufruft, der am sozialen Netzwerk angemeldet ist, gibt **GETFRIENDSANDCOLLEAGUES** eine XML-Zeichenfolge zurück, die Freunde des angemeldeten Benutzers im sozialen Netzwerk darstellt. Die XML-Zeichenfolge entspricht der XML-Schema Definition von **friends** und gibt ein **Person** -Element (das auch der osc-Anbieter Schema Definition entspricht) für jeden Freund an. 
  
Wenn **GetFriendsAndColleagues** die Freundes Informationen für den angemeldeten Benutzer zurückgibt, speichert der osc diese Informationen in einem Ordner Kontakte. Dieser Ordner ist spezifisch für das soziale Netzwerk und befindet sich im standardmäßigen Outlook-Speicher des angemeldeten Benutzers. Weitere Informationen dazu, wie der OSC Freundes Informationen in einem Ordner Kontakte speichert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
Die Informationen zu jedem im Parameter persons zurückgegebenen Friend entsprechen der XML-Schema Definition für **Person**. __ Das **Person** -Element unterstützt viele Informationen für jeden Freund, einschließlich der SMTP-e-Mail-Adressen ( **** die den Elementen "Email Address", " **emailAddress2**" und " **emailAddress3** " zugeordnet sind), die der Freund im Soziales Netzwerk und die Benutzer-ID (die dem **UserID** -Element zugeordnet wird), die diesen Freund im sozialen Netzwerk identifiziert. 
  
Um Aktivitäten für einen Outlook-Benutzer anzuzeigen, der im Personen Bereich ausgewählt ist, versucht der OSC, den Benutzer mit jedem von **GetFriendsAndColleagues**zurückgegebenen Freund zu vergleichen. OSC verwendet hierzu die SMTP-Adresse des ausgewählten Outlook-Benutzers mit den e-Mail-Adressen, die jeder Freund im sozialen Netzwerk angegeben hat. Wenn OSC eine entsprechende SMTP-e-Mail-Adresse findet, verwendet der OSC die entsprechende **UserID** des Freundes, um die [ISocialSession:: GetPerson](isocialsession-getperson.md) -Methode aufzurufen. Dies dient dazu, ein [ISocialPerson](isocialpersoniunknown.md) -Objekt für diesen Freund abzurufen, das dem osc dann ermöglicht, Aktivitäten und Bilder dieses Freundes aus dem sozialen Netzwerk abzurufen. 
  
Wenn der ausgewählte Outlook-Benutzer jedoch nicht dieselbe SMTP-Adresse für ein Konto im sozialen Netzwerk angibt oder wenn der Outlook-Benutzer kein Konto in diesem sozialen Netzwerk hat, kann der OSC keine Übereinstimmung für diesen Benutzer finden und zeigt keine Aktivitäten an. es für diesen Benutzer im sozialen Netzwerk.
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Informationen zu Freunden erhalten](getting-friends-information.md)

