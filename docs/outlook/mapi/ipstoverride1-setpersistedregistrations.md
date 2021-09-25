---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 0d5ebfe46d34c8ba2381900d445f47bd5ea08215
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587860"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert persönliche Ordnerdateien (PST)-Dateien für die automatische Entsperrung, wodurch weitere Aufrufe von HrTrustedPSTOverrideHandlerCallback vermieden werden.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parameter

_pmval_
  
> [in] Eine [SPropValue-Struktur,](spropvalue.md) die einen Zeiger auf den Pfad der zu registrierenden Dynamic Link Library (DLL) enthält. Die Struktur weist die folgenden Merkmale auf: 
    
   - Ein ulPropTag von [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Eine MVszW-Werteigenschaft, die auf ein Array von Unicode-Zeichenfolgen mit NULL-Terminen festgelegt ist. Weitere Informationen finden Sie im Thema ["SWStringArray".](swstringarray.md) 
    
> [!NOTE]
> SPropValue wird in einer MAPI-Eigenschaft im internen Bereich des PST gespeichert. Diese Eigenschaft ist für gewöhnliche MAPI-Anwendungen nicht zugänglich. 
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Permanente Registrierungen können sich negativ auf die Leistung von Anwendungen wie Outlook und Windows Desktopsuche auswirken, die PSTs öffnen. Berücksichtigen Sie den Leistungseffekt, wenn Sie die Verwendung von beibehaltenen Registrierungen verwenden oder erweitern.
  
> [!IMPORTANT]
> Diese Methode ist nur für Unicode implementiert. Außerdem tritt ein Fehler auf, wenn einer der Pfade im Array nicht die Dateinamenerweiterung .dll hat. 
  
## <a name="see-also"></a>Siehe auch

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

