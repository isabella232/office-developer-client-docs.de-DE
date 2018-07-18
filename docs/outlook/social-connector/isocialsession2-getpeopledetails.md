---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Gibt eine Zeichenfolge, die eine Auflistung von Person und Teile des Bildes Details für die durch den PersonsAddresses-Parameter angegebenen Benutzer enthält.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796000"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Gibt eine Zeichenfolge, die eine Auflistung von Person und Teile des Bildes Details für die durch den _PersonsAddresses_ -Parameter angegebenen Benutzer enthält. 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameter

_personsAddresses_
  
> [in] Ein XML-Zeichenfolge, die die Hash SMTP-Adressen einer Gruppe von Benutzern angibt.
    
_personsCollection_
  
> [out] Eine XML-Zeichenfolge, die eine Auflistung von Person und Teile des Bildes Details enthält.
    
## <a name="remarks"></a>Bemerkungen

Outlook Social Connector (OSC) **GetPeopleDetails** aufgerufen, wenn der OSC-Anbieter auf Abruf oder Hybriden Synchronisierung von Freunde und nicht Freunde unterstützt. 
  
Der Parameter _PersonsAddresses_ muss die Schemadefinition für **HashedAddresses**, gemäß Definition im Schema für die Erweiterbarkeit des OSC-Providers entsprechen. Die Zeichenfolge _PersonsAddresses_ stellt eine Reihe von Hash SMTP-Adressen für jeden Benutzer im Bereich Personen angezeigt. Der Benutzer hat keinen Friend der angemeldete Benutzer von der [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) -Eigenschaft dargestellt werden. Hash SMTP-Adressen werden mithilfe der vom **HashFunction** -Element in der Anbieter **Funktionen** XML angegebenen Hashfunktion verschlüsselt. Die OSC identifiziert jedes **HashedAddress** in der _PersonAddresses_ -Auflistung mit einem **Index** -Element. Der Anbieter muss das **Index** -Element zum Identifizieren des Empfängers **Person** XML bei Rückgabe **Freunde** XML für **GetPeopleDetails**verwenden. Wenn der Empfänger keinem registrierten Benutzer von dem sozialen Netzwerk ist, muss der Anbieter keine **Person** XML für diesen Empfänger zurückgeben. Das **Index** -Element für jeden Netzwerkbenutzer von dargestellt durch **Person** XML entspricht dem **Index** -Element für den Empfänger in _PersonsAddresses_.
  
Die OSC werden die Informationen zurückgegeben, die durch den Parameter _PersonsCollection_ im Arbeitsspeicher gespeichert. Die _PersonsCollection_ XML-Zeichenfolge muss der Schemadefinition für **Freunde**, gemäß Definition im Schema für die Erweiterbarkeit des OSC-Providers entsprechen. Weitere Informationen darüber, wie die OSC verwendet und diese Informationen im Speicher aktualisiert finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md)

