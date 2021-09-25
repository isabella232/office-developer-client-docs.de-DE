---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Gibt eine Zeichenfolge zurück, die eine Auflistung von Personen- und Bilddetails für die vom Parameter "personsAddresses" angegebenen Benutzer enthält.
ms.openlocfilehash: 88fef14135718e7b054cf85f7e12bb7b0f9c0478
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629151"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Gibt eine Zeichenfolge zurück, die eine Auflistung von Personen- und Bilddetails für die vom Parameter  _"personsAddresses" angegebenen_ Benutzer enthält. 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameter

_personsAddresses_
  
> [in] Eine XML-Zeichenfolge, die die SMTP-Hashadressen einer Gruppe von Benutzern angibt.
    
_personsCollection_
  
> [out] Eine XML-Zeichenfolge, die eine Auflistung von Personen- und Bilddetails enthält.
    
## <a name="remarks"></a>Bemerkungen

The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends. 
  
Der  _Parameter "personsAddresses"_ muss der Schemadefinition für **hashedAddresses** entsprechen, wie im Schema für die OSC-Anbietererweiterung definiert. Die Zeichenfolge  _"personsAddresses"_ stellt eine Reihe von SMTP-Hashadressen für jeden Benutzer dar, der im Personenbereich angezeigt wird. Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession::LoggedOnUserName-Eigenschaft](isocialsession-loggedonusername.md) dargestellt wird. Die SMTP-Hashadressen werden mithilfe der hashing-Funktion verschlüsselt, die durch das **hashFunction-Element** in der **XML-Funktionen** des Anbieters angegeben wird. Der OSC identifiziert jede **hashedAddress** in der _personAddresses-Auflistung_ mit einem **Indexelement.** Der Anbieter muss das **Indexelement** verwenden, um die **Personen-XML** des Empfängers zu identifizieren, wenn er xml für **GetPeopleDetails** zurückgibt.  Wenn der Empfänger kein registrierter Benutzer im sozialen Netzwerk ist, darf der Anbieter keine **Personen-XML** für diesen Empfänger zurückgeben. Das **Indexelement** für jeden durch **Personen-XML** dargestellten Netzwerkbenutzer entspricht dem **Indexelement** für den Empfänger in _"personsAddresses"._
  
Der OSC speichert die vom  _Parameter "personsCollection"_ zurückgegebenen Informationen im Speicher. Die  _PERSONENSAMMLUNG-XML-Zeichenfolge_ muss der Schemadefinition für **Freunde** entsprechen, wie im Schema für die OSC-Anbietererweiterung definiert. Weitere Informationen dazu, wie der OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md)
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)

