---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408348"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert Dateien für persönliche Ordner (PST) für die automatische Entsperrung, um weitere Aufrufe von HrTrustedPSTOverrideHandlerCallback zu vermeiden.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parameter

_pmval_
  
> [in] Eine [SPropValue-Struktur,](spropvalue.md) die einen Zeiger auf den Pfad der dynamic-link library (DLL) enthält, die registriert werden soll. Die Struktur hat die folgenden Merkmale: 
    
   - Ein ulPropTag von [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Eine MVszW-Werteigenschaft, die auf ein Array mit mit Nullen beendeten Unicode-Zeichenzeichenfolgen festgelegt ist. Weitere Informationen finden Sie im [Thema SWStringArray.](swstringarray.md) 
    
> [!NOTE]
> Der SPropValue wird in einer MAPI-Eigenschaft im internen Bereich des PST gespeichert. Auf diese Eigenschaft kann für normale MAPI-Anwendungen nicht zugegriffen werden. 
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Beibehaltene Registrierungen können sich negativ auf die Leistung von Anwendungen auswirken, z. B. Outlook und Windows Desktopsuche, die PSTs öffnen. Berücksichtigen Sie den Leistungseffekt, wenn Sie die Verwendung von dauerhaften Registrierungen verwenden oder erweitern.
  
> [!IMPORTANT]
> Diese Methode ist nur für Unicode implementiert. Darüber hinaus wird ein Präemptiv fehlschlagen, wenn einer der Pfade im Array keine Dateinamenerweiterung von .dll. 
  
## <a name="see-also"></a>Siehe auch

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

