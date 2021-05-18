---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Letzte Änderung: 24. Februar 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279535"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initiiert die Entsperrprozedur für eine Datei mit persönlichen Ordnern (PST).
  
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
    
## <a name="remarks"></a>Hinweise

Die vom wzDllPath-Parameter angegebene DLL muss mit einem digitalen Zertifikat signiert werden. Die DLL muss auch eine Funktion mit der folgenden Signatur exportieren.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Diese Funktion wird mit einem Zeiger auf das IMsgStore-Objekt für das PST, einem Zeiger auf ein IUnknown-Objekt, das die IPSTOVERRIDE1-Schnittstelle implementiert, und einem Zeiger auf die ursprünglich über pvClientData bereitgestellten Daten aufgerufen.
  
Weitere Informationen finden Sie unter Implementieren eines PST-Außerkraftsetzungshandlers zum Umgehen der [PSTDisableGrow-Richtlinie in Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

