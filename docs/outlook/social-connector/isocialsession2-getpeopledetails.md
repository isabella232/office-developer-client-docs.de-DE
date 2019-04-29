---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Gibt eine Zeichenfolge, die eine Auflistung von Personen-und Bilddetails für die durch den personsAddresses-Parameter angegebenen Benutzer enthält.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404533"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Gibt eine Zeichenfolge, die eine Auflistung von Personen-und Bilddetails für die durch den _personsAddresses_ -Parameter angegebenen Benutzer enthält. 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameter

_personsAddresses_
  
> in Eine XML-Zeichenfolge, die die Hash-SMTP-Adressen einer Gruppe von Benutzern angibt.
    
_personencollection_
  
> Out Eine XML-Zeichenfolge, die eine Auflistung von Personen-und Bilddetails enthält.
    
## <a name="remarks"></a>Bemerkungen

Der Outlook Connector für soziale Netzwerke (OSC) ruft **GetPeopleDetails** auf, wenn der osc-Anbieter die on-Demand-oder Hybrid Synchronisierung von Freunden und nicht-Freunden unterstützt. 
  
Der Parameter _personsAddresses_ muss der Schema Definition für **hashedAddresses**entsprechen, wie im Schema für osc-Anbieter Erweiterbarkeit definiert. Die _PERSONSADDRESSES_ -Zeichenfolge stellt einen Satz von Hash-SMTP-Adressen für jeden Benutzer dar, der im Personen Bereich angezeigt wird. Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) -Eigenschaft dargestellt wird. Die Hash-SMTP-Adressen werden mithilfe der Hashfunktion verschlüsselt, die durch das **hashFunction** -Element in den XML- **Funktionen** des Anbieters angegeben wird. OSC identifiziert jede **hashedAddress** in der _personAddresses_ -Auflistung mit einem **Index** -Element. Der Anbieter muss das **Index** -Element verwenden, um den XML **** -Code des Empfängers zu identifizieren, wenn er **Freundes** -XML für **GetPeopleDetails**zurückgibt. Wenn der Empfänger kein registrierter Benutzer im sozialen Netzwerk ist, darf der Anbieter keinen **Personen** -XML-Code für diesen Empfänger zurückgeben. Das **Index** -Element für jeden durch **Person** -XML dargestellten Netzwerkbenutzer entspricht dem **Index** -Element für den Empfänger in _personsAddresses_.
  
OSC speichert die vom personencollection-Parameter __ zurückgegebenen Informationen im Arbeitsspeicher. Die __ XML-Zeichenfolge personencollection muss der Schema Definition für **Freunde**entsprechen, wie im Schema für osc-Anbieter Erweiterbarkeit definiert. Weitere Informationen dazu, wie der OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)

