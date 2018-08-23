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
description: 'Zuletzt geändert: 24 Februar 2013'
ms.openlocfilehash: 62269b823810964fc0e5749aa6a57d39c503e2b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573579"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Initiiert das Aufheben der Sperre Verfahren für den persönlichen Ordner (PST).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Parameter

 _pwzDllPath_
  
> [in] Ein Zeiger auf den Pfad zu einer Drittanbieter-Dynamic-Link Library (DLL).
    
 _pvClientData_
  
> [in] Ein Zeiger auf die Clientdaten, die vom Anbieter PST in nachfolgende Aufrufe an die DLL HrTrustedPSTOverrideHandlerCallback Funktion übergeben werden. Diese Clientdaten können von der DLL verwendet werden, zur Unterstützung beim Überprüfen, ob die PST-Datei aufgehoben werden soll.
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der Funktionsaufruf war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der WzDllPath-Parameter angegebene DLL-Datei muss mit einem digitalen Zertifikat signiert werden. Die DLL muss auch eine Funktion mit der folgenden Signatur exportieren.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Diese Funktion wird mit einen Zeiger auf das IMsgStore-Objekt für die PST-Datei, einen Zeiger auf eine IUnknown-Objekt, das die IPSTOVERRIDE1-Schnittstelle implementiert und einen Zeiger auf die Daten, die ursprünglich zur Verfügung gestellten PvClientData aufgerufen werden.
  
Weitere Informationen finden Sie unter [ein PST Außerkraftsetzung Handler für die Umgehung die PSTDisableGrow Richtlinie in Outlook 2007 implementiert wird](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

