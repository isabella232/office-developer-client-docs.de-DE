---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Gibt eine Zeichenfolge zurück, die eine Auflistung von Personen- und Bilddetails für die benutzer enthält, die durch den parameter personsAddresses angegeben werden.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404533"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Gibt eine Zeichenfolge zurück, die eine Auflistung von Personen- und Bilddetails für die benutzer enthält, die durch den  _parameter personsAddresses angegeben_ werden. 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameter

_personsAddresses_
  
> [in] Eine XML-Zeichenfolge, die die #A0 einer Gruppe von Benutzern mit Hash angibt.
    
_personsCollection_
  
> [out] Eine XML-Zeichenfolge, die eine Sammlung von Personen- und Bilddetails enthält.
    
## <a name="remarks"></a>Hinweise

Der Outlook Social Connector (OSC) ruft **GetPeopleDetails auf,** wenn der #A0 die On-Demand- oder Hybridsynchronisierung von Freunden und Nicht-Freunden unterstützt. 
  
Der  _parameter personsAddresses_ muss der Schemadefinition für **hashedAddresses** entsprechen, wie im Schema für die Erweiterbarkeit des #A0 definiert. Die  _Zeichenfolge personsAddresses_ stellt eine Gruppe von #A0 mit Hash für jeden Benutzer dar, der im Personenbereich angezeigt wird. Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession::LoggedOnUserName-Eigenschaft dargestellt](isocialsession-loggedonusername.md) wird. Die #A0 mit Hash werden mithilfe der hashing-Funktion verschlüsselt, die durch das **hashFunction-Element** in der #A1 des **Anbieters angegeben** wird. Das OSC identifiziert jedes **HashedAddress** in der _personAddresses-Auflistung_ mit einem **Indexelement.** Der Anbieter muss das **Index-Element** verwenden, um die Person des Empfängers **xml** zu identifizieren, wenn er **friends** XML für **GetPeopleDetails zurückgibt.** Wenn der Empfänger kein registrierter Benutzer im sozialen Netzwerk ist, darf der Anbieter keine **Person-XML** für den Empfänger zurückgeben. Das **Indexelement** für jeden Netzwerkbenutzer, der durch **person** XML dargestellt wird, entspricht dem **Indexelement** für den Empfänger in  _personsAddresses_.
  
Das OSC speichert die vom  _parameter personsCollection_ zurückgegebenen Informationen im Arbeitsspeicher. Die  _personsCollection-XML-Zeichenfolge_ muss der Schemadefinition für **Freunde** entsprechen, wie im Schema für die Erweiterbarkeit des OSC-Anbieters definiert. Weitere Informationen dazu, wie das OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)

