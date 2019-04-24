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
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315477"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert persönliche Ordner-Dateien (PST) für die automatische Entriegelung und verhindert weitere Aufrufe des HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parameter

_pmval_
  
> in Eine [SPropValue](spropvalue.md) -Struktur, die einen Zeiger auf den Pfad der zu registrierende Dynamic Link Library (dll) enthält. Die Struktur weist die folgenden Merkmale auf: 
    
   - Ein ulPropTag von [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Eine MVszW-Werteigenschaft, die auf ein Array von Zeichenfolgen mit null-terminierten Unicode-Zeichensätzen festgelegt ist. Weitere Informationen finden Sie im Thema [SWStringArray](swstringarray.md) . 
    
> [!NOTE]
> Das SPropValue wird in einer MAPI-Eigenschaft im internen Datenbereichen des PST-Speichers gespeichert. Auf diese Eigenschaft kann für normale MAPI-Anwendungen nicht zugegriffen werden. 
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Dauerhafte Registrierungen können sich negativ auf die Leistung von Anwendungen wie Outlook und Windows-Desktop Suche auswirken, die PST öffnen. Berücksichtigen Sie die Leistungsauswirkung bei der Verwendung oder Erweiterung der Nutzung dauerhafter Registrierungen.
  
> [!IMPORTANT]
> Diese Methode ist nur für Unicode implementiert. Außerdem kann es zu einem vorbeugenden Fehler führen, wenn einer der Pfade im Array keine Dateinamenerweiterung von dll aufweist. 
  
## <a name="see-also"></a>Siehe auch

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

