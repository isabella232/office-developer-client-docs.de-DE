---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279556"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt dem Nachrichtendienst einen Dienstanbieter hinzu. 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a>Parameter

 _lpszProvider_
  
> in Ein Zeiger auf den Namen des hinzuzufügenden Anbieters.
    
 _cValues_
  
> in Die Anzahl der Eigenschaftswerte, auf die durch den _lpProps_ -Parameter verwiesen wird. 
    
 _lpProps_
  
> in Ein Zeiger auf ein Eigenschafts Wertarray, das die Eigenschaften des hinzuzufügenden Anbieters beschreibt.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. Der _ulUIParam_ -Parameter wird verwendet, wenn das MAPI_DIALOG-Flag im _ulFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Hinzufügen des Anbieters steuert. Die folgenden Flags können festgelegt werden:
    
  - MAPI_DIALOG: zeigt ein Dialog Feld an, in dem Sie nach Konfigurationsinformationen gefragt werden.
      
  - MAPI_UNICODE: der Anbietername und die Zeichenfolgeneigenschaften sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.
    
 _lpUID_
  
> Out Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner enthält, der den hinzuzufügenden Anbieter darstellt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Anbieter wurde dem Nachrichtendienst erfolgreich hinzugefügt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Mit der **IProviderAdmin:: CreateProvider** -Methode wird dem Nachrichtendienst ein Dienstanbieter hinzugefügt. Der Parameter _lpszProvider_ muss auf den Namen eines Anbieters verweisen, der zum Nachrichtendienst gehört. **CreateProvider** überprüft nicht, ob der Name mit dem Namen eines Anbieters im Dienst übereinstimmt. Wenn der übergebene Name nicht mit einem Dienstnamen übereinstimmt, ist der Aufruf erfolgreich, aber die Ergebnisse sind unvorhersehbar. Bei den meisten Nachrichtendiensten können Anbieter nicht hinzugefügt oder gelöscht werden, während das Profil verwendet wird. 
  
Nachdem alle verfügbaren Informationen zum Dienstanbieter aus der Datei MAPISVC. inf zum Profil hinzugefügt wurden, ruft **CreateProvider** die Einstiegspunktfunktion des Nachrichtendiensts auf, wobei der Parameter _ulContext_ auf MSG_SERVICE_ festgelegt ist. PROVIDER_CREATE. Wenn MAPI_DIALOG im _ulFlags_ -Parameter **** der CreateProvider-Methode festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ auch an die Einstiegspunktfunktion übergeben. Diese zusätzlichen Parameter ermöglichen es dem Dienstanbieter, sein Eigenschaftenblatt anzuzeigen, damit der Benutzerkonfigurationseinstellungen eingeben kann. 
  
## <a name="see-also"></a>Siehe auch

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

