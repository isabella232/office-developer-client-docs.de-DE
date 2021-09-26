---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Last modified: February 24, 2013'
ms.openlocfilehash: c7c074bbfb365d8a975bee12c5611c4d0809dc1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620534"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initiiert die Entsperrungsprozedur für eine persönliche Ordnerdatei (PST).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Parameter

 _pwzDllPath_
  
> [in] Ein Zeiger auf den Pfad einer Dynamic Link Library (DLL) eines Drittanbieters.
    
 _pvClientData_
  
> [in] Ein Zeiger auf Clientdaten, der vom PST-Anbieter an nachfolgende Aufrufe der HrTrustedPSTOverrideHandlerCallback-Funktion der DLL übergeben wird. Diese Clientdaten können von der DLL verwendet werden, um zu überprüfen, ob das PST entsperrt werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die durch den wzDllPath-Parameter angegebene DLL muss mit einem digitalen Zertifikat signiert werden. Die DLL muss auch eine Funktion mit der folgenden Signatur exportieren.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Diese Funktion wird mit einem Zeiger auf das IMsgStore-Objekt für das PST, einem Zeiger auf ein IUnknown-Objekt, das die IPSTOVERRIDE1-Schnittstelle implementiert, und einem Zeiger auf die ursprünglich über pvClientData bereitgestellten Daten aufgerufen.
  
Weitere Informationen finden Sie unter [Implementieren eines PST-Überschreibungshandlers zum Umgehen der PSTDisableGrow-Richtlinie in Outlook 2007.](https://support.microsoft.com/kb/956070)
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

