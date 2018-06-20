---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Ruft eine Zeichenfolge, die eine Auflistung von Personen darstellt.
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795971"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Ruft eine Zeichenfolge, die eine Auflistung von Personen darstellt.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameter

_personsCollection_
  
> [out] Eine XML-Zeichenfolge, die eine Reihe von Freunde der Person darstellt, und gemäß Definition im XML-Schema für die Erweiterbarkeit des Outlook Social Connector (OSC)-Anbieter mit der Definition des **Freunde** entspricht. 
    
## <a name="remarks"></a>Hinweise

Die OSC-Aufrufe **GetFriendsAndColleagues** , wenn der OSC-Anbieter unterstützt zwischengespeichert oder Hybrid Synchronisierung von Freunde im sozialen Netzwerk. Wenn die OSC zunächst die **GetFriendsAndColleagues** -Methode für den Outlook-Benutzer aufruft, der für das soziale Netzwerk **GetFriendsAndColleagues** angemeldet ist, gibt eine XML-Zeichenfolge, die Freunde des angemeldeten Benutzers im sozialen Netzwerk darstellt zurück. Die XML-Zeichenfolge die **Freunde** XML-Schemadefinition entspricht und gibt ein **Person** -Element (das auch die OSC-Anbieter-Schemadefinition entspricht) für jeden Friend. 
  
Wenn **GetFriendsAndColleagues** den Freunden, die Informationen für den angemeldeten Benutzer zurückgibt, speichert die OSC, die betreffenden Informationen in einem Kontakteordner. Dieser Ordner ist speziell für das soziale Netzwerk und befindet sich im Outlook-Standardspeicher des angemeldeten Benutzers. Weitere Informationen dazu, wie die OSC Informationen in einem Kontakteordner Freunde zwischenspeichert finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).
  
Die XML-Schemadefinition für **Person**erfüllt Informationen für jede Freund, die in der _PersonsCollection_ -Parameter zurückgegeben. Das **Person** -Element unterstützt viele Teile der Informationen für einen Freund, einschließlich der SMTP-e-Mail-Adressen (, die die Elemente **EmailAddress**, **emailAddress2**und **emailAddress3** zugeordnet sind), dass die Friend angegeben wurde, auf die soziale Netzwerke und die Benutzer-ID (die **UserID** -Element zugeordnet ist), die dieser Adresse im sozialen Netzwerk identifiziert. 
  
Zum Anzeigen von Aktivitäten für ein Outlook-Benutzer im Bereich Personen ausgewählt, versucht das osc bilden den Benutzer mit jeder Freund von **GetFriendsAndColleagues**zurückgegeben. Die OSC wird durch den Abgleich der SMTP-Adresse des ausgewählten Outlook-Benutzers mit der e-Mail-Adressen, die jeder Freund im sozialen Netzwerk angegeben wurde. Findet die OSC entsprechende SMTP-e-Mail-Adresse, verwendet das osc bilden die entsprechenden **Benutzer-ID** des der Freund die [ISocialSession::GetPerson](isocialsession-getperson.md) -Methode aufrufen. Wird diese Option, damit ein [ISocialPerson](isocialpersoniunknown.md) -Objekt für diese Friend abzurufen, die dann die OSC Aktivitäten und Bilder von dieser Adresse aus dem sozialen Netzwerk abgerufen wird aktiviert. 
  
Jedoch, wenn der ausgewählte Outlook-Benutzer keine der gleichen SMTP-Adresse eines Kontos im sozialen Netzwerk angegeben wird, oder wenn der Outlook-Benutzer nicht über ein Konto für das soziale Netzwerk verfügt, die OSC ist nicht möglich, eine Übereinstimmung für diesen Benutzer zu erhalten und zeigt keine activiti es für diesen Benutzer für das soziale Netzwerk.
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson: IUnknown](isocialpersoniunknown.md)
- [Abrufen von Informationen von Freunden](getting-friends-information.md)

