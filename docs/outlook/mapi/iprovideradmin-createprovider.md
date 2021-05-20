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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430805"
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
  
> [in] Ein Zeiger auf den Namen des hinzuzufügende Anbieters.
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte, auf die der  _lpProps-Parameter_ verweist. 
    
 _lpProps_
  
> [in] Ein Zeiger auf ein Eigenschaftenwertarray, das die Eigenschaften des hinzuzufügenden Anbieters beschreibt.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. Der  _ulUIParam-Parameter_ wird verwendet, wenn MAPI_DIALOG im  _ulFlags-Parameter festgelegt_ ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Anbieter-Addition steuert. Die folgenden Kennzeichen können festgelegt werden:
    
  - MAPI_DIALOG: Zeigt ein Dialogfeld an, in dem Konfigurationsinformationen angezeigt werden.
      
  - MAPI_UNICODE: Der Anbietername und die Zeichenfolgeneigenschaften sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.
    
 _lpUID_
  
> [out] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner enthält, der den hinzuzufügenden Anbieter darstellt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Anbieter wurde erfolgreich dem Nachrichtendienst hinzugefügt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Die **IProviderAdmin::CreateProvider-Methode** fügt dem Nachrichtendienst einen Dienstanbieter hinzu. Der  _lpszProvider-Parameter_ muss auf den Namen eines Anbieters verweisen, der zum Nachrichtendienst gehört. **CreateProvider** überprüft nicht, ob der Name dem Namen eines Anbieters im Dienst entspricht. Wenn der übergebene Name nicht mit einem Dienstnamen übereinstimmen, ist der Aufruf erfolgreich, die Ergebnisse sind jedoch unvorhersehbar. Die meisten Nachrichtendienste ermöglichen das Hinzufügen oder Löschen von Anbietern während der Verwendung des Profils nicht. 
  
Nachdem alle verfügbaren Informationen zum Dienstanbieter dem Profil aus der Datei Mapisvc.inf hinzugefügt wurden, ruft **CreateProvider** die Einstiegspunktfunktion des Nachrichtendiensts auf, und der  _ulContext-Parameter_ ist auf MSG_SERVICE_PROVIDER_CREATE. Wenn MAPI_DIALOG im _ulFlags-Parameter_ der **CreateProvider-Methode** festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ ebenfalls an die Einstiegspunktfunktion übergeben. Mit diesen zusätzlichen Parametern kann der Dienstanbieter sein Eigenschaftenblatt anzeigen, damit der Benutzer Konfigurationseinstellungen eingeben kann. 
  
## <a name="see-also"></a>Siehe auch

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

