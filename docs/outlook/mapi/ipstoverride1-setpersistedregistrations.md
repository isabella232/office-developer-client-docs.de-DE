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
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 9895c558af94eebebe2dacdb6f9bf674e3de6263
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792810"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Betrifft**: Outlook 
  
Registriert persönlichen Ordner (PST)-Dateien für die automatische Entsperren Weitere Anrufe an die HrTrustedPSTOverrideHandlerCallback zu vermeiden.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parameter

_pmval_
  
> [in] Eine [SPropValue](spropvalue.md) -Struktur, die einen Zeiger auf den Pfad zu der Dynamic Link Library (DLL enthält) registriert. Die Struktur weist folgende Merkmale auf: 
    
   - Ein UlPropTag des [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Eine MVszW Value-Eigenschaft, die auf ein Array von Zeichenfolgen mit Null terminierte Unicode-Zeichen festgelegt ist. Weitere Informationen finden Sie unter dem Thema [SWStringArray](swstringarray.md) . 
    
> [!NOTE]
> Die SPropValue wird in einem MAPI-Eigenschaft im internen Bereich der PST-Datei gespeichert. Diese Eigenschaft ist nicht möglich, für normale MAPI-Clientanwendungen. 
  
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Beibehaltene Registrierungen können die Leistung der Anwendung, wie Outlook und Windows-Desktopsuche beeinträchtigen, die PST-Dateien öffnen. Berücksichtigen Sie die Auswirkung auf die Leistung bei der Verwendung oder die Verwendung der permanenten Registrierungen erweitern.
  
> [!IMPORTANT]
> Diese Methode ist nur für Unicode implementiert. Darüber hinaus wird es präventiv fehl, wenn Pfade, die im Array Erweiterung DLL nicht verfügen. 
  
## <a name="see-also"></a>Siehe auch

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

